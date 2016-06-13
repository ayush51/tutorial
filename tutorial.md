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

When you open your webpage, you should see a button at the bottom left of your screen, inviting you to ask for live help.
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

If you enable auto start, it means the webpage including the code snippet will immediatly start a Surfly session. The page will display a red banner asking the 
visitor to wait for an agent to join their session, and the queue pin number.  

To enable this feature, set auto_start to true in the Surfly code snippet.

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

As stealth mode is already the default in the Surfly code snippet, to disallow it, simply set stealth mode to false:

 ```stealth_mode:"false"``` 


<a name="button_appearance"></a>
### Button Appearance

The Surfly button can be completley adapted in order for it to fully integrate into your own website and its design.

Its default appearance is red, with white text and sits to the bottom left of the screen.

The position of the button can be moved to either to the bottom right of the screen, or to the middle left. 
Your preference can be added to the code snippet, for example:

```javascript 
  position:"middleright"
```

You can further adapt the button to suit your needs by specifying the color of the button along with the font size and font color, e.g:

```javascript
    theme_font_background:"#000000",
    theme_font_color:"#ffffff",
    theme_font_size:"16",
```  
Our example code changes the color of the button to black, which suits the theme of the tutorial's website.  The font color remains white, but the size of the 
font has increased to size 16, which also increases the size of the support button. 

![example website with adapted Surfly button](https://raw.github.com/surfly/tutorial/master/screens/adapted_surfly_button.png)

Please Note: 
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



###### The default chat box settings:

 - The icons within the chat box are a soft red color.
 - The default settings for the agent:
   - Can see how many people are in the session
   - Can exit the session
   - Can maximise/ minimise the chat box window
   - Start videochat
   - Share documents

![default for follower](https://raw.github.com/surfly/tutorial/master/screens/default_for_agent.png)

 - The default settings for the leader:
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

You can change the chatbox color in the Surfly code snippet by specifying the chat_box_color parameter and giving it the css string you want to change the
default to.  

```javascript 

chat_box_color:"#80ffbf"
```

As can be seen in the image below, the icons at the top of the Chatbox have been changed from a light red to a deep blue, which is more suited to our website's theme:

![Changed chatbox colours](https://raw.github.com/surfly/tutorial/master/screens/changed_chatbox_colour.png)

###### The agent cannot end the session

You can also change the amount of control the members of the session can have, by adding or removing icons.  For instance, if you do not want to allow the agent to 
be able to end the session, you can specify this in the code snippet:

```javascript
agent_can_end_session:"false",
```

This will remove the exit icon from the agents chatbox:

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

As can be seen in the above image, the hand button is now bold, which means the agent can now use it to take, or request, control.  


<a name="window_size"></a>
#### Window Size options

The window size can also be adjusted to suit your needs by adjusting the min/ max parameters.  

For example, this would set the window size to be larger than 200x200:

```
min_height: "200",
min_width: "200",
```

The window is normally set to the person with the smallest screen, as this allows for a smooth transition into the Surfly session.
However, if required, this can also be removed:    

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

You may want to show a user another page after the session has finished.  You can either show a popup window within the page you want to display, or you can 
redirect them to another url.  

###### Show a popup window

If you want to end the session and show the user a popup window, you can set the end_of_session_popup_url in the code snippet to point to the url of that page.
After the session ends, the window will be loaded on the users page.

```
end_of_session_popup_url:"your_url_here"
```

The user can exit the popup window by clicking on the cross to the top right of the window.

![Popup url](https://raw.github.com/surfly/tutorial/master/screens/popup_example.png)

###### Redirect the user to another url

You can either redirect the leader or the follower to another url after the session has finished.
 
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

Cookies can be carried over from your website, and into the Surfly session.  Once the session has finshed, the information is returned back to the website.
This allows a smooth transition into, and out of, the session.  


There are two main ways to set up session continuation:
 - [Full session continuation](#full_session)
 - [Soft session continuation](#soft_session)

<a name="full_session"></a>
#### Full session continuation

Full session continuation allows the transfer of all data, including (unlike soft session continuation), cookies with a HttpOnly tag.
This requires a change in the host websites' load balancer configuration alongside a small change to the code snippet.

The changes that need to be made in the code snippet are:

```javascript
  cookie_transfer_enabled: true,
  cookie_transfer_proxying: true,
  cookie_transfer_urls: ["https://your_website_name.com/surfly_cookie_transfer/"]
```

To adapt the load balancer configuration you need to set the following request headers in the host website's config file:

 - X-Widget-Key: your_widget_key
 - X-continuation-origin: https://the_origin_page_with_Surfly_Widget.com
 - Host: surfly.com

The X-Widget-Key is the widget key from your code snippet, and the X-Continuation-Origin is the origin page containing the Surfly widget. 
You may also need to specify the port, if it is non-standard.  

###### Please Note:
The API has further details, and includes examples on how to set up full session continuation in Haproxy and Nginx

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

 - [Blacklisting or Whitelisting](#blacklist)
 - [Auditlog](#auditlog)
 - [Form masking](#form_masking)


<a name="blacklist_whitelist"></a>
#### Blacklisting and Whitelisting  

Please note: This option is only available to enterprise clients. 

Blacklisting is used in order to deny users access from a select few pages,  If you want more control over what your users can access, whitelisting may be the most viable option.  
Whitelisting allows access only to the pages specified in the code snippet.  

Both the blacklist and whitelist variables are in the format of a JSON array, and can take the following parameters:
 - pattern: A regular expression matching restricted url (in the case of blacklist), or the allowed url (in the case of whitelist)
 - redirect: An url you wish to redirect the user to after they have attempted to access a restricted page (optional)
 - type: The restriction type. (optional)

If the redirect url is not specified, the user will be redirected to Surfly's default page.

For example:

```
{
   "pattern": ".*your_website\\.com*",
} 

```

would allow (whitelist) or restrict (blacklist) access to your_website.com. If the user attempted to access a restricted page then, in this case, they would see
the Surfly default page as a redirect url has not been provided.   


