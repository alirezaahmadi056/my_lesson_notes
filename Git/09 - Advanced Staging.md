با دستور زیر میتوان Hunk های یک فایل را متوجه شد :
#git_code git add --patch configuration.txt
برای دیدن اطلاعات زیر از علامت سوال ؟ استفاده میکنیم
y - stage this hunk
n - do not stage this hunk
q - quit; do not stage this hunk or any of the remaining ones
a - stage this hunk and all later hunks in the file
d - do not stage this hunk or any of the later hunks in the file
e - manually edit the current hunk
? - print help

برای مشخص کردن دقیق Hunk ها از e استفاده میکنیم. سپس VS Code باز شده و برای Stage نشدن بخش هایی که اضافه شده اند و علامت + دارند، کافیست تا آنها را پاک کرده و فایل را ذخیره کنیم. برای index نشدن بخش هایی که حذف شده اند و علامت - دارند هم بایستی به جای منفی از Space یا " " استفاده کنیم. 