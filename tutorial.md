# The Surfly Tutorial

### Introduction

###### Welcome to Surfly!

Surfly enables you to integrate our co-browsing technology fully into your own website. The appearance of the co-browsing session can be fully customised to allow for a seamless addition to 
your website. Surfly is easy to set up, as only requires a small addition to your websites' source code. Small changes within this code snippet allow you to adapt Surfly to your needs.

###### What is a Surfly session?

A Surfly session allows you to share your browser with others. Typically, a vistor to your website will request a session and be queue'd until an agent joins them. The passive member of the 
session is referred to as the follower, and the active member is the leader.  The leader will navigate the site, and the follower can help guide them through it. Initially the agent is the 
follower, and the website visitor is the leader, however you can choose to swap control during the session. 

Communication within the session can be done via text or video chat, and followers may highlight areas they wish to draw attention to with the drawing functionality. You may also share documents 
and invite others to join your session by sharing the session url or sending an email. Each session has its own ID, which has been formatted to be easily communicated over the phone.   


###### Taking a session

The sessions can be managed via Surfly's admin panel. To take a session, navigate to the Queue panel. Here, agents can see how many users they have queue'd up, their location, and the time 
they have been waiting. To take a session, the agent simply presses the "take call" button. If your visitors are logged in on your website already, you can also show their name in the queue, 
so that the agent greeting them knows who they are.

![The Queue panel](https://raw.github.com/surfly/tutorial/master/screens/queue_panel.png)

The tutorial covers:

 - [Session Modification](#session_modification)
 - [Add Surfly to your website](#add_surfly)
 - [Advanced options](#advanced_options)
 - [Example use cases](#examples)

<a name="session_modification"></a>
### Session Modification

You can adapt the way a session starts, looks and behaves by changing the default settings to meet your needs.

The main points covered in the session modification section are: 

 - [Changing the chat box](#chat_box)
 - [Video chat](#video_chat)
 - [Switching the control options](#switch_control)
 - [The window size options](#window_size)
 - [The drawing mode](#drawing_mode)
 - [Ending a session to display another page, or redirect to another page](#popupurl)

<a name="chat_box"></a>
####Chat box

Modifying the chat box can not only change its appearance, but also limit or extend the amount of control that the leader and the follower 
can have. You can also choose to remove the chat box functionality entirely, and display an icon panel instead.

###### Changing the chatbox color

The default chatbox color is a soft red, however, this can also be altered to match your websites theme. As can be seen in the image below, 
we changed the icons at the top of the Chatbox from a light red to a deep blue, which is more suited to our example website:

![Changed chatbox colors](https://raw.github.com/surfly/tutorial/master/screens/changed_chatbox_colour.png)

###### The agent cannot end the session

You may wish to disable the ability for the agent to end a session, preferring to allow the visitor full control over the session durations.
This is a simple change, and removes the exit icon from the agents chatbox.

![agent cannot exit](https://raw.github.com/surfly/tutorial/master/screens/agent_cannot_end.png)

###### Docked only

It is also possible to remove the video and text chat functionality, if you wish. Only the panel containing the different icons will be visable:

![docked_only](https://raw.github.com/surfly/tutorial/master/screens/docked_only.png)

You can also change the position of the dock from the bottom left of your screen to the top of your screen.

###### Storing the chat logs

If you want to monitor the conversations between the agents and the user, you can store the chat logs.  

After the session has ended, you can go to your dashboard and click on history. The chat log will have two icons inside, allowing you to either view the 
logs, or download them.  

![chatlogs](https://raw.github.com/surfly/tutorial/master/screens/logged_icon.png)

<a name="video_chat"></a>
#### Video chat

Surfly also allows you to have a video chat option. However, if you do not want to use it, it can be easily disabled. You can also set the video to be full screen, or
restrict the quality.

<a name="switch_control"></a>
####Switching the control from leader to follower

If you want to be able to switch the controls between the leader and the follower, you can chose between either allowing the agent to take control, or to 
request it from the leader. This could be useful for when users require further guidance through the website.

![request control](https://raw.github.com/surfly/tutorial/master/screens/agent_request.png)

As can be seen in the above image, the hand button is now bold, which means the agent can now use it to take, or request, control.  


<a name="window_size"></a>
#### Window Size options

You can specify either the maximum or minimum size you want the window to be. The window is normally set to the person with the smallest screen, 
as this allows for a smooth transition into the Surfly session.  However, if required, this can also be removed.

<a name="drawing_mode"></a>
#### Options for the drawing mode

The drawing option allows the followers within the Surfly session to highlight the areas on the screen that they wish to draw attention to. The 
drawing defaults are that the mode is temporary and the color is yellow, however both of these can be changed.

In our example website we adapted the code in order so that the drawing mode would be permanent, and that the color of the drawings would be 
a vibrant green:

The green drawings underscoring the button are clearly visable to the leader of the session:

![changed drawing color](https://raw.github.com/surfly/tutorial/master/screens/drawing.png)

<a name="popupurl"></a>
#### Exiting the session display or redirect to another page

You may want to show a user another page after the session has finished. You can either show a popup window within the page you want to display, or you can 
redirect them to another url.

In the example below, we have chosen to show the leader a popup url within their screen after the session has finished.  
The user can exit the popup window by clicking on the cross to the top right of the window.

![Popup url](https://raw.github.com/surfly/tutorial/master/screens/popup_example.png)


<a name="add_surfly"></a>
### Add Surfly to your website


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
Auto start is especially useful if you want to display a certain webpage whilst the visitor is waiting for an agent to join them.

<a name="surflystart_anchor"></a>
#### Customise your own button

If you want to create your own button, you can use the #surflystart anchor, which can be integrated into your websites source code.  The button can be fully
styled so that it compliments your website design.  In the example website below, you can see the blue button below will lead you to a Surfly session. You can
also specify the text on the button.

![The end result](https://raw.github.com/surfly/tutorial/master/screens/Surflystart_anchor.png)

<a name="stealth_mode"></a>
#### Start a session in stealth mode

If you do not wish to have a visual button or link on your webpage, then you can use stealth mode.  This allows vistors to initiate a Surfly session simply 
by pressing CTRL+ENTER.

<a name="button_appearance"></a>
#### Button Appearance

If you prefer, you can also adapt the default "get live help" button that Surfly provides. The buttons default appearance is red, with white text and sits to the bottom left of the screen. 
The position of the button can be moved to either the bottom right of the screen, or to the middle left. You can further adapt the button to suit your needs by specifying the color of the 
button along with the font size and font color.

As you can see below, in the example website, we changed the position and the style of the button.  The default color of the button was changed to black, which suits the theme 
of our example  website. The font color remains white, but the size of the font has increased to size 16, which also increases the size of the support button.

![example website with adapted Surfly button](https://raw.github.com/surfly/tutorial/master/screens/adapted_surfly_button.png)

#### The session ID approach

The session ID approach enables a small, discrete icon to be added to your website.

#### Integrate with existing chat solutions

#### Create your own invite page

<a name="advanced_options"></a>
### Advanced options

This section covers:

 - [Session continuation](#sessuion_continuation)
 - [Adding custom metadata to queue requests](#custom_metadata)
 - [Field masking](#field_masking)
 - [Blacklist and Whitelist](#blacklist_whitelist)

<a name="session_continuation"></a>
#### Session continuation

Please Note: This is only supported for sessions started with the Surfly widget.

Cookies can be carried over from your website, and into the Surfly session. For example, if a user is logged into your website, they will remain logged in for the duration of the 
session. Once the session has finshed, the information is returned back to the website. This allows a smooth transition into, and out of, the session.

There are two main ways to set up session continuation:
 - Full session continuation allows the transfer of all data, including (unlike soft session continuation), cookies with a HttpOnly tag. 
 - Soft session continuation allows the transfer of cookies from the current page, excluding cookies with a HttpOnly tag.


<a name="custom_metadata"></a>
#### Add custom metadata to Queue request

If a user has logged into your website, you could pass information on to the agent, such as name and address. Surfly will also use the name in order to display this in the chatbox, 
and the email in order to match the correct gravitar to the user.

<a name="field_masking"></a>
#### Field masking

You may want to protect your users data during the Surfly session. Field masking allows you to hide sensitive information, such as payment details, from the session followers.

<a name="blacklist_whitelist"></a>
#### Blacklisting and Whitelisting

Please note: This option is only available to enterprise clients.

Blacklisting is used in order to deny users access from a select few pages, If you want more control over what your users can access, whitelisting may be the most viable option.
Whitelisting allows access only to the pages specified in the code snippet.

If the redirect url is not specified, the user will be redirected to Surfly's default page.


<a name="examples"></a>
### Examples use cases
