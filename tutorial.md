# The Surfly Tutorial

### Introduction

###### Welcome to Surfly!

Surfly enables you to integrate our co-browsing technology fully into your own website. The appearance of the co-browsing session can be fully customised to allow for a seamless addition to 
your website. Surfly is easy to set up, as only requires a small addition to your websites' source code. You may also adapt the functionality of the session, by enabling the options you 
wish to include, or disabling those you wish to remove.  

###### What is a Surfly session?

A Surfly session allows you to share your browser with others. Typically, a vistor to your website will request a session and be queue'd until an agent (the person who receives the call)
joins them. The passive member of the session is referred to as the follower, and the active member is the leader.  The leader will navigate the site, and the follower can help guide them 
through it. Initially the agent is the follower, and the website visitor is the leader, however you can choose to swap control during the session. 

Communication within the session can be done via text or video chat, and followers may highlight areas they wish to draw attention to with the drawing functionality. You may also share documents 
and invite others to join your session by sharing the session url or sending an email. Each session has its own ID, which has been formatted to be easily communicated over the phone.   


###### Taking a session

To take a session, log in to your Surfly account, and navigate to the Queue panel. Here, agents can see how many users they have queue'd up, their location, and the time 
they have been waiting. To take a session, the agent simply presses the "take call" button. If your visitors are logged in on your website already, you can also display metadata, such as
the visitors name in the queue, so that the agent greeting them knows who they are.

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
 - [Document sharing](#document_sharing)
 - [The window size options](#window_size)
 - [The drawing mode](#drawing_mode)
 - [Ending a session to display another page, or redirect to another page](#popupurl)

<a name="chat_box"></a>
####Chat box

Modifying the chat box can not only change its appearance, but also limit or extend the amount of control that the leader and the follower 
can have. You can also choose to remove the chat box functionality entirely, and display only the icon panel instead.

###### Changing the chatbox color

The default chatbox color is a soft red, however, this can also be altered to match your websites theme. As can be seen in the image below, 
we changed the icons at the top of the Chatbox from a light red to purple, which is more suited to our example website:

| [![Default changed color](https://raw.github.com/surfly/tutorial/master/screens/red_default_chat.png)](Default chat color) | [![Changed chatbox colors](https://raw.github.com/surfly/tutorial/master/screens/changed_chatbox_colour.png)](chaged colr icons) |
|:---:|:---:|
| default chat box color | Changed chat box colors |

###### The agent cannot end the session

If you would like to allow your visitor full control over the session duration, you can chose to disable the exit icon from the agents dock. 
The agent can no longer see the exit icon, and the session will only end when the leader exits the session. 

![agent cannot exit](https://raw.github.com/surfly/tutorial/master/screens/agent_cannot_end.png)

###### Docked only

During a session you can choose to minimise the chat window, and display only the icons in a dock. It is also possible to fully disable the video and text chat so only the dock panel 
containing the icons will be available for the session. By deciding to use only the dock, you will also disable document sharing.


![docked_only](https://raw.github.com/surfly/tutorial/master/screens/docked_only.png)

You can also change the default position of the dock from the bottom left of your screen to the top of your screen.

###### Storing the chat logs

If you want to monitor the conversations between the agents and the user, you can choose to store the chat logs.  

After the session has ended, navigate to 'history' in your Surfly admin panel. The chat log section will have two icons inside, allowing you to either view the 
logs, or download them.  

![chatlogs](https://raw.github.com/surfly/tutorial/master/screens/logged_icon.png)

<a name="video_chat"></a>
#### Video chat

Surfly also allows you communicate in your session with video chat. You can also maximise the video to full screen, or
restrict the video quality. However, if you do not want to use it, it can be easily disabled.

<a name="document_sharing"></a>
#### Document sharing 

If you wish to share documents during the Surfly session, you can click the paper icon to the bottom right of the chat box.

![share documents](https://raw.github.com/surfly/tutorial/master/screens/share_document.png)

Once you have clicked on it, you can upload a document from your desktop. The default for document sharing is that they can only be viewed, and not downloaded. However, you can change the settings
so that the files can be downloaded. You may also disable the document sharing tool, if you wish. 

<a name="window_size"></a>
#### Window Size options

The window is normally set to the person with the smallest screen, as this allows for a smooth transition into the Surfly session. You can, however, decide to set a maximum 
or minimum size for the window.  Alternatively you may decide to remove it.

<a name="drawing_mode"></a>
#### Options for the drawing mode

The drawing option allows the followers within the Surfly session to highlight the areas on the screen that they wish to bring attention to. It works in a similar way to a highlighter, or 
a magic marker. The drawing function takes two parameters, drawing_mode and drawing_color.  The defaults are that the mode is temporary (so the drawings will fade out) and the color is 
initially set to yellow. Of course, if you would prefer to have something different, both of these parameters can be changed, or you can turn the drawing function off entirely. 

In our example website we adapted the code so that the drawing mode would be permanent, and that the color of the drawings would be 
a vibrant green:

The green drawings underscoring the button are clearly visable to the leader of the session:

![changed drawing color](https://raw.github.com/surfly/tutorial/master/screens/drawing.png)

<a name="popupurl"></a>
#### Exiting the session display or redirect to another page

You may want to show a user another page after the session has finished. You can either show a popup window within the host website, or you can 
send them to another webpage.

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
Auto start is especially useful if you want to display a certain webpage whilst the visitor is waiting for an agent to join them.  In our example webpage we have enabled autostart and
have customised the page so that the user is aware that they are in the queue.

![auto_start](https://raw.github.com/surfly/tutorial/master/screens/auto_start.png)

<a name="surflystart_anchor"></a>
#### Customise your own button

If you want to create your own button, you can use the #surflystart anchor, which can be integrated into your websites source code. The button can be fully
styled with css so that it compliments your website design.  In the example website below, you can see the blue button below will lead you to a Surfly session. You can
also specify the text on the button.

![The end result](https://raw.github.com/surfly/tutorial/master/screens/Surflystart_anchor.png)

<a name="stealth_mode"></a>
#### Start a session in stealth mode

If you do not wish to have a visual button or link on your webpage, then you can use stealth mode. This allows vistors to initiate a Surfly session simply 
by pressing CTRL+ENTER.  The vistor will then be queue'd, and the Surfly session will start as normal.

<a name="button_appearance"></a>
#### Button Appearance

If you prefer, you can also adapt the default "get live help" button that Surfly provides. The buttons default appearance is red, with white text and sits to the bottom left of the screen. 
The position of the button can be moved to either the bottom right of the screen, or to the middle left. You can further adapt the button to suit your needs by specifying the color of the 
button along with the font size and font color.

As you can see below, in the example website, we changed the position and the style of the button.  The default color of the button was changed to black, which suits the theme 
of our example  website. The font color remains white, but the size of the font has increased to size 16, which also increases the size of the support button.

![example website with adapted Surfly button](https://raw.github.com/surfly/tutorial/master/screens/adapted_surfly_button.png)

The button, by default, will only be shown if an agent is logged in to the Surfly admin page. This can also be disabled, if you wish.

#### The session ID approach

The session ID approach enables a small, discrete icon to be added to your website.  When a visitor clicks on this icon, they will start a Surfly session.

#### Integrate with existing chat solutions

#### Create your own invite page

<a name="advanced_options"></a>
### Advanced options

This section covers:

 - [Session continuation](#sessuion_continuation)
 - [Adding custom metadata to queue requests](#custom_metadata)
 - [Field masking](#field_masking)
 - [Blacklist and Whitelist](#blacklist_whitelist)
 - [Customise control switching](#customise_control_switching)
 - [The REST API](#rest_api)

<a name="session_continuation"></a>
#### Session continuation

Please Note: This is only supported for sessions started with the Surfly widget.

Cookies can be carried over from your website, and into the Surfly session. For example, if a user is logged into your website, they will remain logged in for the duration of the 
session. Once the session has finshed, the information is returned back to the website. This allows a smooth transition into, and out of, the session.

There are two main ways to set up session continuation:
 - Full session continuation allows the transfer of all data, including (unlike soft session continuation), cookies with a HttpOnly tag. This requires a change in the load balance configuration
   of the host website. 
 - Soft session continuation does not require a change in the load balance configuration, but is more limited.  A Surfly widget needs to be present on all pages you wish to transfer cookies from, 
   and excludes cookies with a HttpOnly tag.

<a name="custom_metadata"></a>
#### Add custom metadata to Queue request

Adding custom metadata to the Queue requests allows you to give extra information about the user to the agent. For example, if the user is logged in to your website, then you can pass on some 
of this data, such as name and address. Surfly will also use the name in order to display this in the chatbox, and the email in order to match the correct gravitar to the user.

<a name="field_masking"></a>
#### Field masking

You may want to protect your users data during the Surfly session. Field masking allows you to hide sensitive information, such as payment details, from the session followers.

<a name="blacklist_whitelist"></a>
#### Blacklisting and Whitelisting

Please note: This option is only available to enterprise clients.

Blacklisting is used in order to deny users access from a select few pages, If you want more control over what your users can access, whitelisting may be the most viable option.
Whitelisting allows access only to the pages specified in the code snippet.

If the redirect url is not specified, the user will be redirected to Surfly's default page.

<a name="customise_control_switching></a>
#### Customise control switching 

If you want to be able to switch control between the leader and the follower, you can chose between either allowing the agent to take control, or to
request it from the leader. This could be useful for when users require further guidance through the website.

![request control](https://raw.github.com/surfly/tutorial/master/screens/agent_request.png)

As can be seen in the above image, the hand button is now bold, which means the agent can now use it to take, or request, control.


<a name="rest_api"></a>
#### The REST API

The REST API allows you to tightly integrate Surfly into your website. You can delete, create, update and retrieve information on your agents, sessions and the incoming queue.
Using the REST API allows for a more programmatical approach towards integration.

<a name="reseller information"></a>
#### Resellers 

Resellers can create new Surfly clients, through the use of the REST API.  You may invoice the clients directly, or let Surfly do this for you. 
The REST API allows you to manage your clients by letting you create, delete, and get information about the client.

<a name="examples"></a>
### Examples use cases
