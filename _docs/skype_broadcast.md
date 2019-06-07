---
layout: docs
title: Skype Meeting Broadcast and T2M Cloud
css: ['documents.css']
---

## What is "Skype Meeting Broadcast"?

The new Skype Meeting Broadcast feature allows you to host extremely large meetings. This meeting is designed to be a town-hall style meeting where up to six presenters provide one-way communication to an audience of up to 10,000 users.

The meeting attendees join via a web browser on their computer or mobile device to watch and listen to the meeting.  The meeting attendees do not have the ability to turn on their microphone and communicate via audio.  If feedback from attendees is desirable, a Yammer room can be created to allow your meeting attendees to communicate in real time via instant message.

The following meeting types are best for Skype Meeting Broadcast: 

* Town hall Style Meetings 
* Meetings up to 10,000 users 
* Meetings that are sharing Video or PowerPoint information 

The following meeting types should NOT be used for Skype Meeting Broadcast: 

* Meetings that require attendees to participate in the audio conversation 
* Meetings that require participants to dial in via the PSTN (traditional phone network) 
* Meetings that require desktop sharing (Desktop Share can technically be done, but require a special adapter to convert your desktop share to a video source.) 

## Technical Requirements

There are several requirements that must be attended to before one can begin using Skype Meeting Broadcast


1.	The user who is scheduling meetings must be created in Office 365 and have the Skype for Business Plan 2 license assigned to the user. 
2.	The user’s Login Name (UPN), SIP Address and E-mail (SMTP) Addresses must match exactly. 
3.	You must be using the Office 2013 MSI or Click to Run installer running in Skype for Business Mode or the Office 2016 Click to Run installer.  Using the Office 2016 MSI installer will not work.  
4.	Your tenant administrator must have enabled the service on your O365 Account. 
5.	Ensure the Skype for Business Online PowerShell tools are installed. They can be found <a href="http://go.microsoft.com/fwlink/?LinkId=294688">here</a>   
6.	Launch PowerShell as Administrator.   
7.	Run the following commands, replacing “domain.onmicrosoft.com” with your tenant onmicrosoft domain name:

Set-ExecutionPolicy Unrestricted 
$Credential = get-credential 
$LyncSession = New-CsOnlineSession -Credential $credential  –OverrideAdminDomain 
"domain.onmicrosoft.com" 
Import-PSSession $LyncSession 
Set-CsBroadcastMeetingConfiguration –EnableBroadcastMeeting $True 

## Scheduling Skype Broadcast

In order to use Skype Meeting Broadcast, you must first schedule a meeting. 

1. Open your browser and go to https://broadcast.skype.com
2. Login with your Office 365 Credentials
3. The welcome screen will display all of your existing broadcast meetings cheduled for this month
4. Click on New Meeting

Next, you will be brought to the meeting creation page. Fill out the necessary information for the meeting:

* **Meeting Details** It is necessary to give your meeting a title and event time. You can start your broadcast meeting one (1) hour before the scheduled time and can last up to four (4) hours.
* **Event Team** The Event Team are the individuals who will be sharing a PowerPoint, Audio, or Video during the meeting.  You must specify at least one person.  You do not need to add yourself to the Event Team as the meeting organizer. 

There are two types of event team members: Presenters and Producers.  A presenter is someone who will be sharing Audio or Video.  A producer is someone who will control which camera is live.  If there is only a single audio/video source, then having a single person act as both producer and presenter is sufficient.

* **Attendees** Select who can join your meeting.  It is recommended to choose Anonymous or All Company.  Selecting All Company will require the users to login with their Office 365 account in order to watch the presentation
* **Video Recording** Select if you want your meeting to be recorded. 

Once all details have been entered, click Done and your meeting will be created. You may now return to the calendar page and verify that the meeting has been created

## Customizing Your Broadcast Meeting

You can customize certain aspects of your meeting. This is entirely optional, but it allows you to add some functionality to the meeting beyond what is possible in the initial set-up.

From the Skype Meeting Broadcast page, click on your meeting and select Customize from the top right. From here, you may add **Audience Participation Apps**. Remember that a Skype Broadcast Meeting does not allow for the audience to communicate over audio/video- if you want live feedback from the viewers of the meeting, this is the section where you can enable those features. You can add a Yammer Fee, Bing Pulse, and in the future, a Question/Answer feed

### Adding a Yammer Group Feed to the Meeting

First, click on **Right Panel App**. Click the radio button next to Yammer and click Select. Then, simply enter the necessary information for your Yammer group.

### Custom Troubleshooting and Support

Rather than the default Microsoft support link, you may also add a custom troubleshooting link for your audience to use if they experience issues with the meeting

###Custom Content Link

You may also set up a custom link for attendees so they may load content during the meeting. When you are finished setting up custom settings, click **Done** at the top of the screen to save.

Using Outlook (or any other method) send out the Meeting URL for attendees and Team Members. When viewing your meeting in the portal, click Show LInk and copy/paste that URL and distribute.

## Ensuring a Positive Experience on Event Day

A broadcast meeting typically has a large number of users. Thus, some prep work should be done prior to the meeting to ensure a positive experience for presenters and attendees both.

### 30 Minutes Prior to Meeting

Your presenters, organizers, and producers should login to the meeting using the Meeting Link at least thirty minutes prior to the meeting's start time (you may join up to one hour before the scheduled start). Click the **Sign in as even team member** button to join.

If you are not already logged into Office 365, it will prompt you to now. Depending on your browser, your Skype for Business client should join the meeting. Some browsers may prompt you before joining. 

When you join your Skype Meeting Broadcast, it will look very similar to a normal conference call.

* **The Upper Left Corner** will show all team members who are logged in. There can be a total of six people logged in.
* **The lower left corner** will show an IM conversation that can ONLY be seen by the event team members logged in.

Have all event team members who are going to use audio and video start them at this time. Remember, if you have multiple event team members in the same room, only one should start their video/audio.

Upload any PowerPoint presentations to the video conference at this time. It is recommended to put in a slide that welcomes people to the meeting to tell them when it will start.

### 15 Minutes Prior to Meeting

Decide what Audio/Video stream will be used to start the meeting. Right click on that user in the Participant List and choose **Make Active Video for Broadcasting**. You will see which video active at the top of the screen.

It is important to note that any Event Team Member can mute another user. For the 15 minutes prior to the start of the broadcast, you man want use the Active Video.

Lastly, choose how you want your content to be displayed. 
* Video Only
* Video and Content
* Content Only

## Starting the Meeting

Once you are satisfied with your configuration, click the Start Broadcast button

**NOTE: ONCE YOU HAVE STARTED A BROADCAST, YOU MAY NOT STOP IT. DOING SO WILL END THE MEETING AND MAKE THE MEETING URL INVALID FOR FUTURE USERS**

Once you have started the meeting broadcast (it can take up to 5 minutes for it to start), any user who may have already joined via the web will see the video and PowerPoint share.

When you are ready, have the producer unmute the audio of the presenter and start the broadcast meeting. Because of how the stream works, you should expect those watching on the web to be delayed by approximately 30 seconds from your live stream.

Those joining from the web should click the green Join the Event button from their invite URL. Users joining from the web can paus, rewind, and fast forward the session.

## Ending the Meeting

when your meeting is complete, click the Stop Broadcast button. It will warn you that you cannot restart the meeting once it's stopped.

Those who were watching on the web will be allowed to finish watching the event. Anyone who didn't join the meeting before can still join the URL and re-watch the video. This feed is available for the next four hours. 

After the meeting has completed, you may visit https://broadcast.skype.com to access a number of post-meeting options.
* **Reports** You can download a list of all users who joined your meeting
* **Video Recording** A few hours after the meeting is complete, you can download a recording of your video that you can then share.
