<hr>
<br>

# آموزش کامل Commit
<br>

**نکته :** به اولین کامیتی که بر روی ریپو اعمال میشود، کامیت مرجع یا root commit میگویند.

**نکته 2 :** هر کامیت دارای یک هش کد میباشد. این هش با استفاده از سیستم رمز نگاری sha1 ساخته میشود و بسیار مهم و حیاتی خواهد بود.

نمایش خلاصه تر Commit ها : 
#git_code git log --oneline

گرفتن گزارش یک فایل خاص :
#git_code git log test.html

گزارش تک خطی از یک فایل خاص : 
#git_code git log --oneline test.html

نمایش اطلاعات بیشتر از یک فایل در کامیت ها :
#git_code git log -p test.html
**نکته :** برای خارج شدن از جزئیات بایستی Q را بزنیم
(END) Q
نمایش تمام اتفاقات یک کامیت :
#git_code git show hash_code ( or Head )

نمایش تمام اتفاقات یک فایل خاص در یک کامیت :
#git_code git show hash_code FileName

نمایش کامیت های 5 روز اخیر :
#git_code git log --since "5 days ago"

نمایش کامیت های انجام شده تا پریروز : 
#git_code git log --until "2 days ago"

نمایش کامیت های قبل از یک ساعت خاص : 
#git_code git log --until "15:55:26" --oneline

نمایش کامیت های یک نویسنده خاص : 
#git_code git log --author "AlirezaAhmadi"

نمایش کامیت هایی که یک کلمه خاص در آن وجود دارد : 
#git_code git log --grep "test"

نمایش تمام کامیت های تمام برنچ ها : 
#git_code git log --oneline --all

نمایش تمام کامیت های تمام برنچ ها در حالت گراف : 
#git_code git log --oneline --all --graph

ته دستورات نمایش جزئیات کامیت ها : 
#git_code git reflog