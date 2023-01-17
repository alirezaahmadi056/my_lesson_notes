
ابتدا باید در وبسایت [back4app.com](http://back4app.com/) ثبت نام کنیم. این وبسایت یک واسط برای استفاده از Parse Platform میباشد که ما با ایجاد اکانت در آن، امکان استفاده از مزایای پارس پلتفرم را خواهیم داشت.
<br>
## افزودن کتابخانه parse به پروژه

در این مرحله بایستی از آدرس [github.com/parse-community/Parse-SDK-Android](http://github.com/parse-community/Parse-SDK-Android) کتابخانه Parse را به پروژه اندرویدی خود اضافه کنیم.

```groovy
//settings gradle
repositories {
    maven{url "https://jitpack.io"}
}

//build gradle
ext {
    parseVersion = "4.1.0"
}

dependencies {
		implementation"com.github.parse-community.Parse-SDK-Android:parse:$parseVersion"
}
```
<br>

## افزودن سه رشته زیر به فایل String

```XML
<string name="server_url">https://parseapi.back4app.com/</string>
<string name="app_id">your_app_id</string>
<string name="client_key">your_key</string>
```

**نکته :** اطلاعات بالا را بایستی از بخش App Status → Settings → Core Settings همان App که در Back4App ساخته ایم دریافت و جای گذاری کنیم.
<br>

## افزودن مجوز های دسترسی

کتابخانه Parse Platform از اینترنت استفاده میکند. پس به مجوز های زیر نیاز دارد.

```XML
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
```
<br>

## افزودن Meta Data

پس از افزودن مجوز ها به فایل Manifest بایستی یک سری Meta Data در همان فایل مانیفست و در بدنه تگ Application اضافه کنیم. این متا ها در ادامه لیست شده اند.

```XML
<meta-data
    android:name="com.parse.SERVER_URL"
    android:value="@string/server_url" />

<meta-data
    android:name="com.parse.APPLICATION_ID"
    android:value="@string/app_id" />

<meta-data
    android:name="com.parse.CLIENT_KEY"
    android:value="@string/client_key" />
```
<br>

## ایجاد کلاس Application

برای initialize کردن Parse بایستی یک کلاس از نوع Application ایجاد و کد های زیر را درون آن قرار دهیم.

```kotlin
class A:Application() {

    override fun onCreate() {
        super.onCreate()

        Parse.initialize(
            Parse.Configuration.Builder(applicationContext)
                .server(getString(R.string.server_url))
                .clientKey(getString(R.string.client_key))
                .applicationId(getString(R.string.app_id))
                .build()
        )

    }

}
```

**نکته :** پس از ایجاد کلاسی از نوع App بایستی در تگ application موجود در فایل Android Manifest خصوصیت زیر را اضافه کنیم.

```XML
<application
    android:name=".androidWrapper.A"
```
<br>

## تست Parse Platform

در نهایت برای تست اتصال به Back4app کافیست تا قطعه کد زیر را در اکتیویتی مورد نظر اضافه کنیم.

```kotlin
//test back4app
ParseInstallation.getCurrentInstallation().saveInBackground()
```
