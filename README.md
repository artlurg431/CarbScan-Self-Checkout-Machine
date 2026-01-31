# CarbScan-Self-Checkout-Machine
A roblox studio free self checkout machine

You can get the model in the release or the toolbox for a more stable but less updated version

This will be a long list on how to use this model

The instructions underneath are for v3.1.5PT, and its api and stuff. I will keep them there for legacy purposes, **scroll to where it says Instructions for v3.5.0**

# v3.1.5PT Instructions

First, ungroup the folder named UNGROUP, thats where everything is

When you ungroup, you should be met with this:

<img width="110" height="102" alt="image" src="https://github.com/user-attachments/assets/6ca1f5ba-116a-4a63-8054-8604494e9e9c" />

_Excluding the CRBApi folder which you put in replicated **storage**_

_You can see i have something in the CarbNet folder already, you however, shouldnt_

Make sure to only have 1 of each folders in workspace

Second, put the CRBApi folder in Replicated Storage
Like This:

![image](https://github.com/user-attachments/assets/7b491955-aa5d-46a0-85c5-41554a130af3)
_Note: this image is from v.3.0.0, not v.3.1.4PT_

Make sure you are putting it in Replicated **Storage** not _Replicated First_

To make your tool compatible make 2 String values and put them at the root of your tool, _not sure what a root is?, look [here](https://imgur.com/a/mmvWcQo)_

Name 1 string value "Object" and the other one "Price", change the values in the properties tab to what you want

Add another BoolValue and name it "HasBeenBought" put all of them at the root of your tool/item
_HasBeenBought is used for EAS, but you still need it_

# Settings

Settings are used for, well setting up the item, the values in the settings can be changed easily and dont require coding skills to change
![image](https://github.com/user-attachments/assets/345f80a5-672a-4528-a6e4-377e93010f6a)

One **Very** important setting you should change is CarbNet
<img width="830" height="68" alt="image" src="https://github.com/user-attachments/assets/04ad99e3-c68d-48fe-86e2-808cc153ad1e" />

<sub>_This is found in the GeneralSettings part of the module script_</sub>

It is used for utilising the [CarbNet Product](https://github.com/artlurg431/CarbNet)
If you are not planning on using it, please disable this



At the start of the settings module, you can see different variables available for us to change
Owners name should be changed to your name, but is not nesseccary

Allowed objects are the objects that can be scanned, remember the _Object_ string value you created? go back and see what you named the value on it, the table here in the Allowed objects is looking
for the names of the value of the Object string value, the value of your _Object_ should be written down there like it shows in the picture

# API Introduction

<img width="526" height="368" alt="image" src="https://github.com/user-attachments/assets/c102cbc9-d0ec-4826-b51a-aefd7656f3a2" />

<sub>_This image is from v2.0.3 of the API module, instructions stay the same_</sub>

**What the Api does**

The api is used for controlling selfserv with another product like [CRBEAS](https://github.com/artlurg431/CarbEAS-EAS-Alarm-For-Roblox)

**How can you use the API**

You can use it for controlling multiple different CRB products with the [CarbNet+ tablet](https://github.com/artlurg431/CarbNet)

_How to connect the different products to work together?_

First open the **logic** script present in every model, then select the "MODEL" value

<img width="294" height="302" alt="image" src="https://github.com/user-attachments/assets/d6498eba-5165-43f0-b657-bdd6ba93d4ea" />

Here you can see how in the properties the value is set to "A", thats what the CarbNet+ will use to differenciate between your different self checkouts

<img width="320" height="229" alt="image" src="https://github.com/user-attachments/assets/d0b48009-5034-440e-b39a-f070e8faa6a2" />


When adding a new one, just simply make that letter into a "B"

Aslong as the models are in their folder, the API script will do everything!

<sub>_This applies to nearly all new model_</sub>

<sub>_Please note: you need the **Free** CRBNet product to use the api_</sub>

# API Reasons

<img width="583" height="377" alt="image" src="https://github.com/user-attachments/assets/e5010659-e73b-47d3-8a82-fdda8d2cf69c" />

These reasons are used for knowing why the api was called and to know what function to pass

# Custom API Calls

This section will show you how **you** can create your own api call 

<sub>_(my code really sucks so i hope it wont be too difficult )_</sub>

Start from requiring the API module from whatever you want, like this

`local API = require(game.ReplicatedStorage.CrbAPI.API)`

From this, you now have access to call any function you want to the API module

To fire your function in the API module, just simply do this

`API.functions.Example("Model", "Color", "Request", "Reason")`

The "Model" should be the MODEL string value inside the Logic script, and make sure to include the .Value

The "Color" should be nil most of the time

The "Request" can be used for pretty much anything extra

The "Reason" is why you are calling the function. The reason has to be in the table like shown above

<img width="1666" height="616" alt="image" src="https://github.com/user-attachments/assets/2f447627-dfd9-4a9e-9f49-5671f1d91f2e" />

# APICall

This script should be inside of every models logic script

It takes events fire from the API module that you learned to do above, the API module fires the API Bindable based on the MODEL value inside of every model

Basically, `Invoker > API > API event > APICall > Logic`

This is how a API Call function looks like:

<img width="634" height="903" alt="image" src="https://github.com/user-attachments/assets/1f05bf55-93b2-4bd5-8cdb-eed0703be80a" />

ik it sucks but when it gets a event call from the API event it checks through all the reasons in the API and see if it matches it, if it does it does whatever function you like


<img width="294" height="305" alt="image" src="https://github.com/user-attachments/assets/d2cbe7d9-fb23-47ef-9ccf-454bb8d5d3eb" />

# CrbPack v3.5.0 Instructions

Every model i release gets easier and simpler to set up, for this one you literally dont need to do anything!

Seriously, once you put the CrbPack folder in your workspace you can leave it there and everything will put itself in its correct space

Although to add your own items you **do still need to do some stuff** but its simple! I promise!

First, open everything like this to the CustomItem, this item is here to help you with understanding how items work with this sco

<img width="285" height="449" alt="image" src="https://github.com/user-attachments/assets/95ed8d20-e8a2-4026-99fd-9fad37b2b9b6" />

<img width="232" height="160" alt="image" src="https://github.com/user-attachments/assets/8e947745-41f1-4bd4-81c5-c8715baac3d6" />

^^I dont know how to format these images correctly to show up well so just live with it

These values i selected are the most important part of your item. The 2 tob ones are **Bool Values** and the 3 bottom ones are **String Values**

The ones you need to edit are the **String Values**, Object is your item name that shows up on the sco among other things, Price is the price that shows up on your sco, SavingsPrice is the price that
shows up when using your Loyalty Card

Editing the savingsprice is optional.

To edit the Object value click on it and look at your properties tab

<img width="332" height="266" alt="image" src="https://github.com/user-attachments/assets/282d4f90-1b0a-4d9b-a799-e8fbdcd43f13" />

Click on "ChangeMe" and change that to what you want your item name to be, like "Water" or smth

For the price do the same thing as the Object value, click on it and look at the properties tab, click on "1.00" and change that to the price you want, make sure its numbers though.

# Settings and changing the overall settings of everything

<img width="1815" height="930" alt="image" src="https://github.com/user-attachments/assets/c918cabe-bfdc-45fb-8ad0-0a1c0a72c4dc" />

Most of the settings you would want to change are right here, i will explain each one

CarbNet - Not required anymore, you can leave it to either true or false

Ui - For custom ui's i will go over this later

DefaultStatLight - Again, i will go over this again

Pin - your universal employee pin, used on every product when needed

Ranks - Not used currently, will be used in 3.6 which will come out shortly

TimeBetweenScan - Not even sure if this is used anymore, but it basically just is the time you need to wait before scanning your next item (debounce)

Groupid - Not used currently

StaffRank - Not used currently

LockingTime - i think this is some old ahh legacy feature that dosent exist anymore

GiveCredit - Probably dosent even work anymore, just prints out my name on spawn, leave this disabled

RimLight - dosent exist anymore

AssitanceFreq - Havent figured out how to use this, would be annoying aswell, so maybe thats for the better

BootUp - Shows the machine bootup (Credits to Phontinox for it :p)

UnlockFromNet - CrbNet dosent exist anymore, this therotically does work i have implemented it and might work with crbnet if you enabled the sco in it which is auto hidden

ArePluginsEnabled - If you decided to torture yourself trying to find out how my code works then this would be used, not used officially

BootupSound - DOsent work anymore because of the new bootup screen (Thanks again to Phontinox for making it)

RequireStaffToInteract - Dosent exist yet sadly

You can scroll through the whole module and change everything to how you want

# CUSTOM UI'S

I honestly havent tested this (I KNOW CALL ME LAZY BUT NO ONE IS GONNA MAKE A CUSTOM UI FOR TS BECAUSE NO ONE IS GONNA USE THIS SCO AHHA)

Sorry for that crashout, but i actually havent tested this, but it should work aslong as you dont mess stuff up

First, open the screen model, then the screen part to find all of this

<img width="256" height="515" alt="image" src="https://github.com/user-attachments/assets/3d17c93d-e5aa-498b-8ec6-3876773305f7" />

Select this folder and duplicate it ctrl + d and whatever tf for mac users and then rename it to what you want, like "Custom" or smth

<img width="281" height="231" alt="image" src="https://github.com/user-attachments/assets/72037079-444b-4914-9613-41ea6fb09bac" />

After that, Move the default folder somewhere else and then everything in your new folde is free to customise, (im assuming you know how to change and make ui's)

BUT make sure to not delete or rename anything, doing that will mess stuff up, so just dont

Once your done, go to the settings module and go to Ui, change "Default" to your ui folder name, also please contact me on discord if you have issues with this, because i myself would too prob

<img width="311" height="43" alt="image" src="https://github.com/user-attachments/assets/de07fe4b-18a9-4d75-9621-16499e1b8cce" />

# Status Lights

These are thankfully easier to setup than the custom uis kinda

<img width="467" height="620" alt="image" src="https://github.com/user-attachments/assets/8faf90d3-efcb-4b8d-b1d6-25432c81e640" />

It is easy, if you want to change the default status light to one of these, go to where they are stored, which is here in TriLights

<img width="255" height="479" alt="image" src="https://github.com/user-attachments/assets/04c8c1a1-24a6-45fc-86a3-b4c6ff838ee8" />

Drag and drop them into the ModelPlugins folder whioch is in the Plugins folder, then delete or move the DefaultLight model somewhere else

Next, go to the settings module and go to DefaultStatLight, which looks like this:

<img width="762" height="35" alt="image" src="https://github.com/user-attachments/assets/48c1f58d-eabd-48c1-9bae-96fb3c93fdeb" />

Change "DefaultLight" to the name of the new status light your using, like "LightSaber" or "ZebraTriLight"

You can also make your own trilights!, just make sure it has 2 parts named StatusLight and StatusLight2 in them and then everything else is the same as the provided extra trilights

# CarbWifiNeo

<img width="1110" height="765" alt="image" src="https://github.com/user-attachments/assets/6208235b-4753-4950-ba3e-99b1621c4de4" />

The insturctions below are mostly outdated, although adding new wifi's is the same as adding extra sco's or eas'

This is a relitevly new product, here i will show you how to set it up (_The setup is the same for every other additional model_)

Also, you need the CrbNet model to use this product

When you first insert CarbWifiNeo into your game it should come in a folder like this:

<img width="319" height="30" alt="image" src="https://github.com/user-attachments/assets/2d9e4f06-b635-4070-905c-1deaf86d4e39" />

Inside there should be a bunch of empty folders, if you already have those folder, eg. EAS, SelfScan, CarbNet. Delete them.

If you already have CRBAPI in your replicated **storage** check that the one you already have is on the latest version (v.2.0.4) and if it is
leave it, if it isnt delete it and put in the new one (you will have to sadly put all of your settings back in for now)

Once you did all that you can ungroup the folder that everythings in by selecting it and pressing ctrl+u
if your planning on adding multiple of these go into the CarbWifiNeo model, then go into the logic folder, after that select the MODEL value
and in the properties menu change the value to B on your second model, then C for more models and so on...

#

_Still needing help? [check out my discord](https://discord.gg/N7vvn9tSur)_
Feel free to DM me, i will respond, i promise!

You can also email me at crbproducts.proton@gmail.com

<sub>_i recommend opening a forum in crb-product-help incase someone else has the same problem_</sub>

That is the **Bare** minimum to get this product set up, _still confused? [check out my video here](https://youtu.be/boNGEnkyBzE)_

Made by lots of people

If you find any bugs, please report them to me on discord, the faster i get bugs fixed the fatser i can release newer models. There shouldnt be any bugs, but please report them to me

If you want to contribute, message me on discord!
