# The Surfly Tutorial

### Introduction

###### Welcome to Surfly!

Surfly provides co-browsing, this enables you to share your browsing session with others..
You can start a Surfly session simply by entering the url of the website you want to browse into the 'start session' panel on your admin page.  You can then invite people to join you by sharing
the session url with them. This is the easiest and quickest way to co-browse and does not require any configuration.
However, if you wish to use Surfly as a feature on your own website, you can also add a Surfly button to your website. By doing this, you will be able to fully customise your session and use as much or as little of Surfly's functionalty within your own product.

###### During the session

A Surfly session allows you to share your browser with others. During the session, the mouse arrows from all users will be visible. Only the leader can select or click items on the page,
and if the leader decides to navigate to another url, the followers' screens will be synchronised so that they can also see this new page. The followers can take advantage of the drawing tool provided in order to highlight areas on the screen. During the session, users can communicate via text or video chat, share documents and invite others to join them.

###### Website Integration

If you wish to integrate Surfly to your website, visitors to your website will be able to click the "get live help" to request a session. They will then be queue'd until an agent (the person who receives the call) joins them. The passive member of the session is referred to as the follower, and the active member is the leader.
The leader will navigate the site, and the follower can help guide them through it. Initially the agent is the follower, and the website visitor is the leader, however you can choose to swap control at any time during the session.

###### Responding to incoming requests

To take a session, log in to your Surfly account, and navigate to the 'Queue' panel. Here, agents can see how many users they have queue'd up, their location, and the time they have been waiting. To take a session, the agent simply presses the "take call" button. If your visitors are logged in on your website already, you can also display metadata, such as the visitors name in the queue, so that the agent greeting them knows who they are.

![The Queue panel](https://raw.github.com/surfly/tutorial/master/screens/queue_panel.png)

###### The Admin panel

Surfly's admin panel allows you to track your users and your agents, and can be customised to suit your needs.

The buttons on the admin panel are:

 - The 'start' button, this allows you to immediatly start co-browsing.  When you click on this link you are asked to invite someone to join your session, by either sending them the session url directly, or via email.  
 - The 'queue' button, which gives you a list of queue'd users.  You can add metadata to this so that the agent knows more information about the user.
 - The 'history' button gives an overview of your sessions, the agent that took them and the duration.  You can also choose to add chat logs to the history panel.
 - The 'agent' button allows you to add agents to your account, and also gives you access to some information about agents such as their ID and the amount of sessions they have joined.
 - The 'settings' button lets you change your profile settings, and also includes your account details. Here, you can review your account plan, billing and personal information. The settings button also contains your integration information, the Surfly code snippet and the REST API key. 
 - The 'log out' button lets you exit the admin panel.

###### The tutorial covers:


 - [Session Modification](#session_modification)
 - [Integration](#add_surfly)
 - [Integration options](#advanced_options)
 - [Example use cases](#examples)

<a name="session_modification"></a>
### A Surfly session

Surfly comes with several different options for communicating with other users. You may decide to video or text chat, and followers can highlight areas with the drawing tool. 
If Surfly is integrated to your website, you can adapt the way a session starts, looks and behaves by changing the default settings. This is easily accomplished by specifying your prefences in the Surfly widget.  
If you would like greater control over the user interface, you can also fully customise it through the API (please see the documentation for further details).

The main points covered in the session modification section are: 

 - [Inviting users to join your session](#invite_user)
 - [Chat box](#chat_box)
 - [Video chat](#video_chat)
 - [Document sharing](#document_sharing)
 - [The window size options](#window_size)
 - [The drawing mode](#drawing_mode)
 - [Ending a session to display another page, or redirect to another page](#popupurl)
 - [Control switching](#customise_control_switching)

<a name="invite_user"></a>
#### Inviting a user to join your session

You can invite a user to join your session from your Surfly admin panel or from within a Surfly session: 
 - To start a session from the Surfly admin panel, navigate to the "start" button at the top left of your screen. 
 - Within the Surfly session the leader can, by default, invite people by clicking on the "add user" icon in the dock.

Both of these methods will load the following screen:

![invite_user](https://raw.github.com/surfly/tutorial/master/screens/invite_user.png)

You can then decide to either share the url of the session, or send an email to the user you wish to invite. 

<a name="chat_box"></a>
####Chat box

Surfly provides a chat box which can be used to communicate with other users. 
The default chatbox color is a soft red, however, this can be altered to match your website's theme. As can be seen in the image on the right, we changed the icons at the top of the chatbox from a light red to purple, which is more suited to our example website:

![Default changed color](https://raw.github.com/surfly/tutorial/master/screens/red_default_chat.png)  ![Changed chatbox colors](https://raw.github.com/surfly/tutorial/master/screens/changed_chatbox_colour.png)

Modifying the chat box can not only change its appearance, but also limit or extend the amount of control that the leader and the follower can have. By default, every user is able to exit the session but if you would like to allow your visitors full control over the session duration, you can choose to disable the exit icon from the agents' dock. 

![agent cannot exit](https://raw.github.com/surfly/tutorial/master/screens/agent_cannot_end.png)

You can also choose to minimise the chat window, and display only the icons in a dock. By deciding to use only the dock, you will also disable document sharing. 

![docked_only](https://raw.github.com/surfly/tutorial/master/screens/docked_only.png)

If you want to monitor the conversations between the agents and the users, you can choose to store the chat logs. You can access them by navigating to 'History' in your Surfly admin panel. The chat log section will have two icons inside, allowing you to either view the 
logs, or download them.  

![chatlogs](https://raw.github.com/surfly/tutorial/master/screens/logged_icon.png)

<a name="video_chat"></a>
#### Video chat

Surfly also allows you to communicate in your session with video chat. You can maximise the video to full screen, or restrict the video quality. However, if you do not wish to use this functionality you can easily disable it.

<a name="document_sharing"></a>
#### Document sharing 

If you wish to share documents during the Surfly session, you can click the paper icon to the bottom right of the chat box.

![share documents](https://raw.github.com/surfly/tutorial/master/screens/share_document.png)

Once you have clicked on it, you can upload a document from your desktop. The default for document sharing is that they can only be viewed, and not downloaded. However, you can change the settings
so that the files can be downloaded. It is also possible to share documents by dragging the directly to the chat box. 
If you wish, you may also disable the document sharing tool. 

<a name="window_size"></a>
#### Window Size options

The window is normally set to the person with the smallest screen, as this allows for a smooth transition into the Surfly session. If you see blank edges at the side of your screen, it is 
only because your screen is larger than the person you are co-browsing with. However, you can also decide to set a maximum or minimum size for the window.  Alternatively you may decide to remove the
set to smallest screen functionality altogether.

<a name="drawing_mode"></a>
#### Options for the drawing mode

The drawing option allows the followers within the Surfly session to highlight the areas on the screen that they wish to bring attention to. It works in a similar way to a highlighter, or 
a magic marker. By default, the drawings are temporary (they will fade out) and the color of the drawing tool is set to yellow. Of course, if you would prefer to have something different, both of these parameters can be changed, or you can turn the drawing function off entirely. 

In our example website we adapted the code so that the drawing mode would be permanent, and that the color of the drawings would be a vibrant green:
The green drawings underscoring the button are clearly visable to the leader of the session:

![changed drawing color](https://raw.github.com/surfly/tutorial/master/screens/drawing.png)

<a name="popupurl"></a>
#### Exiting the session display or redirect to another page

You may want to show a user another page after the session has finished. You can either show a popup window within the host website, or you can 
send them to another webpage.

In the example below, we have chosen to show the leader a popup url within their screen after the session has finished.  
The user can exit the popup window by clicking on the cross to the top right of the window.

![Popup url](https://raw.github.com/surfly/tutorial/master/screens/popup_example.png)

<a name="customise_control_switching"></a>
#### Customise control switching

If you want to be able to switch control between the leader and the follower, you can chose between either allowing the agent to take control, or to
request it from the leader. This could be useful for when users require further guidance through the website.

![request control](https://raw.github.com/surfly/tutorial/master/screens/agent_request.png)

As can be seen in the above image, the hand button is now bold, which means the agent can now use it to take, or request, control.


<a name="add_surfly"></a>
### Integration

To start an inbound Surfly session, you need to add the Surfly code snippet into your websites source code. The default parameters within the code snippet can be modified to allow for a 
seamless integration into your website. 

#### The Surfly Code Snippet

This can be found by clicking on the 'integration' panel in your account settings.
If you get a message telling you that you do not have the API key set up yet, click on
'Generate API'.

You should now be looking at:

![The integration page](https://raw.github.com/surfly/tutorial/master/screens/snippet_initial_screen.png)


In the 'domain names' section on the integration page, you need to specify the domains on which you want to show the Surfly button. This is easily set up,
if your website is hosted on "https://example.com", simply add "example.com" to the domain name list.

Finally, copy the code snippet and add it to the source code of your website.

When you open your webpage, you should see a "get live help" button at the bottom left of your screen. If a visitor clicks on this, they will be queue'd for support.  
You can answer this request via the Surfly admin panel.

<a name="start_session"></a>
### Starting a session

You can start a session in the following ways:
 - [The auto_start option](#auto_start)
 - [Customise your own button](#surflystart_anchor)
 - [Stealth mode](#stealth_mode)


<a name="auto_start"></a>
#### Auto start a session

If you enable auto start, it means the webpage including the code snippet will immediatly start a Surfly session. The page will, by default, display a red banner asking the
visitor to wait for an agent to join their session, and the queue pin number.
Auto start is especially useful if you want to display a certain webpage whilst the visitor is waiting for an agent to join them.  In our example webpage we have enabled autostart and
have customised the page so that the user is aware that they are in the queue.

![auto_start](https://raw.github.com/surfly/tutorial/master/screens/auto_start.png)

<a name="surflystart_anchor"></a>
#### Customise your own button

If you want to create your own button, you can use the #surflystart anchor, which can be integrated into your website's source code. You can choose the text you wish to write 
onto the button, and it can be fully styled with css so that it compliments your website design.  As you can see in the image below, we created our own start button. If a visitor to the website
clicks on it, it will lead them to a Surfly session.

![The end result](https://raw.github.com/surfly/tutorial/master/screens/Surflystart_anchor.png)

<a name="stealth_mode"></a>
#### Start a session in stealth mode

If you do not wish to have a visual button or link on your webpage, then you can use stealth mode. This allows visitors to initiate a Surfly session simply 
by pressing CTRL+ENTER.  The visitor will then be queue'd, and the Surfly session will start as normal.

<a name="button_appearance"></a>
#### Button Appearance

If you prefer, you can also adapt the default "get live help" button that Surfly provides. The buttons default appearance is red, with white text and sits to the bottom left of the screen. 

![default button appearance](https://raw.github.com/surfly/tutorial/master/screens/default_button.png)

The button appearance can be adapted by changing where it appears on your screen, and the colors and size of it. The position of the button can be moved to either the bottom right of the screen,
or to the middle left. You can further adapt the button to suit your needs by specifying the color of the button along with the font size and font color.

As you can see below, in the example website, we changed the position and the style of the button. This was achieved with a simple change to the code snippet.

```javascript

position:"middleright"
theme_font_background:"#000000",
theme_font_color:"#ffffff",
theme_font_size:"16",

```

The default color of the button was changed to black, which suits the theme 
of our example  website. The font color remains white, but the size of the font has increased to size 16, which also increases the size of the support button.

![example website with adapted Surfly button](https://raw.github.com/surfly/tutorial/master/screens/adapted_surfly_button.png)

The button, by default, will only be shown if an agent is logged in to the Surfly admin page. This can also be disabled, if you wish.

<a name="session_id"></a>
#### The session ID approach

The session ID approach is especially useful if you are already in contact with a customer via another medium. If the customer needs help navigating a website, the 
agent can direct them to start a co-browsing session. The customer will click on the link, and have a unique ID assigned to them, which they can give to the agent. 
As shown in the image below, this unique session ID will also be shown in the queue panel, allowing the agent to identify the customer, and join the session.

![The Queue panel](https://raw.github.com/surfly/tutorial/master/screens/queue_panel.png)


#### Integrate with existing chat solutions


It is also possible to integrate Surfly with existing chat solutions. For example, if you have already established your own video or text chat, you may want to add Surfly's co-browsing functionality to this.
In this case, Surfly can be integrated in such a way so that it acts as a transparent addition to your product and allow you to entirely customise the appearance of the session. 
As can be seen in the image below, the chat solutions are given a higher z-index than Surfly, so are stacked on top of the co-browsing session.  

![Chat solutions](https://raw.github.com/surfly/tutorial/master/screens/chat_solutions.png)

#### Create your own invite page

You can fully customise the page from which you want to invite users to start a session.  If your user has logged in to your website, you can also decide to add metadata to your
queue panel.  This allows you to pass information to your agents, such as name or email address. You also do not have to use the Surfly url for the session and can redirect your clients to a customised landing page.


<a name="integration_options"></a>
### Integration Options

This section covers:

 - [Surfly and third party cookies](#third_party_cookies)
 - [Session continuation](#session_continuation)
 - [Adding custom metadata to queue requests](#custom_metadata)
 - [Security Features](#security_features)
 - [Add information to a session log](#session_log_info)
 - [Customising the website appearance depending on who is in control](#customise_appearance_for_user)

<a name="third_party_cookies"></a>
#### Surfly and third party cookies

When integrating Surfly into your website, it is important to know that top level domains do not transfer third party cookies to the iframe, so instead you may choose to open a session in a 
new tab, or to use a CNAME.

<a name="session_continuation"></a>
#### Session continuation

Please Note: This is only supported for sessions started with the Surfly widget.

Cookies can be carried over from your website, and into the Surfly session. For example, if a user is logged into your website, they will remain logged in for the duration of the 
session. Once the session has finished, the information is sent back to the website. This allows a smooth transition into, and out of, the session.

There are two main ways to set up session continuation:

 - Full session continuation allows the transfer of all data, including (unlike soft session continuation), cookies with a HttpOnly tag.
 - Soft session continuation is more limited, and excludes cookies with a HttpOnly tag.

<a name="custom_metadata"></a>
#### Add custom metadata to Queue request

Adding custom metadata to the Queue requests allows you to give extra information about the user to the agent. For example, if the user is logged in to your website, then you can pass on some 
of this data, such as name and address, to the agent. Surfly will also use the name in order to display this in the chatbox, and the email in order to match the correct gravitar to the user.

You can also track the queue status from the clients side, so you can monitor the behaviour of the client when they leave, rejoin, or are waiting in the queue.

<a name="security_features"></a>
#### Security Features

Surfly's security features allow you the option to protect users data during the session, and, if required, restrict access to selected webpages. 

 - [Field masking](#field_masking)
 - [Blacklisting and Whitelisting](#blacklist_whitelist)

<a name="field_masking"></a>
##### Field masking

Field masking allows you to protect the leaders data during the Surfly session. If the user is required to enter sensitive information (such as payment details), into your website,
you can hide that input from the session followers. As shown in the images below, the leader is still able to read what they are typing into the form, but the followers (including the
agent) will only see a series of x's.

| [![Leader field masking](https://raw.github.com/surfly/tutorial/master/screens/Leader_fieldmasking.png)](The leader) | [![Follower field masking](https://raw.github.com/surfly/tutorial/master/screens/follower_fieldmasking.png)](The follower) |
|:---:|:---:|
| The leader | The follower |

To enable field masking, you need to add surfly_private to the form element in your html file, for example:

```
<input type = "text" name = "Login" surfly_private>
```

###### Please note: 

Whilst the leader can mask their data, and hide it from the followers, the followers cannot hide their data from the leader.

<a name="blacklist_whitelist"></a>
##### Blacklisting and Whitelisting

Please note: This option is only available to enterprise clients.

Blacklisting is used in order to deny users access from a select few webpages. If you want more control over what your users cannot access, whitelisting may be the most viable option.
Whitelisting allows access only to the pages specified in the code snippet. 

The format for blacklisting or whitelisting is a string representation of a JSON array.  You need to specify the restricted url, and then can optionally decide whether to add a redirect url
and a restriction type. If the redirect url is not specified, the user will be redirected to Surfly's default page. 

```
blacklist: JSON.stringify([{"pattern": ".*/restricted.*", "redirect": "{{referer}}#restricted"}])
```

In the above example, the pattern will prevent access to any url which includes 'restricted'.  If a user tries to access this page, they will be redirected to the home page with the restricted anchor added.

<a name="session_log_info"></a>
#### Add information to the session log

You can use the REST API to add additional information to the session log.  This is especially useful if you want to be able to monitor your agents, for example, you could log 
your agents individual sales.  
You can also create custom log messages using the Surfly.log() function. 

<a name="customise_appearance_for_user"></a>
#### Customise website appearance depending on who is in control

Surfly sessions are always comprised of one leader, and one or more followers. The leader is the only person who can click or type during the session, but you can switch control between
the leaders and the followers, if required.  You can specify the features you want to give to the leader and the follower during the session by enabling or disabling icons in the dock. 

<a name="examples"></a>
### Examples use cases
