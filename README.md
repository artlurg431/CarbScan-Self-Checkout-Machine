# CarbScan-Self-Checkout-Machine
A roblox studio free self checkout machine

These are instructions for v3.1.4PT

If you came here from the settings module from CarbEAS you can find the setup proccess [here](https://github.com/artlurg431/CarbEAS-EAS-Alarm-For-Roblox)

You can get the model in the release or the toolbox for a more stable but less updated version

This will be a long list on how to use this model

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

# CarbWifiNeo

<img width="1110" height="765" alt="image" src="https://github.com/user-attachments/assets/6208235b-4753-4950-ba3e-99b1621c4de4" />

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

<sub>_i recommend opening a forum in crb-product-help incase someone else has the same problem_</sub>

That is the **Bare** minimum to get this product set up, _still confused? [check out my video here](https://youtu.be/boNGEnkyBzE)_

Made by lots of people

If you find any bugs, please report them to me on discord, the faster i get bugs fixed the fatser i can release newer models. This is a public beta test, the model isnt stable!
Toolbox version comming soon, they usually take longer to receive updates due to stability concerns (another reason to report bugs) 

If you want to contribute, message me on discord!
