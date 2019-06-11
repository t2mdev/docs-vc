---
layout: docs
title: Clarity Connect
css: ['documents.css']
---

## What is Clarity Connect?

Clarity Connect is an advanced call routing / queuing software that integrates directly with your existing Skype for Business (SfB) software. As an Agent, inbound calls are pushed to your SfB client and can answered like any other call. However, there are some important call-handling rules that you must be aware of while operating as a Clarity agent.  
 
## Presence 
Your availability to take calls is determined by your Presence in the Skype for Business client.  
* **In order to receive calls, your presence must be Available.** You will not receive calls if it is set to anything else.  
* **If you miss an incoming call**, your presence will be changed to Away and RONA (Ring On No Answer). You must manually change your presence back to Available in order to begin receiving calls again.  
* **After a call is completed**, your presence will be changed to AfterCall Work. It will stay in AfterCall Work until either the configured time limit for after-call work expires or you manually close the conversation window for that call. In these cases, your presence will automatically change back to Available and you will be eligible to receive a new call.

## Answering a Call

When a call comes from the queue and rings your client, you will see the call pop up like any other call. Depending on the settings configured by your administrator, the name of the queue, the caller’s phone number or the Caller ID information may also be displayed. Answer the call and the Agent Console will be loaded in your client.  

## Agent Console

Once you answer an incoming call, the Agent Console and session IM window will open in your Skype for Business client:

The **IM Window** on the left side of conversation window will load with a message containing basic information about the call, such as the caller’s name, phone number, originating queue, etc. depending upon your organization’s configuration. It also contains a link to load the Agent Console for that conversation in a separate browser window if desired. This is where your IM conversations with the customer will occur, if your organization’s Clarity is configured for IM communications. 

The **Agent Console** itself contains all call control features, conversation and call flow details, and basic readouts of your call metrics. **It is important to note that ALL call handling should be performed using the buttons inside the Agent Console**, NOT by using the native Skype for Business call controls.  
 	 
## Call Handling

The Agent Console call controls are split into two sections – standard controls and Transfer-specific functions

* **DETAILS** Clicking the Details button allows you to select a Disposition and Sub-Disposition for the call, which are used for reporting. It also allows you to add a conversation note. These conversation details are internal and will be visible to other agents if the same individual calls again in the future.  

Click Save and Close to save your notes and disposition; otherwise click Cancel to exit without saving. This pop-up will also appear at the end of every call automatically. 

* **START HOLDING** Clicking the Start Holding button will place the caller on hold with music. Once this button is clicked, it will change to “Stop Holding” and begin a timer indicating how long the caller has been on hold. Clicking the button again will resume the call.
* **END** Clicking the End button will end the call and change your presence to AfterCall Work. Once the configured amount of time for aftercall work has expired, your presence will change back to Available. You can trigger this status change earlier by simply closing the conversation window.  
* **RECORD** Clicking the Record button will start recording the current call. If the call is already recording, clicking it again will have no effect.  
* **STOP RECORDING** Clicking the Stop Recording button will stop recording the call immediately. This affects both audio recording and IM transcripts. If recording has been stopped, it may be resumed by clicking the Record button.  

There are three types of call transfers available while on a call:

* **AGENT** Clicking on the Agent button will take you to an agent transfer submenu. This menu displays other agents in your queue and their current presence. To the left of each agent are four buttons, each for a different type of transfer

**Consult** allows you to speak privately with the agent you’re transferring the call to before bringing in the caller. In this type of transfer the caller is placed on hold while the two agents speak. While a caller is on hold for a Consult transfer, you may bring the other agent in for a 3-way call with the customer, transfer the call directly to the new agent, or return to the customer yourself without the new agent.  

**Transfer** is a traditional direct transfer. You may transfer a call to any agent if their presence is shown as Available. You will stay on the line with the customer until the new agent picks up.  
<br>**Invite** brings the new agent into the conversation with the customer creating a 3-way call; the original agent can then leave the call.  
<br>**VM** transfers the call immediately into the destination agent’s voicemail box without ringing the agent. 

* **QUEUE** Clicking the Queue button will take you to a queue transfer submenu. This menu shows the current queues in your organization that you may transfer to, as well as the number of agents online, available and the number of calls. There are two options to the left of each queue: 

**Consult** looks in the selected queue and finds an available agent with the necessary skills and creates a private one-on-one call between you and an available agent. From there you may bring the other agent into a 3-way call with the caller, transfer the call directly to the new agent, or return to the call with the customer yourself.  
<br>**Enqueue** immediately transfer the call directly to the selected queue and you are removed from the call. Their position in line in the new queue is determined by their original connection time, not the time of transfer.  

* **CONTACT** Clicking the Contact button will take you to a contact transfer submenu where you may transfer or consult with a user who is not configured as an agent in your contact center. In the search bar, you may search by e-mail or phone number. When you transfer a call using Contact, no metrics will be recorded for the call once it is transferred, because the destination contact does not have the Agent Console running. There will be three or four buttons displayed to the left of the contact.  

**Consult** allows you to speak privately with the contact you’re transferring the call to before bringing in the caller. In this type of transfer the caller is placed on hold while you and the contact speak. While a caller is on hold for a Consult transfer, you may bring the contact in for a 3-way call with the customer, transfer the call directly to the contact, or return to the customer yourself without the new contact.  
<br>**Transfer** is a traditional direct transfer. You may transfer a call to any contact if their presence is shown as Available or any phone number. You will stay on the line with the customer until the contact picks up.  
<br>**Invite** brings the new contact into the conversation with the customer creating a 3-way call; the original agent can then leave the call.  
<br>**VM** transfers the call immediately into the destination contact’s voicemail box without ringing the contact. This button will not appear if the contact is an external phone number.

* **METRICS** 
A metrics bar displays several statistics in the lower view of the Agent Console:

**Talk indicates how long you have been connected with the current call. 
<br>**Session** indicates how long the caller has been on the phone or in an IM session, including time spent navigating through the voice menu and time spent speaking with agents. 
<br>**# Queued** indicates how many calls are waiting in queues for which you are skilled. 
<br>**Available Agents** indicates how many agents are currently available to take calls in queues for which you are skilled. 
<br>**Your # Handled** indicates how many calls you have handled that day 







