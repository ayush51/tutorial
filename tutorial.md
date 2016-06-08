# The Surfly Tutorial

### Introduction

Welcome to the Surfly tutorial! 
Here you will find a detailed description on how to integrate Surfly into your website, and adapt it to your needs.


The tutorial covers:

 - [Integrating Surfly into your website](#add_surfly)
 - [How to start a session](#start_session)
 - [Button Appearance](#button_appearance)
 - [Session Appearance](#session_appearance)
 - [Session Continuation](#session_continuation)
 - [Security Features](#security_features)
 - [Customizing Surfly](#customizing_surfly)

Our API is also highly detailed, so if you don't find what you are looking for, it may be in the 
documentation.  Otherwise, please do not hesitate to contact us for help.  

<a name="add_surfly"></a>
### Integrating Surfly into your website


#### The Surfly Code Snippet

This can be found by clicking on the 'integration' panel in your Settings. 
If you get a message telling you that you do not have the API key set up yet, click on
'Generate API'. 

You should now be looking at:

![The integration page](https://raw.github.com/surfly/tutorial/master/screens/snippet_initial_screen.png)


Copy the code snippet and add it to the source code of your website.
Check the scripts to make sure it is running, you may have to add https: to the src. 

You should see a button at the bottom left of your screen, inviting you to ask for live help.
Otherwise, you may get a message saying that your original domain is not listed on your Surfly integration page,
in order to get around this, simply add your domain to the widget's section
on the integration page.  


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

<a href="surflystart"> Click to start a Surfly session!</a>
```

As can be seen from the link below, this will add a link within your website which visitors will click in order to start a Surfly session.

![The end result](https://raw.github.com/surfly/tutorial/master/screens/Surflystart_anchor.png)

Of course, you can customise the look of the link with css in order for it to fit in better with your own website design.

<a name="stealth_mode"></a>
#### Start a session in stealth mode

Stealth mode means that the visitor can initiate a Surfly session by pressing CTRL+ENTER.

This is already the default in the Surfly code snippet, to disallow it, simply set ```stealth_mode:"false"```


<a name="button_appearance"></a>
### Button Appearance

The Surfly button can be completley adapted in order for it to fully integrate into your own website and its design.

The default position for the button is "bottomright", but this can easily be changed.  
In the Surfly code snippet, it is simply changing the default value, eg:

```javascript 
  position:"middleright"
```

The color, font size and the text color can also be changed, e.g:

```javascript
  theme_font_background:"#ff0080", 
  theme_font_color:"#ffffff",
  theme_font_size:"16",
```  

This then gives a much better integration into our example website: 

![example website with adapted Surfly button](https://raw.github.com/surfly/tutorial/master/screens/adapted_surfly_button.png)

Please Note: 
 - the way in which visitors can start a session (stealth mode, auto_start or #surflystart anchor) was covered in the 
   previous section, "Starting a session" 
 - A consise table detailing all of the options available for customization can be found in the API documentation.
 
<a name="session_appearance"></a>
### Session appearance

You can simply adjust the javascript snippet configuration to suit your needs, for example, by setting ```docked_only:"true"```,
you are able to remove the chat and video, and have just the icons available.

![docked_only](https://raw.github.com/surfly/tutorial/master/screens/docked_only.png)

You can also change the position of the dock from the bottom left to the top of your screen by using ```dock_top_position:"true"```

You can also change the look and the appearance of the chatbox, change the quality and size of the video, and switch the control from one user to another. 

The main points covered in the session appearance section are: 

 - [Changing the chat box](#chat_box)
 - [Switching the control options](#switch_control)
 - [The window size options](#window_size)
 - [The drawing mode](#drawing_mode)


######Please note: 
 - A comprehensive and consise table detailing the session appearance can be found in the API documentation.

<a name="chat_box"></a>
####Chat box

You can change the chatbox color in the Surfly code snippet by changing the css string. 

```javascript 

chat_box_color:"#80ffbf"
```

The icons at the top of the Chatbox have been changed from a light red to a deep blue, which is more suited to our website's theme:

![Changed chatbox colours](https://raw.github.com/surfly/tutorial/master/screens/changed_chatbox_colour.png)


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

There are two ways in which to adapt the drawing feature:
 - drawing_mode takes 3 options:
  - temporary, meaning that the drawings fade out. 
  - permanent, meaning that the drawing remain until the drawing_mode changes.
  - disabled, meaning that the drawing is turned off.

 - drawing_colour
  -  the default is yellow.
  -  but can be changed to any CSS string.


In the Surfly snippet this can be done as easily as the other changes

```javascript
   drawing_color:"#66ccff",
   drawing_mode:"permanent",
```
This changes the drawing function so that the drawings do not fade away, but remain on the page.  The color
of the magic marker has also been changed to a light blue.

![changed drawing colour](https://raw.github.com/surfly/tutorial/master/screens/drawing.png)

<a name="session_continuation"></a>
### Session continuation

Please Note: This is only supported for sessions started with the Surfly widgit. 

Information can be carried over from your website, and into the Surfly session.  Once the session has finshed, the information is returned back to the website.

There are two main ways to set up session continuation:
 - [Full session continuation](#full_session)
 - [Soft session continuation](#soft_session)

<a name="full_session"></a>
#### Full session continuation

A full session continuation requires a change in the host websites' load balancer configuration. It allows the transfer of all data, including (unlike soft session continuation), 
cookies with a HttpOnly tag.


<a name="soft_session"></a>
#### Soft session continuation

Soft session continuation allows you to carry out session continuation without changing the load balancer configuration. The Surfly widget needs to 
be on all the pages you wish to transfer the information from. For security reasons, the widgit also needs to be on the final page that the session
will end on.

In order to allow soft session continuation, you need to adapt the widget like so:

```
   cookie_transfer_enabled: "true",
   cookie_transfer_proxying: "false",
```

If you do not want the customer to start a session, but wish to be able to continue their session should they chose to later on in the process, you can always set 
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

(unknown as to what this is -> possibly to do with the storing and removal of data?)

<a name="form_masking"></a>
#### Form masking

This allows you to set 'surfly_private' on forms which may have sensitive data, such as payment details.
Surfly will not synchronise the content of the field to the followers.

<a name="customizing_surfly"></a>
### Customizing Surfly

Depending on who is in control, certain buttons can be disabled.

This is specified in the session integration options, where it is possible to add:
 - 'agent_can_end_session', which, if activated, lets the 'end session' button appear on the users end.  

Only the leader of the session can change the drawing function, the followers cannot.
