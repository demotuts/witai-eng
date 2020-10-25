# Chat bot with wit.ai and Facebook Messanger in under 10 minutes    

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-25%20at%201.37.54%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-25%20at%201.37.54%20PM.png)

Licene : MIT open source

## Level :
 Beginner / intermediate
## Requirements : 

>Does not require any chatbot developmenet expereince, does not require software development expereince

You'll only need :

1. [Facebook.com](http://facebook.com/) account
2. [wit.ai](http://wit.ai/) account.
3. [glitch.com](http://glitch.com/) account.

## Goals : 
Chatbots are considered one of the most successful customer service tools, it is also free using wit.ai free Natural Language Processing (NLP) frameork.

In this tutorial we will create a chatbot in easy and simple steps using wit.ai
The chatbot will automatically answer questions from the customers of a fictional bus operator which we will call Safety Travels.
These questions will be posed by customers using Facebook Messenger.

## Steps:
### 1. Creating an app on wit.ai
### 2. Creating a Facebook page
### 3. Creating a Facebook App that uses Messenger
### 4. Cloning a glitch.com projeict that will connect wit.ai with messanger Messenger service
### 5. Testing our bot using Facebook messenger

***

### 1. Creating an app on wit.ai

Why we're using wit.ai?
It's easy to create a bot that answers a single question like "ًwhat's the distance between Chicago and Seattle?"
But what if the users ask different variations of the question?
Like for example "How many Miles between Chicago and Seattle?" our chatbot will fail if we don't include all those variations, luckily we don't have to go this route.
We can simply use and train an NLP tool like wit.ai to respond to all variation of a questions  _**Utterances**_ by grouping them into ### _**Intents**_ , for example one intent for questions related to time "What's the time now in Boston?" or distance, tempreture, price etc. The intent output, will help us match the question asked with the relevant answers as we will see below.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png)

We can also train the wit.ai app with more variations of the questions to increase it's accuracy.
wit.ai is free and open for all.

After you signup or login into wit.ai , create a "New App"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.37.04%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%207.37.04%20PM.png)

and choose a unique name for your app

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.05.30%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.05.30%20PM.png)

You will be greeted by "Train Your App" page

Here you'll enter the questions that you expect the customers will ask "Utterances"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.17.22%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.17.22%20PM.png)

To understand what's going on on this page, let's reiterate again our goal here:

we're training our wit.ai app to understand what the customer has typed , or said. Is the customer asking for the time? or is the customer asking for a distance?
The app also extracts the details "Entities" that help us find a more accurate answers.

![](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%201.47.52%20PM.png)

### _**Utterance**_
These are examples of what the customer might ask from our bot.

### _**Intent**_
An intent is derived from the Utterance, so at this point we know the category of the questions, if it is about a time or a distance etc.
But if it is a distance, we still don't have enough information to find an answer, the bot stilll don't know what distance the customer is asking about. This is why we have 
 
### _**Entities**_
Entities are the details that will help us answer the customer's question, so if the customer is asking about the distance between Chicagk and Seattle, then Chicago is an Entity of type location, as well as Seattle.

It's the same when the customer asks about the time, the Entity here is of type location.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%201.47.19%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%201.47.19%20PM.png)

Obviously the more Utterances we enter to train the wit.ai app the more the chatbot is able to guess what the customer needs to know.

> ### wit.ai supports more than 130 languages

After the above, we should faceno problem in following the coming steps to enter Utterances and train our wit.ai app

we can enter some variations of questions asking for the distance between 2 locations.

Because we will handle each Intent differently we need to name each Intent a descriptive name, so Intents related to distance between 2 locations we will cal them `distanceBetween` it's very important to get them correctly.

We make sure that we highlight city names in our Utterance, these are our Entities, choose type location

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.10.16%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.10.16%20PM.png)

Let's also add Utterances/Questions about local time in few cities

Let's name this Intent `timeAtPlace`
Highlight the city, the city is our Entitiy and we select type location, if not auto detected.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.19.26%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.19.26%20PM.png)

After you click "Train Your App" training takes between seconds to minutes
Wait until training is complete then explore your Intents and Entities from the left menu to make sure that that they're all set correctly.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.20.38%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.20.38%20PM.png)


You can also revise all the Utterances from the Utterances section on the left

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.22.59%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.22.59%20PM.png)

wit.ai also stores all the Utterances / Questions which your customers has asked, this is extremly useful in going in retraining and refining how your bot interperts the customers' questions.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%202.24.37%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%202.24.37%20PM.png)

All we need at this point is to copy and save the "Server Access Token" for our app, from the settings section, we will need this Access Token soon.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.23.21%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.23.21%20PM.png)

***

### 2. Creating a Facebook page

Why?

We will need to create a new Facebook page for our fictional company "Safet Travels", We do this because we want when the customers send Messenger messages to be assoicated with this page.
To create a facebook page, visit the following link

https://www.facebook.com/pages/creation

If you are already a Facebook user all you'll need to do is to choose a name for your new page, if you aren't you'll need to sign up to facebook first.

Click on "+" and choose crate new "Page" , enter the name and description for your new page.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.33.18%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.33.18%20AM.png)

***

### 3. Creating a Facebook App that uses Messenger

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

### 4. Cloning a glitch.com projeict that will connect wit.ai with messanger Messenger service

ما فائدة هذه الخطوة؟

في الخطوة ١ اعلاه استخدمنا wit.ai للتعرف على ما يقصده العميل و ترجمة ذلك الى مخرجات يمكننا استخدامها في البحث عن اجابة لسؤال العميل . wit.ai لا تعرف الاجابة ، هي فقط تترجم لنا سؤال العميل .
فمثلا حين يسأل العميل عن "المسافة بين بيروت و عمان" ، تعطينا wit.ai  مخرجات مفادها ان العميل يبحث عن مسافة بين موقعين ، و انه ذكر مدينتين هما "مسقط" و "الكويت" ، كما تشمل المخرجات خط الطول و العرض لكل مدينة.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png)


هذا نموذج للمخرجات التي نحصل عليها من السؤال أعلاه

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


دورنا الان هو الاستفادة من تلك المخرجات في الاجابة على سؤال العميل ، بمعنى ان نحسب المسافة بين خطي الطول و العرض لكل مدينة ، لحسن الحظ كل تلك الحسابات متوفرة في التطبيق الذي ستقوم بنسخه بضغطة زر واحدة الى حسابك على منصة glitch.com 

منصة glitch تغنينا عن استخدام استضافات و سيرفرات معقدة ، فهي تهئ لنا الربط بسهولة شديدة بين تطبيقنا على wit.ai و فيسبوك Messenger


التطبيق ايضا يستخدم المخرجات من الاسئلة الخاصة بالوقت مثل "ما هو الوقت الان في تونس؟" لطلب التوقيت المحلي تلقائيا من من خدمة التوقيت من موقع.

[worldtimeapi.org/api](http://worldtimeapi.org/api/)

ادناه نموذج للمخرجات التي نحصل عليها من تطبيق wit.ai حينما يسأل العميل "ماهو الوقت الان في تونس؟"


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

فقط توجه الى صفحة المشروع

https://glitch.com/~aeolian-sponge-glade

هو باختصار مشروع مبرمج بلغة `Node.JS`

اذا لم تسجل دخول ، سجل دخولك لمنصة glitch ، كي تنسخ هذا التطبيق و تستخدمه فقط اضغط على زر "Remix Your Own" 
و ستقوم المنصة تلقائيا بنسخ المشروع و اضافته الى حسابك و إنشاء عنوان انترنت جديد له ، سيستغرق ذلك بضع دقائق

<!-- Remix Button -->
<a href="https://glitch.com/edit/?utm_content=project_aeolian-sponge-glade&utm_source=remix_this&utm_medium=button&utm_campaign=glitchButton#!/remix/aeolian-sponge-glade">
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

### 5. Testing our bot using Facebook messenger

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

***

تطبيق glitch اعلاه مقتبس من نموذج ل 
Arnold Scott, Partner Engineer at Facebook 
https://glitch.com/~dapper-hungry-grapple
