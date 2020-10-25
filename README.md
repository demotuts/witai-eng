<div dir="rtl">

# روبوت دردشة باستخدام wit.ai    

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%2012.45.28%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%2012.45.28%20PM.png)

MIT open source

## المستوى :
 متوسط
## ألمتطلبات : 

> لا يتطلب اي خبرة سابقة في مجال روبوتات الدردشة
> و لا حتى في مجال البرمجة

1. حساب على  [Facebook.com](http://facebook.com/) 
2. حساب على  [wit.ai](http://wit.ai/) 
3. حساب على  [glitch.com](http://glitch.com/)  


## الأهداف : 
في هذه المقالة ستتعلم و بصورة سهلة و لا تتطلب اي خبرة سابقة طريقة تجهيز روبوت دردشة  باستخدام منصة wit.ai 
سنقوم بصنع روبوت يرد على أسئلة عملاء شركة و همية ، سنسميها سفريات السلامة .
ربط Facebook Messenger مع روبوت الدردشة للرد تلقائيا على الأسئلة الواردة 

تعد روبوتات الدردشة من انجح وسائل خدمة العملاء و الرد على استفساراتهم كما انها مجانية
يقدم فيسبوك خدمة wit.ai المجانية و التي تمكنك في خطوات بسيطة من نشر روبوت دردشة يتمتع بالذكاء الصناعي


## الخطوات:
### 1. إنشاء روبوت الى على منصة wit.ai
### 2. إنشاء صفحة على فيسبوك
### 3. تهئة تطبيق على فيسبوك للرد على محادثات ال Messenger
### 4. نسخ و لصق تطبيق على منصة glitch.com لربط الروبوت مع ال Messenger
### 5. اختبار الربوت باستخدام Facebook messenger

***

### 1. إنشاء روبوت الى على منصة wit.ai

ما فائدة wit.ai هنا ؟ 

من السهل ان نصنع روبوتا يرد على سؤال واحد مثل "ما هي المسافة من مسقط الى الكويت"
دون استخدام اداة ذكاء اصطناعي مثل wit.ai ، لكن ماذا سيحدث ان سأل العميل "كم كيلو متر بين مسقط و الكويت؟" او ماذا يحدث ان سأل نفس السؤال بلغة اخرى؟
هنا يأتي دور الذكاء الاصطناعي في تحليل جمل العميل المكتوبة او المنطوقة NLP Natural Language Processing ، و استخدام الذكاء الاصطناعي القابل للتدريب في فهم الجمل المشابهة ، و بعدة لغات ، و تصنيفها اذا ما كانت سؤال عن مكان او زمان او درجة حرارة .. الخ، لمساعدتك في طلب الاجابة الصحيحة . حيث يمكنك ربط wit.ai بنظام البيع مثلا للإجابة على أسئلة من قبيل "كم سعر التذكرة من مسقط الى الكويت؟"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png)

كما يمكنك تدريب النظام لزيادة دقة فهمه لما يقصده السائل، كما سيرد معنا لاحقا في هذه المقالة.
خدمةwit.ai مجانية و متاحة للجميع.

بعد ان تسجل حسابا في خدمة wit.ai اشرع في إنشاء تطبيق جديد "New App"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.37.04%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.37.04%20PM.png)

اختر اسما لتطبيقك ، كل ما يهم انه اسم لم يستخدم من قبل على منصة wit.ai و بالحروف اللاتينية


[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.05.30%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.05.30%20PM.png)


ستظهر صفحة "Train Your App"
هنا سنقوم بتدريب التطبيق على العبارات التي نتوقع ان يستخدمها العملاء في أسئلتهم Utterances


[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.17.22%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.17.22%20PM.png)


لكي نفهم معا هذه الصفحة لنراجع معا ما هو هدفنا هنا ، نحن نريد ان "ندرب" wit.ai  على ان يتعرف على  ما يكتبه او ينطقه العميل ، و يستنتج ما الذي يقصده العميل ، هل يسأل عن الوقت ، هل يسأل عن مسافة؟ كما يستخلص التفاصيل التي تجعل من بحثنا عن اجابة اكثر دقة. إذا كما نرى في الرسم التوضيحي أدناه :

![](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%201.47.52%20PM.png)

### _**Utterance**_
 هي نماذج  من ما نتوقع ان يسألنا اياه العميل مثل "ما هي المسافة بين مسقط و الكويت؟"

### _**Intent**_
 هو استنتاج الغرض من عبارة  العميل اعلاه ، في هذه الحالة نستنتج ان العميل يبحث عن مسافة بين موقعين . لكن الى الان لم نعرف التفاصيل ، في الوقت الراهن Wit.ai لا تعلم الموقعين الذين بحث عن المسافة بينهما.
هنا يأتي دور 
### _**Entities**_
  و هي التفاصيل ، مسقط هي  Entity من نوع "موقع جغرافي" ، و كذلك "الكويت" هي Entity و من نوع "موقع".

كذلك هو الحال حينما يسأل العميل عن الوقت لموقع جغرافي يحدده بالإسم

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%201.47.19%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%201.47.19%20PM.png)

هكذا عرفنا ما تحتاجه منصة wit.ai كي تتدرب على فهم أسئلة العملاء ، بالطبع كلما زادت النماذج التي ندخلها لتدريب التطبيق كلما زادت قدرة تطبيق wit.ai على استنتاج ما يقصده العميل. 

> ### ملاحظة : منصة wit.ai تدعم اكثر من ١٣٠ لغة من ضمنها الأسئلة باللغة العربية ، الا ان هذا الدعم ما زال في المرحلة التجريبية بيتا ، لذلك سنتعامل في هذه التطبيق مع الاسئلة باللغة الانجليزية .

الان لن تواجهنا اي مشكلة في اتباع الخطوات التالية في ادخال النماذج و تدريب تطبيقنا.

نضيف بعض الأسئلة الخاصة بالمسافة بين مدينتين بصيغ منوعة
و نسمي هذا ال Intent بإسم `distanceBetween` هذا مهم جدا ، لاننا سنتعامل مع كل Intent أو إستنتاج بصورة مختلفة

و نتأكد من تظليل اسماء المدن و اختيار Entity من نوع location

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.10.16%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.10.16%20PM.png)

و كذلك أسئلة عن الوقت المحلي لبعض المدن
و نسمي هذا ال Intent بإسم `timeAtPlace` 
و أيضا و نتأكد من تظليل اسماء المدن و اختيار Entity من نوع location

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.19.26%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.19.26%20PM.png)


تدريب التطبيق على استنتاج مغزى الأسئلة يستغرق بضع ثواني الى بضع دقائق بعد ضفط زر
"Train Your App"
إنتظر حتى تتم علمية التدريب و من ثم 
بإمكانك مراجعة ذلك من قسم ال intent و قسم الEntities من على يسار القائمة

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.20.38%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.20.38%20PM.png)

كما يمكنك مراجعة 
كافة النماذج التي تم التدريب عليها من قسم Utterance من القائمة على الجهة اليسرى

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.22.59%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.22.59%20PM.png)

تقوم wit.ai ايضا بتخزين سجل كل الاسئلة التي سـالها العملاء في السابق و كذلك الاستنتاجات من تلك الاسئلة ، وهذا مفيد جدا لاعادة تدريب تطبيقنا على wit.ai على استنتاج المقصود من تلك الاسئلة الشائعة.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%202.24.37%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%202.24.37%20PM.png)

كل ما نحتاجه الان  من wit.ai هو الحصول على الرمز السري الذي يسمح لنا باستخدام التطبيق الذي أنشأناه توا من صفحة Settings

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.23.21%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.23.21%20PM.png)

***

### 2. إنشاء صفحة على فيسبوك

ما فائدة هذه الخطوة؟

كي يتمكن عملاء سفريات السلامة التواصل معنا بواسطة ال messenger سنحتاج لإنشاء صفحة خاصة بسفريات السلامة على فيسبوم (لن نقوم بإنشاء حساب شخصي جديد ان كنت من مستخدمي فيسبوك ، بل سنشئ صفحة جديدة تحت حسابك فيسبوك الخاص بك) عندها سيتمكن العملاء من ارسال استفساراتهم الى سفريات السلامة عبر ال messenger الخاص بصفحتها

لأنشاء صفحة على فيسبوك اتجه لهذا العنوان 
https://www.facebook.com/pages/creation
اذا كنت من مستخدمي فيسبوك ، فكل ما ستحتاجه هو اختيار اسم فريد  للصفحة  و نبذة عنها
اذا لم تكن مستخدمي فيسبوك فستحتاج لإنشاء حساب على فيسبوك

اضغط على زر "+" و اختار إنشاء صفحة جديدة ، أدخل الاسم الذي اخترته للصفحة و بيانات تفاصيل الصفحة

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.33.18%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.33.18%20AM.png)

***

### 3. تهيئة تطبيق على فيسبوك للرد على محادثات ال Messenger

ما فائدة هذه الخطوة؟

لاحظ ان wit.ai يمكن ربطها بصفحة في موقع سفريات السلامة على الانترنت او بتطبيقاتها الهاتفية ، لكننا اخترنا لهذه المقالة ربط wit.ai ب Messenger فيسبوك لسهولة عمل ذلك فنحن لن نحتاج تهيئة استضافة للموقع سفريات السلامة او لن نحتاج الى صنع تطبيق هاتف لاجل الاجابة على اسئلة العملاء ، كما انه بسبب انتشار استخدام فيسبوك فأن اكثر العملاء بامكانهم التواصل مع سفريات السلامة عبر ال Messenger


[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%2012.29.38%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%2012.29.38%20PM.png)

لإنشاء هذا التطبيق اتجه الى 
https://developers.facebook.com/apps/

و اضغط على "Create App"
و أختار الاختيار الأول "Manage Business Integrations"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.55.45%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.55.45%20AM.png)

أختار اسم للتطبيقك على فيسبوك ، غرض التطبيق هو الوصول الى المعلومات الخاصة  بك ، أي "App Purpose" "Yourself or your own business"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.57.24%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.57.24%20AM.png)

لكل تطبيق في فيسبوك هناك رمز سري خاص بذلك التطبيق ، للحصول على هذا الرمز السري سنذهب الى قسم الاعدادات Settings , Basic

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.44.07%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.44.07%20PM.png)

بالعودة الى "Dashboard"
هناك الكثير من المنتجات المرتبطة بفيسبوك ، لكن لتطبيقنا هذه سنختار Messenger

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.58.49%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.58.49%20AM.png)

العملاء سيتواصلون معنا عبر الصفحة التي أنشأناها اعلاه ، عبر خدة الماسنجر ، لذلك نحتاج ان نربط تطبيقنا بتلك الصفحة

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.01.57%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.01.57%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.03.03%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.03.03%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.04.37%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.04.37%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.10%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.10%20PM.png)

لأجل إستخدام هذا التطبيق للرد على محادثات العملاء ، نحتاج لإنشاء رمز Token 
و ذلك بالضغط على "Genrate Token"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.25%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.25%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.19.53%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.19.53%20PM.png)


***

### 4. نسخ و لصق تطبيق على منصة glitch.com لربط الروبوت مع ال Messenger

ما فائدة هذه الخطوة؟

في الخطوة ١ اعلاه استخدمنا wit.ai للتعرف على ما يقصده العميل و ترجمة ذلك الى مخرجات يمكننا استخدامها في البحث عن اجابة لسؤال العميل . wit.ai لا تعرف الاجابة ، هي فقط تترجم لنا سؤال العميل .
فمثلا حين يسأل العميل عن "المسافة بين بيروت و عمان" ، تعطينا wit.ai  مخرجات مفادها ان العميل يبحث عن مسافة بين موقعين ، و انه ذكر مدينتين هما "مسقط" و "الكويت" ، كما تشمل المخرجات خط الطول و العرض لكل مدينة.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png)


هذا نموذج للمخرجات التي نحصل عليها من السؤال أعلاه
</div>

```
{
    "text": "What's the distance between Beirut and Amman?",
    "intents": [
        {
            "id": "340263910599935",
            "name": "distanceBetween",
            "confidence": 0.97
        }
    ],
    "entities": {
        "wit$location:location": [
            {
                "id": "3487207574650572",
                "name": "wit$location",
                "role": "location",
                "start": 28,
                "end": 34,
                "body": "Beirut",
                "confidence": 0.9195,
                "entities": [],
                "resolved": {
                    "values": [
                        {
                            "name": "Beirut",
                            "domain": "locality",
                            "coords": {
                                "lat": 33.89331817627,
                                "long": 35.501571655273
                            },
                            "timezone": "Asia/Beirut",
                            "external": {
                                "geonames": "276781",
                                "wikidata": "Q3820",
                                "wikipedia": "Beirut"
                            },
                            "attributes": {}
                        }
                    ]
                },
                "type": "resolved"
            },
            {
                "id": "3487207574650572",
                "name": "wit$location",
                "role": "location",
                "start": 39,
                "end": 44,
                "body": "Amman",
                "confidence": 0.9328,
                "entities": [],
                "resolved": {
                    "values": [
                        {
                            "name": "Amman",
                            "domain": "locality",
                            "coords": {
                                "lat": 31.955219268799,
                                "long": 35.945030212402
                            },
                            "timezone": "Asia/Amman",
                            "external": {
                                "geonames": "250441",
                                "wikidata": "Q3805",
                                "wikipedia": "Amman"
                            },
                            "attributes": {}
                        },
                        {
                            "name": "Amman Governorate",
                            "domain": "region",
                            "coords": {
                                "lat": 31.583690643311,
                                "long": 36.333351135254
                            },
                            "timezone": "Asia/Amman",
                            "external": {
                                "geonames": "250439",
                                "wikidata": "Q472788",
                                "wikipedia": "Amman Governorate"
                            },
                            "attributes": {}
                        }
                    ]
                },
                "type": "resolved"
            }
        ]
    },
    "traits": {}
}
```


<div dir="rtl">


دورنا الان هو الاستفادة من تلك المخرجات في الاجابة على سؤال العميل ، بمعنى ان نحسب المسافة بين خطي الطول و العرض لكل مدينة ، لحسن الحظ كل تلك الحسابات متوفرة في التطبيق الذي ستقوم بنسخه بضغطة زر واحدة الى حسابك على منصة glitch.com 

منصة glitch تغنينا عن استخدام استضافات و سيرفرات معقدة ، فهي تهئ لنا الربط بسهولة شديدة بين تطبيقنا على wit.ai و فيسبوك Messenger


التطبيق ايضا يستخدم المخرجات من الاسئلة الخاصة بالوقت مثل "ما هو الوقت الان في تونس؟" لطلب التوقيت المحلي تلقائيا من من خدمة التوقيت من موقع.

[worldtimeapi.org/api](http://worldtimeapi.org/api/)

ادناه نموذج للمخرجات التي نحصل عليها من تطبيق wit.ai حينما يسأل العميل "ماهو الوقت الان في تونس؟"

</div>

```
{
    "text": "What's the time in Tunis?",
    "intents": [
        {
            "id": "3303593069738308",
            "name": "timeAtPlace",
            "confidence": 0.9944
        }
    ],
    "entities": {
        "wit$location:location": [
            {
                "id": "3487207574650572",
                "name": "wit$location",
                "role": "location",
                "start": 19,
                "end": 24,
                "body": "Tunis",
                "confidence": 0.9342,
                "entities": [],
                "resolved": {
                    "values": [
                        {
                            "name": "Tunis",
                            "domain": "locality",
                            "coords": {
                                "lat": 36.818969726562,
                                "long": 10.165789604187
                            },
                            "timezone": "Africa/Tunis",
                            "external": {
                                "geonames": "2464470",
                                "wikidata": "Q3572",
                                "wikipedia": "Tunis"
                            },
                            "attributes": {}
                        }
                    ]
                },
                "type": "resolved"
            }
        ]
    },
    "traits": {}
}
```

<div dir="rtl">
فقط توجه الى صفحة المشروع

https://glitch.com/~few-quintessential-horesradish

هو باختصار مشروع مبرمج بلغة `Node.JS`

اذا لم تسجل دخول ، سجل دخولك لمنصة glitch ، كي تنسخ هذا التطبيق و تستخدمه فقط اضغط على زر "Remix Your Own" 
و ستقوم المنصة تلقائيا بنسخ المشروع و اضافته الى حسابك و إنشاء عنوان انترنت جديد له ، سيستغرق ذلك بضع دقائق

<!-- Remix Button -->
<a href="https://glitch.com/edit/?utm_content=project_few-quintessential-horesradish&utm_source=remix_this&utm_medium=button&utm_campaign=glitchButton#!/remix/few-quintessential-horesradish">
  <img src="https://cdn.glitch.com/2bdfb3f8-05ef-4035-a06e-2043962a3a13%2Fremix%402x.png?1513093958726" alt="remix this" height="33">
</a>

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.24.59%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.24.59%20PM.png)

بإمكانك الان فتح التطبيق الذي نسخته من داخل حسابك على glitch 

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.34.15%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.34.15%20PM.png)

اضغط على Share بالجهة اليسرى من الصفحة

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.33%20PM%20copy.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.33%20PM%20copy.png)

اختار "Live App" هذا كان عنوان تطبيقك الذي تريد ربطه مع فيسبوك
 نتجه الان الى فيسبوك و الى اعدادات تطبيقنا هناك و تحت عنوان Messenger و تحت settings
و نختار اضافة webhook
"Add Callback URL"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.07%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.07%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.49%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.49%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.48.41%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.48.41%20PM.png)

نلصق العنوان الذي نسخناه من تطبيق glitch.com و نلصقه هنا , لكن نضيف كلمة "/webhook" الى نهاية العنوان، كي يبدوا كما هو في الصورة ، لكن تذكر ان عنوان تطبيق glitch الخاص بك  سيكون مختلفا عن العنوان اعلاه ، تذكر ان تستخدم عناوانك الذي نسخته من glitch
 في المساحة السفلى ادخل كلمة `verifytoken` و هي كلمة اخترناها عشوائيا ، لكن يجب ان تطابق ما سنضيفه لاحقا في ملف الاعدادات في تطبيق glitch

الان فيسبوك Messanger  يعرف الى اين يمرر الأسئلة الواردة

بالعودة الى التطبيق في موقع glitch.com
 اختار من القائمة اليسرى ملف ".env" و هو الملف الخاص بالاعدادات
غني عن القول ان مدخلاتك ستختلف عن المدخلات التي تظهر ادناه في الصورة ، اتبع الخطوات المكتوبة ادناه

[<img src="
https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.15%20PM.png" width="60%"/>](
https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.15%20PM.png)

بعد نسخ التطبيق ستحتاج الى تخصصه ليعمل مع العناصر الاخرى التي جهزتها سابقا ، فقط سنضيف اليه :
*  كلمة سرية لتأكيد الرمز `FB_VERIFY_TOKEN` ، يمكن ان تكون اي جملة ، لكننا في الخطوة السابقة اخترنا في تطبيق فيسبوك ان تكون `verifytoken`
*  `WIT_TOKEN` الرمز من wit.ai ، نحصل عليها من صفحة settings من wit.ai
* صورة شاشة
*  `FB_APP_SECRET` الرمز السري لتطبيق فيسبوك الذي أنشأناه في الخطوة رقم ٣ 
* صور للشاشة تظهر جميع الخطوات
*  `FB_PAGE_TOKEN` الرمز السري لصفحة facebook المرتبطة بالتطبيق الذ أنشأناف في الخطوة رقم ٣
* صور للشاشة تظهر جميع الخطوات

***

### 5. اختبار الربوت باستخدام Facebook messenger
الان و بعد ان قمت بكل هذا المجهود ، بامكانك قطف ثماره
ارجع الى صفحة Facebook التي أنشأتها و اضغط على "View As Visitor"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.28.06%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.28.06%20PM.png)

و سيظهر لك زر المحادثة باستخدام Messenger

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.27.41%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.27.41%20PM.png)

 إسأل مثلا عن الوقت في تونس
What's the time in Tunis

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.25.37%20PM.png" width="30%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.25.37%20PM.png)

أو اكتب سؤالا مثل : ما هي المسافة بين بيروت و عمان ، باللغة الانجليزية
What's the distance between Beirut and Amman

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%208.32.06%20PM.png" width="30%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%208.32.06%20PM.png)

### > تذكر فقط ان المدن المتوفرة محدودة في هذا التطبيق

نستطيع ان نعود الى wit.ai و نراجع جميع الأسئلة التي وصلت للروبوت ، و نستطيع تحسين الأجابات

### > مبروك! لقد طورت للتو روبوت دردشة و ربطته مع فيسبوك Messenger

### اضافات اختيارية للروبوت 
بامكانك تطوير هذا الروبوت باستخدامه للتواصل مع عملائك على تويتر ، تليجرام او اي منصة اخرى
كما تتمتع روبوتات wit.ai بخاصية الاستجابة للاوامرالصوتية ، بدلا من كتابة الرسائل النصية.

كما اسلفنا سابقا فأن wit.ai تدعم اكثر من ١٣٠ لغة ، قد تود تجربة اعداد تطبيقك للتجاوب للأسئلة المكتوبة او المنطوقة باللغة العربية

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.39.30%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.39.30%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.49.49%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.49.49%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.52.45%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.52.45%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%208.04.03%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%208.04.03%20PM.png)


***

تطبيق glitch اعلاه مقتبس من نموذج ل 
Arnold Scott, Partner Engineer at Facebook 
https://glitch.com/~dapper-hungry-grapple

</div>
