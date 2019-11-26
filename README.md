# floats-and-clearfix-example

A clearfix in CSS  is used to fix issues with content overflowing from a div when it or content close to it has been floated.
A clearfix requires 3 perimeters, display, content and clear.
Here is the code for a clearfix:
```css
.clearfix::after{
    */This sets the elements display property to block meaning that like a heading it will take up one line on the screen from
  edge to edge./*
    display: block;
    */The content property is empty as we do not want any text to be showing inside of this element.
      The empty sting is in place to make sure the element isn't "flat."/*
    content: "";
    */The clear property is used to make sure that the clearfix element will extend the full with of the page leaving no white 
      space./*
    clear: both;

}
```

As we can see a clearfix is at first glance a simple refrence to a clas. However, what makes this so special is that it
essentially creates another div directly under where it has been assigned hence the `::after` code.

To further clarify lets use an example:
Lets say we have a div with the class of wrapper to hold all of the main content of our webpage.
Inside of that div we have some text and an image.
Now we would like for that text to wrap arround our image or at the very least sit next to it, 
insted of having these page elements sit one on top of the other.
To do this we would start by floating the image left or right as we prefer, and setting the overflow property to auto.
In so doing we have now taken the photo in question out of the normal flow of the page,
and asked the browser to handle any overflow for us automatically. The issue is that the other elements of our page in this case
the text well respond in kind and be placed behind our image, and our image will still spill out of the wrapper. 
This is not what we want.
To fix the issue we can use a clearfix. To start lets add a class of clearfix to the wrapper div.
Once we have done this, we will need to add the clear fix to our CSS as above.
Once this is done a new invisable element will be created at the bottom of the wrapper div to allow our content to fit correctly
and no longer "overflow" from the wrapper div.

#### Download the repo's files and open index.html for a working example.
