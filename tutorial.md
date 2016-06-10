# The Surfly Tutorial

### Introduction

Welcome to the Surfly tutorial! 
Here you will find a detailed description on how to integrate Surfly into your website using the Surfly widget. 

The tutorial covers:

 - [Integrating Surfly into your website](#add_surfly)
 - [How to start a session](#start_session)
 - [Button Appearance](#button_appearance)
 - [Session Appearance](#session_appearance)
 - [Session Continuation](#session_continuation)
 - [Security Features](#security_features)

Our API is also highly detailed, so if you don't find what you are looking for, it may be in the 
documentation.  Otherwise, please do not hesitate to contact us for help.  

<a name="add_surfly"></a>
### Integrating Surfly into your website


#### The Surfly Code Snippet

This can be found by clicking on the 'integration' panel in your account settings. 
If you get a message telling you that you do not have the API key set up yet, click on
'Generate API'. 

You should now be looking at:

![The integration page](https://raw.github.com/surfly/tutorial/master/screens/snippet_initial_screen.png)


Copy the code snippet and add it to the source code of your website.
Check the scripts to make sure it is running, you may have to add https: to the src. 

You should see a button at the bottom left of your screen, inviting you to ask for live help.
Otherwise, you may get a message saying that your original domain is not listed on your Surfly integration page,
in order to get around this, simply add your domain to the widget's section
on the integration page.  You do not need to add https:// to the start of the domain name.  


<a name="start_session"></a>
### Starting a session

You can start a session in the following ways:
 - [The auto_start option](#auto_start)
 - [The #surflystart anchor](#surflystart_anchor)
 - [Stealth mode](#stealth_mode)


<a name="auto_start"></a>
#### Auto start a session

If you enable auto start, it means the page will immediatly redirect to a Surfly session. 
Set the auto_start flag to true in the Surfly code snippet.

```javascript

   auto_start:"true"
```
  

<a name="surflystart_anchor"></a>
#### Start a session with the anchor

In order to use this, you need to add the #surflystart anchor to a page with the Surfly code snippet.

```javascript

<a href="#surflystart"> Click to start a Surfly session!</a>
```

As can be seen from the link below, this will add a link within your website which visitors will click in order to start a Surfly session.

![The end result](https://raw.github.com/surfly/tutorial/master/screens/Surflystart_anchor.png)

Of course, you can customise the look of the link with css in order for it to fit in better with your own website design.

<a name="stealth_mode"></a>
#### Start a session in stealth mode

Stealth mode means that the visitor can initiate a Surfly session by pressing CTRL+ENTER.

As stealth mode is already the default in the Surfly code snippet, to disallow it, simply set ```stealth_mode:"false"```


<a name="button_appearance"></a>
### Button Appearance

The Surfly button can be completley adapted in order for it to fully integrate into your own website and its design.

Its default appearance is red, with white text and sits to the bottom left of the screen.

 
The position of the button can be moved to either to the bottom right of the screen, or to the middle left. 
Your preference can be added to the code snippet, for example:

```javascript 
  position:"middleright"
```

The full appearance of the button can be changed.  You can specify the color of the button along with the font size and font color, e.g:

```javascript
    theme_font_background:"#000000",
    theme_font_color:"#ffffff",
    theme_font_size:"16",
```  
This changes the color of the button to black, which suits the theme of our example website.  The font color remains white, but the size of the 
font has increased to size 16, which also increases the size of the support button. 

![example website with adapted Surfly button](https://raw.github.com/surfly/tutorial/master/screens/adapted_surfly_button.png)

Please Note: 
 - the way in which visitors can start a session (stealth mode, auto_start or #surflystart anchor) was covered in the 
   previous section, "Starting a session" 
 - A consise table detailing all of the options available for customization can be found in the API documentation.
 
<a name="session_appearance"></a>
### Session appearance

The main points covered in the session appearance section are: 

 - [Changing the chat box](#chat_box)
 - [Switching the control options](#switch_control)
 - [The window size options](#window_size)
 - [The drawing mode](#drawing_mode)
 - [Ending a session to display another page, or redirect to another page](#popupurl)

######Please note: 
 - A comprehensive and consise table detailing the session appearance can be found in the API documentation.

<a name="chat_box"></a>
####Chat box

###### The default:

 - The icons are a soft red color.
 - The agent:
   - Can see how many people are in the session
   - Can exit the session
   - Can maximise/ minimise the chat box window
   - Start videochat
   - Share documents

![default for follower](https://raw.github.com/surfly/tutorial/master/screens/default_for_agent.png)

 - The leader:
   - Can see how many people are in the session
   - Can exit the session
   - Can maximise/ minimise the chat box window
   - Can switch control
   - Can add a user to the session
   - Can navigate to a new url
   - Start videochat
   - Share documents   

![default for leader](https://raw.github.com/surfly/tutorial/master/screens/default_for_leader.png)

###### Changing the chatbox color

You can change the chatbox color in the Surfly code snippet by changing the css string. 

```javascript 

chat_box_color:"#80ffbf"
```

The icons at the top of the Chatbox have been changed from a light red to a deep blue, which is more suited to our website's theme:

![Changed chatbox colours](https://raw.github.com/surfly/tutorial/master/screens/changed_chatbox_colour.png)

###### The agent cannot end the session

You can also change the amount of control the members of the session can have.  For instance, if you do not want to allow the agent to 
be able to end the session, you can specify this in the code snippet:

```javascript
agent_can_end_session:"false",
```

This will remove the exit symbol from the agents chatbox:

![agent cannot exit](https://raw.github.com/surfly/tutorial/master/screens/agent_cannot_end.png)

###### Docked only

If you do not wish to have a chatbox, you can set ```docked_only:"true"```.  Only the panel containing the different icons will be visable:

![docked_only](https://raw.github.com/surfly/tutorial/master/screens/docked_only.png)

To change the position of the dock from the bottom left of your screen to the top of your screen add  ```dock_top_position:"true"``` to the code snippet

###### Storing the chat logs

If you wish to store the chat logs, set ```store_chat_logs: "true"``` in the code widget. 

After the session has ended, you can go to your dashboard and click on history.  The chat log will have two icons inside, allowing you to either view the 
logs, or download them.  

![chatlogs](https://raw.github.com/surfly/tutorial/master/screens/logged_icon.png)

<a name="switch_control"></a>
####Switching the control from leader to follower


The options are: 
 - agent_can_request_control. With the controllers permission, the agent can take control.
 - agent_can_take_control. In this case, the agent can take control without needing approval from the controller.

Both of these parameters gives the agent another option in their dock.  

![request control](https://raw.github.com/surfly/tutorial/master/screens/agent_request.png)

As can be seen in the above image, the hand button has changed from faded, to bold.  This is the button allowing the agent to take, or request, control.  


<a name="window_size"></a>
#### Window Size options

The window size can also be adjusted to suit your needs.  
If you are using the Surfly code snippet you can adjust the min/ max parameters.  

For example, this would set the window size to be larger than 200x200:

```
min_height: "200",
min_width: "200",
```

The window is normally set to the person with the smallest screen. This allows for a smooth transition into the Surfly session.
However, this can also be removed:    

```
set_to_smallest: "false"
```

<a name="drawing_mode"></a>
#### Options for the drawing mode

The drawing option allows the followers within the Surfly session to highlight the areas on the screen that they wish to draw attention to.  The 
drawing functionality can be adapted to change the mode or the color of the drawings.  To do this, simply specify your preferences in 
the code snippet.  

 - drawing_mode takes 3 options:
  - temporary, the drawings fade out. 
  - permanent, the drawings remain until the drawing_mode changes.
  - disabled, the drawing functionality is disabled.

 - drawing_colour:
  -  the default is yellow.
  -  but can be changed to any CSS string.


In our example website we adapted the code in order so that the drawing mode would be permanent, and that the color of the drawings would be 
a vibrant green:

```javascript
   drawing_color:"#55ff00",
   drawing_mode:"permanent",
```

The green drawings underscoring the button are clearly visable to the leader of the session:

![changed drawing colour](https://raw.github.com/surfly/tutorial/master/screens/drawing.png)

<a name="popupurl"></a>
#### Exiting the session display or redirect to another page

You may want to show a user another page after the session has finished.  You could show a popup window with the page you want to display, or you can 
redirect them to another url.  

Showing a window:
 - [Show a page in a popup](#showpage)
 - [Redirect the user to another url](#url_redirect)


<a name="showpage"></a>
###### Show a popup window

If you want to end the session and show the user a popup window, you can set the end_of_session_popup_url in the code snippet to point to the url of that page.
After the session ends, the window will be loaded on the users page.

```
end_of_session_popup_url:"your_url_here"
```

The user can exit the popup window by clicking on the cross to the top right of the window.

![Popup url](https://raw.github.com/surfly/tutorial/master/screens/popup_example.png)

<a name="url_redirect></a>
###### Redirect the user to another url

You can either redirect to the leader or the follower to another url after the session has finished.
 

This is simply:

```javascript

follower_redirect_url: "your url here"

```

Or, for the leader:

```javascript

leader_redirect_url: "Your url here"
```


<a name="session_continuation"></a>
### Session continuation

Please Note: This is only supported for sessions started with the Surfly widget. 

Information can be carried over from your website, and into the Surfly session.  Once the session has finshed, the information is returned back to the website.

There are two main ways to set up session continuation:
 - [Full session continuation](#full_session)
 - [Soft session continuation](#soft_session)

<a name="full_session"></a>
#### Full session continuation

Full session continuation requires a change in the host websites' load balancer configuration. It allows the transfer of all data, including (unlike soft session continuation), 
cookies with a HttpOnly tag.


<a name="soft_session"></a>
#### Soft session continuation

Soft session continuation allows you to carry out session continuation without changing the load balancer configuration. The Surfly widget needs to 
be on all the pages you wish to transfer the information from. For security reasons, the widget also needs to be present on the final page that the session
will end on.

In order to allow soft session continuation, you need to adapt the widget like so:

```
   cookie_transfer_enabled: "true",
   cookie_transfer_proxying: "false",
```

If you do not want the customer to start a session on a certain page, but wish to be able to transfer information from that page to a later Surfly session, you can always set 
the button to be hidden:

```
   hidden: "true",
```


<a name="security_features"></a>
### Security Features

The following security features can be integrated into your website:

 - [Blacklist](#blacklist)
 - [Whitelist](#whitelist)
 - [Auditlog](#auditlog)
 - [Form masking](#form_masking)


For both Blacklisting and Whitelisting, you may choose to add two options:
 - redirect, this allows you to redirect the user back to the page on which they clicked the restricted link.
 - type, this allows you to specify which requests get redirected.

<a name="blacklist"></a>
#### Blacklist 

This option is only available to the enterprise clients. Blacklisting restricts access to certain resources.

<a name"whitelist"></a>
#### Whitelist

This option is only available to the enterprise clients. Whitelisting allows access only to specific resources, and
therefore gives more control over where a visitor can access, or not.

<a name="auditlog"></a>
#### Auditlog

This allows you to see the records from sessions. 
You can also set a message for the logs:

```
Sufly.log("custom message")
```

<a name="form_masking"></a>
#### Form masking

This allows you to set 'surfly_private' on forms which may have sensitive data, such as payment details.
Surfly will not synchronise the content of the field to the followers.



{show the entire changed widget code here}
