#android-log

##Introduction
android lib - log

##System requirements
Android 2.2+

##Download
Download [the latest jar][1] or grab via Maven:

```xml
<dependency>
  <groupId>com.github.snowdream.android.util</groupId>
  <artifactId>log</artifactId>
  <version>1.0.4</version>
</dependency>
```

or Gradle:
```groovy
    compile 'com.github.snowdream.android.util:log:1.0.4'
```

##Usage
1.enable/disable log  
```java
Log.setEnabled(true);  
Log.setEnabled(false);  
```

2.set the Tag for the log  
```java
Log.setTag("Android");  
```

3.log simple  
```java
Log.d("test");  
Log.v("test");  
Log.i("test");  
Log.w("test");  
Log.e("test");  
```

4.log simple -- set custom tag  
```java
Log.d("TAG","test");  
Log.v("TAG","test");  
Log.i("TAG","test");  
Log.w("TAG","test");  
Log.e("TAG","test");  
```

5.log advance  
```java
Log.d("test",new Throwable("test"));  
Log.v("test",new Throwable("test"));  
Log.i("test",new Throwable("test"));  
Log.w("test",new Throwable("test"));  
Log.e("test",new Throwable("test"));  
```

6.log advance  -- set custom tag   
```java
Log.d("TAG","test",new Throwable("test"));  
Log.v("TAG","test",new Throwable("test"));  
Log.i("TAG","test",new Throwable("test"));  
Log.w("TAG","test",new Throwable("test"));  
Log.e("TAG","test",new Throwable("test"));  
```

7.Log to File

log into one file      
```java
Log.setPath("/mnt/sdcard/debug.txt");
Log.setPolicy(Log.LOG_ALL_TO_FILE);

Log.d("test 1");
Log.v("test 2");
Log.i("test 3");
Log.w("test 4");
Log.e("test 5");
```

log into one directory with a lot of log files
```java
Log.setPath("/mnt/sdcard/snowdream/log","log","log");
Log.setPolicy(Log.LOG_ALL_TO_FILE);

Log.d("test 1");
Log.v("test 2");
Log.i("test 3");
Log.w("test 4");
Log.e("test 5");
```

##License
```
Copyright (C) 2013 Snowdream Mobile <yanghui1986527@gmail.com>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

[1]:https://oss.sonatype.org/content/groups/public/com/github/snowdream/android/util/log/1.0.4/log-1.0.4.jar