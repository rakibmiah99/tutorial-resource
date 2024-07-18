Laravel এ ডিপেন্ডেন্সি ইনজেকশন এবং সার্ভিস কন্টেইনার ব্যবহার করে কিভাবে একটি নির্দিষ্ট প্যারামিটার অটোমেটিকভাবে সার্ভিস কন্সট্রাক্টরে সেট করা যায় তা নিচে দেখানো হলো:

`app/Services/CompanyService.php`
```php
namespace App\Services;

use App\Models\Company;

class CompanyService
{
    protected $companyId;

    public function __construct($companyId)
    {
        $this->companyId = $companyId;
    }

    public function canDelete()
    {
        // আপনার লজিক এখানে হবে
        return Company::find($this->companyId)->orders()->count() == 0;
    }
}

```

Service Provider তৈরি করুন
```
php artisan make:provider CompanyServiceProvider
```


`app/Providers/CompanyServiceProvider.php`
```php
namespace App\Providers;

use Illuminate\Support\ServiceProvider;
use App\Services\CompanyService;
use Illuminate\Http\Request;
use Illuminate\Foundation\Application; //you can use service for method suggetion 
class CompanyServiceProvider extends ServiceProvider
{
    /**
     * Register services.
     *
     * @return void
     */
    public function register()
    {
        $this->app->bind(CompanyService::class, function ($app) {
            $request = $app->make(Request::class);
            $companyId = $request->route('id'); // Route থেকে ID গ্রহণ করা হচ্ছে

            return new CompanyService($companyId);
        });
    }

    /**
     * Bootstrap services.
     *
     * @return void
     */
    public function boot()
    {
        //
    }
}

```

## Used In Controller


`app/Http/Controllers/CompanyController.php`
```php
namespace App\Http\Controllers;

use App\Services\CompanyService;
use Illuminate\Http\Request;

class CompanyController extends Controller
{
    public function delete($id, CompanyService $companyService)
    {
        return $companyService->canDelete();
    }
}

```