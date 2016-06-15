# tutorial

#### A list of the Markdown syntax used to format the tutorial to provide continuity for collaborators.

###### The headers:

 - Section titles, e.g Introduction, Add Surfly to the Website, Advanced Options ect. are h3 size, and are styled with
    three hashes. e.g ### Introduction
 - Subsections (for example, in Advanced Options, Session Continuation would be a subheading) are prefixed with four hashes,
    e.g #### Session continuation
 - If these subsections are further broken down into smaller sections, use five hashes. e.g in the chat box appearance section
   (which is a subsection of Modifications), titles are prefixed as so: ##### Changing the chat box color
 - The subheadings in the introduction are a special case, and are prefixed with six hashes, e.g ###### Welcome to Surfly

###### The images:

 - Images are uploaded to the screens (short for screenshots) folder 
 - To add an image to the text you need to provide the pathway to the raw image file in github. This is done as follows:
   
   `![Example Image Path](https://raw.github.com/surfly/tutorial/master/screens/example_image_path.png)`
   
   The first section in square brackets is the name of the image, and the pathway points to the place the image is saved. 
 - Adding images inline is similar to adding images, but with the table drawn in.
   
   `| [![First Example](https://raw.github.com/surfly/tutorial/master/screens/first_example.png)](First example) | 
     [![Second Example](https://raw.github.com/surfly/tutorial/master/screens/second_example.png)](second example) |
     |:---:|:---:| 
     | first example | second example |`
     
     *please note* this will add captions to the images

###### In text links

 - To add an in text link, provide the name of the link, and the text you want to make a link:
 
   `[Advanced Options](#advanced_options)`
   
   Would make the text Advanced Options into a link to a place in the text that carried the:
   
   `<a name="advanced_options"></a>`
   
   tag.  
   
