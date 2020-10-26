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

Why?

We can connect our wit.ai app to web page on Safety Travels website, or its mobile app, but for this tutorial we've choosen to connect our wit.ai app to Facebook Messanger. So we don't need to build and host a web page or create a mobile app from scratch.

The other reason is Facebook has a huge user base, and many of Safety Travels clients would be Facebook users, and would likely have Facebook Messanger app on their mobile devices.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%2012.29.38%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%2012.29.38%20PM.png)

To create your Facebook app head to

https://developers.facebook.com/apps/

click on "Create App"

Then select "Manage Business Integrations"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.55.45%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.55.45%20AM.png)

Select a name for your Facebook app, because you're creating this app to access your own data on Facebook, meaning your Page and the associated Messenger messeges, in the App Purpose field select "Yourself or your own business"

This relates to the (A) part in the Facebook [diagram](#3-creating-a-facebook-app-that-uses-messenger-1)  above.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.57.24%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.57.24%20AM.png)

A new App ID and an App Secret will automatically be generated for your new app, we will need to copy and save the App Secret , because we will need it later on.

We can find it under Settings > Basic

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.44.07%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.44.07%20PM.png)

Head back to the Dashboard and you'll be offered many Facebook products to incorporate in your app, for our app we only want to select Messanger

This relates to the (B) part in the Facebook [diagram](#3-creating-a-facebook-app-that-uses-messenger-1)  above.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.58.49%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2011.58.49%20AM.png)

Customers will reach out to Safety Travels through Facebook Messenger associated with Safety Travels Facebook page.

This is why we will need to connect our application to this Safety Travels Page.

This is illustrated in the (C) part in the Facebook [diagram](#3-creating-a-facebook-app-that-uses-messenger-1)  above.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.01.57%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.01.57%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.03.03%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.03.03%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.04.37%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.04.37%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.10%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.10%20PM.png)

To be able to post messages back to our customers over Messenger, we need a token, we can get one by clicking on "Generate Token"

This relates to the (C) i) part in the Facebook [diagram](#3-creating-a-facebook-app-that-uses-messenger-1)  above.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.25%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.05.25%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.19.53%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.19.53%20PM.png)


***

### 4. Cloning a glitch.com projeict that will connect wit.ai with messanger Messenger service

Why?

Wit.ai is great in interperting what the customer would type, and translate the customers questions into Intents and Entities and produce them as output. But wit.ai cannot answer those questions on its own. 

We will still need to use this categorized output, that we got from step 1 above, to find matching answers.

So for example when a customer asks about "The distance between Chicago and Seattle" then wit.ai will give us an output that reflects the customer has the intent to learn the distance between 2 locations, and the output will include the lattitudes and longitudes of these 2 cities.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-22%20at%207.33.52%20AM.png)

Below is a sample for the output from wit.ai

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

Now it's up to us to use the information above to calculate the distance between the 2 cities.

Luckily you don't need to do any calculation, our gilitch.com project has all the code needed to calculate the distance.

You can clone and add the glitch.com project to your account with a single click of a button.

We're using glitch because it makes it extremely easy to deploy an app that connects our app on wit.ai and the our Facebook app with Facebook Messenger, without the need for hosting or complicated setups.

Our chatbot also make use of the output from questions about time, such as "What's the time now in Toronto?" to get the local time for a city from the following API

[worldtimeapi.org/api](http://worldtimeapi.org/api/)

Below is a sample output for when the customer asks about the time in a certain city


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

To complete this step , just head to the glitch project at

https://glitch.com/~aeolian-sponge-glade

in a nutshell, it's a Node.JS end point that will glow our other components together

To copy this project, click on the button below "Remix This" If you're not logged into glitch.com you would want to login.


<!-- Remix Button -->
<a href="https://glitch.com/edit/?utm_content=project_aeolian-sponge-glade&utm_source=remix_this&utm_medium=button&utm_campaign=glitchButton#!/remix/aeolian-sponge-glade">
  <img src="https://cdn.glitch.com/2bdfb3f8-05ef-4035-a06e-2043962a3a13%2Fremix%402x.png?1513093958726" alt="remix this" height="33">
</a>

Within few minutes glitch will automatically add the project to your account, clone and deploy the app for you witha new URL.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.24.59%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.24.59%20PM.png)

Now you can open the project that you have cloned

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.34.15%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.34.15%20PM.png)

On the left side of the screen click on "Share", and click on the "Live App" tab

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.33%20PM%20copy.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.33%20PM%20copy.png)

This now is the URL that points to your app, click on copy because this URL will be the where the Facebook app will send in the questions from Messenger, so we can forward it to wit.ai and get the output that will help us in generating an answer.

Now we head to the Facebook app, and click on Messenger on the left menu, and Settings 

Find the Webhook section in the page and click on "Add Callback URL"

This relates to the (C) ii) part in the Facebook [diagram](#3-creating-a-facebook-app-that-uses-messenger-1)  above.

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.07%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.07%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.49%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.46.49%20PM.png)

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.48.41%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.48.41%20PM.png)

Paste the URL we've copied earlier from our glitch.com project and add the suffix `/webhook` to the end of the URL, so the correct address is `https://YOUR_PROJECT_URL/webhook`

Remember that the address to your glitch.com project will be different than the one you see here.

In the field below, "Verify Token" enter `verifytoken`, we choose this randomly it could be any other word or sentence, but we need to be consistent with the one we will enter later in our glitch project. 

After entering the Webhook and Verify Token, now we need to choose when we need to be notified by the Facebook App, we need to be notified when there's a message or action taken by the customer on the Messanger.

So we need the `pessages` and `pessaging_postbacks` 

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.47.30%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.47.30%20PM.png)

Now our Facebook app knows where to forward the questions coming from the Messenger 

We return now to our glitch.com project to complete its configuration

From the left menu select the ".env" file, this is where we will enter our configuration

Again it's needless to say that most of the values below will be different than the ones you will enter in your configuration file, just follow along to know where you'll get those values.

[<img src="
https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.15%20PM.png" width="60%"/>](
https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%2012.45.15%20PM.png)

To configure the glitch.com project and allow it to work with the other compnents of the chatbot, we will need to enter the following:

*  `FB_VERIFY_TOKEN` in a previous step we have decided that the Veirfy Token will be `verifytoken`
*  `WIT_TOKEN` this is the wit.ai Token that we copied in step one from wit.ai the Settings page 


[<img src="
https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.23.21%20PM.png" width="60%"/>](
https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-20%20at%209.23.21%20PM.png)


*  `FB_APP_SECRET` The Facbook App Secret that we copied in step 3 

*  `FB_PAGE_TOKEN` The Facebook Page Token that we have generated in step 3

***

### 5. Testing our bot using Facebook messenger

All the above hard work has paid off and it's time to use Facebook Messenger and test the chatbot

Head to the Facebook Page that we have created and click on "View As Visitor"

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.28.06%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.28.06%20PM.png)

You will see the Messenger button, click on it

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.27.41%20PM.png" width="60%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.27.41%20PM.png)

To test it, type for example : 
What's the time in Tunis

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.25.37%20PM.png" width="30%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%201.25.37%20PM.png)

Or  What's the distance between Beirut and Amman?

[<img src="https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%208.32.06%20PM.png" width="30%"/>](https://storage.googleapis.com/assets2020/Screen%20Shot%202020-10-21%20at%208.32.06%20PM.png)

### > Remember that the number of cities are limited

At this stage we can review the questions we've asked and wit.ai interpertations of those questions, we can fine tune and retrain the wit.ai app


### > Congratulations, you've just created a chatbot and connected it to Facebook Messanger 

### For those who want to go further

This chatbot can be used to connect with customers over Twitter , Telegram web or any other platform, and with the right modification it can respond to customers' voices

***

The glitch.com application above is inspired by a demo app by 
Arnold Scott, Partner Engineer at Facebook 
https://glitch.com/~dapper-hungry-grapple
