<hr>
<br>

# آموزش دستورات ابتدایی گیت
<br>

 تنظیمات گیت در سه سطح دسته بندی میشوند :

1.  **سطح محلی یا Local :** صرفا همان یوزر که مخزن را ایجاد کرده است دسترسی دارد
2.  **سطح Global :** برای تمام یوزر هایی که از مخزن استفاده میکنند و مخزن را دریافت کرده اند
3.  **سطح سیستمی :** زمانی که در یک سیستم کامپیوتری چندین حساب کاربری باشد

1.  git config - - local
2.  git config - - global
3.  git config - - system

طریقه شناسایی نام خود به گیت :
#git_code git config --global user.name "Alireza"

شیوه شناسایی ایمیل :
#git_code git config --global user.email "test@gmail.com"

نمایش لیست کانفیگ های موجود در گیت :
#git_code git config --list

نمایش کانفیگ های Global :
#git_code git config --global --list

ویرایش پیکربندی Global :
#git_code git config - - global - - edit

نمایش نام کاربری پیکربندی شده :
#git_code git config user.name

**نکته :** در صورت مشخص نکردن سطح پیکربندی، گیت به صورت پیشفرض از حالت Local استفاده میکند.