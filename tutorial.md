
# Introducing Surfly

### Welcome to Surfly

###### What is co-browsing?

Surfly's co-browsing technology enables you to share your browser with others, synchronising mouse clicks and key events. You can start a Surfly session simply by entering the url of the website you want to browse into the 'start session' panel on your admin page. Then, invite people to join you by sharing the session url with them. This is the easiest and quickest way to co-browse and does not require any configuration. However, if you wish to use Surfly as a feature on your own website, you can also add a Surfly button to your website. By doing this, you will be able to fully customise your session and use as much, or as little, of Surfly's functionality within your own product.

The introduction gives an overview of what Surfly is, and outlines the various ways in which it can be integrated and adapted for your own needs. More information on how to make these changes can be found in the Surfly tutorial and in the API documentation.


###### During the session

During the session, the mouse arrows from all users will be visible. The leader will navigate the site, and the follower can help guide them through it. There can only be one leader, but you can have multiple followers, and switch control between the different users during the session. Only the leader can select or click items on the page, and if the leader decides to navigate to another url, the followers' screens will be synchronised so that they can also see this new page. The followers can take advantage of the drawing tool provided in order to highlight areas on the screen. During the session, users can communicate via text or video chat, share documents and invite others to join them.

###### Responding to incoming requests

To accept an incoming request, log in to your Surfly account, and navigate to the 'Queue' panel. Here, agents can see how many users they have queue'd up, their location, and the time they have been waiting. To answer, the agent simply has to press the 'take call' button. If your visitors are logged in on your website already, you can also display metadata, such as the visitor's name in the queue, so that the agent greeting them knows who they are.

![The Queue panel](https://raw.github.com/surfly/tutorial/master/screens/queue_panel.png)

###### The Admin panel

Surfly's admin panel allows you to track your users and your agents, and can be customised to suit your needs.

The buttons on the admin panel are:

 - The 'start' button, this allows you to immediatly start co-browsing.  When you click on this link you are asked to invite someone to join your session, by either sending them the session url directly, or via email.
 - The 'queue' button, which gives you a list of queue'd users.  You can add metadata to this panel so that the agent knows more information about the user.
 - The 'history' button gives a brief overview of your session. You can also choose to record the chat logs which will then be accessible from the history panel.
 - The 'agent' button allows you to add agents to your account, and also gives you access to some information about agents such as their ID and the amount of sessions they have joined.
 - The 'settings' button lets you change your profile settings, and also includes your account details. Here, you can review your account plan, billing and personal information. The settings button also contains your integration information, the Surfly code snippet and the REST API key. 
 - The 'log out' button lets you exit the admin panel.


<a name="session_modification"></a>
### A Surfly session

Surfly comes with several different options for communicating with other users. You may decide to video or text chat, share documents and highlight areas with the tool. 
If Surfly is integrated into your website, you can adapt the way a session starts, looks and behaves by changing the default settings. 

The main points covered in this section are: 

 - [Inviting users to join your session](#invite_user)
 - [Navigating to a new website](#invite_user)
 - [Chat box](#chat_box)
 - [Video chat](#video_chat)
 - [Document sharing](#document_sharing)
 - [Window size options](#window_size)
 - [Drawing mode](#drawing_mode)
 - [Control switching](#customise_control_switching)
 - [Adding metadata to the queue](#metadata)
 - [Ending the session display or redirect to another page](#popupurl)

<a name="invite_user"></a>
#### Inviting users to join your session

You can invite a user to join your session from your Surfly admin panel or from within a Surfly session: 
 - To start a session from the Surfly admin panel, navigate to the "start" button at the top left of your screen. 
 - Within the Surfly session the leader can, by default, invite people by clicking on the "add user" icon in the dock.

Both of these methods will load the following screen:

![invite_user](https://raw.github.com/surfly/tutorial/master/screens/invite_user.png)

You can then decide to either share the url of the session, or send an email to the users you wish to invite. During a session, there is always one leader at any given time, but there can be multiple followers.

<a name="new_url"></a>
#### Navigating to a new website 

At any given time during a Surfly session, the leader can decide to surf to another website within the co-browsing session. In order to do so, you can use the "navigate to new url" button in the chat box. You will then see the following screen asking you to enter the new url:

![new_url](https://raw.github.com/surfly/tutorial/master/screens/new_url.png)

However, if you wish to open a new tab you can simply hold Ctrl and click on the link you want to open. When the last tab has been closed, the normal Surfly session will resume.

Please note: the standard Ctrl + T shortcut to open a new tab will not open a tab within the Surfly session

<a name="chat_box"></a>
####Chat box

Surfly provides a chat box which can be used to communicate with other users. 
The default chatbox color is a soft red, however, this can be altered to match your website's theme. Modifying the chat box can not only change its appearance, but also limit or extend the amount of control that the leader and the followers can have. 

If you want to monitor the conversations between the agents and the users, you can choose to store the chat logs. You can access them by navigating to 'History' in your Surfly admin panel. The chat log section will have two icons inside, allowing you to either view the logs, or download them.

![chatlogs](https://raw.github.com/surfly/tutorial/master/screens/logged_icon.png)

If you do not want to have the chat functionality, you can either have just the dock, displaying the control panel, or remove it completely.

<a name="video_chat"></a>
#### Video chat

Surfly also allows you to communicate in your session with video chat. You can maximise the video to full screen, or restrict the video quality. However, if you do not wish to use this functionality you can easily disable it.

<a name="document_sharing"></a>
#### Document sharing 

If you wish to share documents during the Surfly session, you can click the paper icon to the bottom right of the chat box. Once you have clicked on it, you can upload a document from your desktop. By default, shared documents can only be viewed, and not downloaded. However, you can change the settings so that the files can be downloaded. It is also possible to share documents by dragging them directly to the chat box. 
If you wish, you may also disable the document sharing tool. 

<a name="window_size"></a>
#### Window size options

The size of the window is normally set to the person with the smallest screen, as this allows for a smooth transition into the Surfly session. If you see blank edges at the side of your screen, it is only because your screen is larger than the person you are co-browsing with. However, you can also decide to set a maximum or minimum size for the window.
Alternatively, you may decide to remove the set to smallest screen functionality altogether. In this case, the window will be set to the size of the leader's screen.

<a name="drawing_mode"></a>
#### Drawing mode

The drawing option allows the followers within the Surfly session to highlight the areas on the screen that they wish to bring attention to. It works in a similar way to a highlighter, or a magic marker. By default, the drawings are temporary (they will fade out) and the color of the drawing tool is set to yellow. Of course, if you would prefer to have something different, both of these parameters can be changed, or you can turn the drawing function off entirely. You can also set the pixel size and the timeout length. 

In our example website we adapted the code so that the drawing mode would be permanent, and that the color of the drawings would be in our blue theme color. 

![changed drawing color](https://raw.github.com/surfly/tutorial/master/screens/drawing.png)

<a name="customise_control_switching"></a>
#### Control switching

If you want to be able to switch control between the leader and the follower, you can choose between either allowing the agent to take control, or to
request it from the leader. This could be useful for when users require further guidance through the website.


<a name="metadata"></a>
#### Adding metadata to the queue

When a user is being queue'd, you may want to pass some information to the agents, allowing them to know a bit more about the clients, or to identify a specific client. For instance, if a user has logged in to your site, you could pass some of that information to the agent. As shown in the image, the information is added to the 'meta data' section in the queue panel.


![queue metadata](https://raw.github.com/surfly/tutorial/master/screens/queue_metadata.png)

<a name="popupurl"></a>
#### Exiting the session display or redirect to another page

You may want to show a user another page after the session has finished. In this case, you can either show a popup window within the host website, or you can send them to another webpage.

In the example below, we have chosen to show the leader a popup url within their screen after the session has finished.
The user can exit the popup window by clicking on the cross to the top right of the window.

![Popup url](https://raw.github.com/surfly/tutorial/master/screens/popup-cake.png)

This can be especially useful if you wish to receive feedback by asking your visitors to fill out a survey when the session ends.

<a name="add_surfly"></a>
### Integration

If you integrate Surfly with your website, visitors will be able to click the 'get live help' button to request a session. They will then be queue'd until an agent (the person who receives the call) joins them. By default, the person who initiated the session is the leader and the agent who takes the call will be the follower, however you can choose to swap control at any time during the session.

To integrate Surfly, you need to add the Surfly code snippet into your website's source code. The default parameters within the code snippet can be modified to allow for a seamless integration into your website. The code snippet will allow you to customise the way the session looks and behaves, if you wish a deeper integration, you can use the REST API, which gives you control over the backend.

Please see the tutorial for a detailed step by step guide on how to integrate Surfly into your website.

#### The Surfly Code Snippet

This can be found by clicking on the 'integration' panel in your account settings.
If you get a message telling you that you do not have the API key set up yet, click on 'Generate API'.

You should now be looking at:

![The integration page](https://raw.github.com/surfly/tutorial/master/screens/snippet_initial_screen.png)

In the 'domain names' section on the integration page, you need to specify the domain of your website. For instance, if your website is hosted on "https://example.com", simply add "example.com" to the domain name list.

Finally, copy the code snippet and add it to the source code of your website.

When you open your webpage, you should see a 'get live help' button at the bottom left of your screen. If a visitor clicks on this, they will be queue'd for support. You can answer this request via the Surfly admin panel.

**Please see the tutorial for a detailed step by step guide on how to integrate Surfly into your website.**

<a name="start_session"></a>
### Starting a session

 - [Button appearance](#button_appearance)
 - [Stealth mode](#stealth_mode)
 - [Customise your own button](#surflystart_anchor)
 - [Session ID](#session_id)
 - [Create an invite page](#auto_start)
 - [Integrate with existing chat solutions](#integrate_chat)

<a name="button_appearance"></a>
#### Button appearance

If you prefer, you can adapt the 'get live help' button that Surfly provides. The button's default appearance is red, with white text and sits to the bottom left of the screen. 

![default button appearance](https://raw.github.com/surfly/tutorial/master/screens/default-button.png)

You can adapt the button appearance by changing its position, colors and size. 

The button, by default, will only be shown if an agent is logged into the Surfly admin page. This can also be disabled, if you wish.

<a name="stealth_mode"></a>
#### Start a session in stealth mode

If you do not wish to have a visual button or link on your webpage, then you can use stealth mode. This allows visitors to initiate a Surfly session simply by pressing CTRL+ENTER.  The visitor will then be queue'd, and the Surfly session will start as usual.

<a name="surflystart_anchor"></a>
#### Customise your own button

If you want to create your own button, you can use the #surflystart anchor, which can be integrated into your website's source code. You can choose the text you wish to write onto the button, and it can be fully styled with css so that it compliments your website design.  As you can see in the image below, we chose to use the image of a cake as a button. If a visitor to the website clicks on it, it will lead them to a Surfly session.

![The end result](https://raw.github.com/surfly/tutorial/master/screens/cake-button.png)

<a name="session_id"></a>
#### The session ID approach

The session ID approach is especially useful if you are already in contact with a customer via the phone. If the customer needs help navigating a website, the agent can direct them to start a co-browsing session. 
You can use the REST API to access the session ID and display it. The user can then communicate this ID to the agent so that they will be able to join the session and help them.

Once the agent has the session ID, they can simply enter it into the start session panel on the Surfly admin page, and will immediately join the session.

![Start Surfly](https://raw.github.com/surfly/tutorial/master/screens/enter_session_id.png)

<a name="auto_start"></a>
#### Create an invite page

Enabling auto_start in the code snippet means that the webpage will immediatly start a Surfly session. This option allows you to fully customise your invite page. The page will display the default red Surfly banner, letting the visitor know that they have been queue'd. 
The red banner may also be removed through a simple change to the code snippet. Just set the "block_until_agent_joins" parameter to "false".

Further customisation is also possible through the use of the REST API. For example, you can use it to detect whether a Surfly session has started or not, and alter your websites' appearance based on this. For instance, if we're in a Surfly session, we can get the unique queue code which identifies the user who initiated the session and display it.

As can be seen below, we were then able to set up our own invite page:

![Queue ID](https://raw.github.com/surfly/tutorial/master/screens/custom-lp.png)


<a name="integrate_chat"></a>
#### Integrate with existing chat solutions

It is also possible to integrate Surfly with existing chat solutions. For example, if you have already established your own video or text chat, you may want to add Surfly's co-browsing functionality to this. In this case, Surfly can be integrated in such a way so that it acts as a transparent addition to your product and allows you to entirely customise the appearance of the session.

Simply add the code snippet to the page including your chat solution, and alter it to either remove the user interface entirely, or to display a dock with session control options (more information on the docked_only option can be found here). You will then be able to use Surfly's co-browsing functionality in addition to your own chat solution.

<a name="integration_options"></a>
### Integration Options

This section covers:

 - [Surfly and third party cookies](#third_party_cookies)
 - [Session continuation](#session_continuation)
 - [Security Features](#security_features)
 - [Add information to a session log](#session_log_info)
 - [Customising the website appearance depending on who is in control](#customise_appearance_for_user)

<a name="third_party_cookies"></a>
#### Surfly and third party cookies

When integrating Surfly into your website, it is important to know that top level domains do not transfer third party cookies to the iframe, so instead you may choose to open a session in a new tab, or to use a CNAME.

<a name="session_continuation"></a>
#### Session continuation

Please note: This is only supported for sessions started with the Surfly widget.

Cookies can be carried over from your website, and into the Surfly session. For example, if a user is logged into your website, they will remain logged in for the duration of the session. Once the session has finished, the information is sent back to the website. This allows a smooth transition into, and out of, the session.

There are two main ways to set up session continuation:

 - Full session continuation allows the transfer of all data, including (unlike soft session continuation), cookies with a HttpOnly tag.
 - Soft session continuation is more limited, and excludes cookies with a HttpOnly tag.

<a name="security_features"></a>
#### Security Features

Surfly's security features allow you the option to protect users' data during the session, and, if required, restrict access to selected webpages. 

 - [Field masking](#field_masking)
 - [Blacklisting and Whitelisting](#blacklist_whitelist)

<a name="field_masking"></a>
##### Field masking

Field masking allows you to protect the leader's data during the Surfly session. If the user is required to enter sensitive information (such as payment details), into your website, you can hide that input from the session followers. The leader is still able to read what they are typing into the form, but the followers (including the agent) will only see a series of x's.

###### Please note: 

Whilst the leader can mask their data, and hide it from the followers, the followers cannot hide their data from the leader.

<a name="blacklist_whitelist"></a>
##### Blacklisting and Whitelisting

Blacklisting is used to ban users from a select few webpages, whereas whitelisting is more restrictive, and allows access only to the pages specified in the code snippet.

###### Please note: 
This option is only available to enterprise clients.

<a name="session_log_info"></a>
#### Add information to the session log

The surfly.log() function can be used to log custom messages during the Surfly session. You can use the REST API to track occurances of that message/ 

In our example website, we wanted to track the amount of times an agent had made a sale. Everytime the "buy" button is clicked, we create a Surfly log message indicating that the sale has been completed.  We matched the "Sale completed" message to the agent's id and counted the amount of times that this message had been logged using the REST API. A page could then be created showing the number of sales the agent has made.


<a name="customise_appearance_for_user"></a>
#### Customise website appearance depending on who is in control

Surfly sessions are always comprised of one leader, and one or more followers. The leader is the only person who can click or type during the session, but you can switch control between the leader and the followers, if required. You can specify the features you want to give to the leader and the followers during the session by enabling or disabling icons in the dock. Moreover, you can adapt the status of the elements of a page depending on who is in control. For example, you may want to make a button clickable only when the leader (the person who initiated the session) is in control.


