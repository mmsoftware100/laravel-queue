# Laravel Queue

ပထမဆုံး ကြုံရတာကတော့ Permission Issues ပဲ
Mac မှာလည်း 

```bash
sudo chmod -R 777 storage
```

ဒါမျိုးပေးရတာ ခပ်လန့်လန့်။
အချိန်ပေးပြီး ဘယ်လိုပေးရမလဲ​ ပြန်ကြည့်ရမယ်။

User Group တွေနဲ့ Permission တွေအကြောင်း ဖတ်ကြည့်ရမယ်။



## Bash Logs


```bash
composer create-project laravel/laravel .
# update storage folder permission
# update db credential in .env

# queue အတွက် table ဆောက်
php artisan queue:table
php artisan migrate

# create job
php artisan make:job SendEmail
# The generated class will implement the Illuminate\Contracts\Queue\ShouldQueue interface, indicating to Laravel that the job should be pushed onto the queue to run asynchronously.

# update .env
# QUEUE_CONNECTION=database

# run artisan command
php artisan queue:work

```