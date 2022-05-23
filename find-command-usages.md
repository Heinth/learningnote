# Find command usages

### File Name ဖြင့်ရှာဖွေခြင်း <a href="#file-name-pa-ng-ya-pa-kh-ng" id="file-name-pa-ng-ya-pa-kh-ng"></a>

```
find /etc -name "*.conf"    
```

File name စာလုံး အကြီး၊ အသေး မရွေးစေချင်လျှင်တော့ `-iname` ဆိုတဲ့ option ကိုသုံးနိုင်ပါတယ်။

```
$ mkdir testing
$ cd testing
$ touch hello HelloGuys HelloThere
$ find . -name "hel*"
./hello
$ find . -iname "hel*"
./hello
./HelloGuys
./HelloThere
```

### Folder နှင့် File ခွဲခြားရှာဖွေခြင်း <a href="#folder-n-ng-file-kh-kh-ya-pa-kh-ng" id="folder-n-ng-file-kh-kh-ya-pa-kh-ng"></a>

```
$ mkdir HelloDir
$ find . -type d -iname "hel*"
./HelloDir
$ find . -type f -iname "hel*"
./hello
./HelloGuys
./HelloThere
```

### အချိန်ဖြင့်ရှာဖွေခြင်း <a href="#akh-n-pa-ng-ya-pa-kh-ng" id="akh-n-pa-ng-ya-pa-kh-ng"></a>



လွန်ခဲ့တဲ့ ၅ရက်လောက်အတောအတွင်းမှာ edit (သို့) modify လုပ်ထားတဲ့ File တွေ Folder တွေကိုရှာချင်လျှင်တော့ `-mtime` ဆိုတဲ့ option ကိုသုံးနိုင်ပါတယ်။ Default Parameter ကတော့ Day နဲ့ သတ်မှတ်ပါတယ်။ လက်ရှိနေ့မှ ၅ရက်အတွင်း ရှာဖွေမှာဖြစ်တဲ့အတွက် `-5` လို့သတ်မှတ်ပေးရပါမယ်။ `5` လို့ပဲသတ်မှတ်လိုက်မယ်ဆိုလျှင်တော့ ၅ရက်အတွင်းမဟုတ်တော့ဘဲ ၅ရက်မြောက်နေ့မှာ modify လုပ်ထားတဲ့ ဖိုင်တွေကိုပဲထုတ်ပြပေးမှာဖြစ်ပါတယ်။

```
$ find /home -mtime -5
$ find /home -mtime 5

```

### Size ဖြင့်ရှာဖွေခြင်း <a href="#size-pa-ng-ya-pa-kh-ng" id="size-pa-ng-ya-pa-kh-ng"></a>

File နှင့် Folder တို့ရဲ့ Size အကြီးအသေးပေါ်မူတည်ပြီး ရှာဖွေ မယ်ဆိုလျှင်တော့ `-size` option ရှိပါတယ်။ 5MB ပမာဏရှိတဲ့ File တွေ Folder တွေကိုရှာချင်တယ်ဆိုလျှင် -

```
$ find /home -size 5M
```

5MB ကနေ 20MB ပမာဏကြားရှိတဲ့ ဖိုင်တွေဆိုလျှင်တော့ -

```
$ find /home -size +5M -size -20M
ဒီနေရာမှာတော့ + ကို Greater Than အနေနဲ့သတ်မှတ်အသုံးပြုပြီး - ကိုတော့ Less Than အနေနဲ့အသုံးပြုပါတယ်။
```

User (သို့) Group ဖြင့်ရှာဖွေခြင်း

```
$ find / -user user1
$ find / -group group1
```

Permission ဖြင့်ရှာဖွေခြင်:

```
$ find /etc -perm 0755
$ find /etc -perm 0777
```

