<hr>
<br>

# برنچ ها در گیت :
<br>

## مفهوم و کاربرد برنچ :

هنگام توسعه بخش های جدید یک پروژه یا رفع باگ ها، بهتر است برنچ ایجاد کنیم. برنچ ها دقیقا از همان نقطه ای که ایجاد میشوند یک کپی از پروژه گرفته و ما تغییرات جدید را بر روی آنها اعمال میکنیم. اگر در نهایت تغییرات مورد تایید بود، برنچ را با برنچ دیگر ادغام خواهیم کرد. 

نمایش برنچ های لوکال :
#git_code git branch

نمایش برنچ های ریموت :
#git_code git branch -r

نمایش همه برنچ های موجود :
#git_code git branch -a

ایجاد برنچ جدید :
#git_code git branch new_feature

رفتن به برنچ با روش قدیمی :
#git_code git checkout new_feature

رفتن به برنچ با روش بهتر و جدیدتر : 
#git_code git switch new_feature

ادغام دستور ایجاد و رفتن به برنچ :
#git_code git switch -c test_feature

حذف کردن یک برنچ خاص :
#git_code git branch -d test_feature
**نکته :** قبل از حذف بایستی از این برنچ خارج شویم.

نمایش خفن تر لاگ های برنچ ها : 
#git_code git log --oneline --all --graph

## انواع ادغام کردن برنچ ها :

1: ادغام از نوع Fast Forward : یعنی همه تغییرات جلوی Master هستند و در Master تغییری رخ نداده
2: ادغام از نوع Not Fast Forward : در اینجا در Master هم اتفاقات و تغییراتی رخ داده است.