# UIKit

![Chewie](http://i.imgur.com/lfLcgZ2.png?1)  

> Rrrrrrr-ghghghghgh! ~[Chewbacca](https://en.wikipedia.org/wiki/Chewbacca)

## Learning Objectives

* Explain the role of UIKit in the development of iOS programs
* Describe the major UI controls that are included as a part of UIKit

## UIKit

iOS includes a framework called _UIKit_. UIKit provides you with a standard set of widgets, referred to as _elements_ or _controls_, that you can use in your app's views to provide a way for your users to interact with your app.

## UI Controls

So far, you have been introduced to a few user interface elements, including basic views, labels, and buttons. In this lesson, you'll get a quick overview of some of the other interesting user interface elements that you can use in your iOS apps.

To begin this investigation, create a new iOS project in Xcode. You can use the single-view application template provided with Xcode. (There is also a sample application included in this repository. It's located at `UIElements/UIElements.xcodeproj`. But you should start your own project so you can get a feel for these elements yourself.)

### Labels

_Labels_, also known as `UILabel`s, are the most basic way to display strings of text in your app. You've already seen a few labels in your previous lessons, and should be pretty comfortable with them by now. Just for old time's sake, go ahead and drag a label onto your app's main view. You can find it in the object library in the bottom right corner of Xcode's main window. (You _do_ remember where that is and how to filter for labels, right?) Drop it in the top left corner of the application, so it looks like this:

![UILabel](http://i.imgur.com/JzkVqyN.png)

Labels are pretty simple, but they're used a lot in iOS apps. Remember that they're often referred to as `UILabel`s, since the class that describes them is called `UILabel`.

You've seen these a lot before (and will see them even more in the future), so let's keep moving.

### Buttons

_Buttons_ are the fundamental way for your users to interact with your application. Like buttons in real life, users can press them, and your app can do things in response to those presses. You've seen this in action in the previous lesson about IB actions. Go ahead and drag a button from the object library. Position it just below the label you created, so your interface looks like this:

![UIButton](http://i.imgur.com/st2u7ef.png)

Buttons are a bit more interesting than labels because the user can press them, and your app can do things in response to those presses (whereas labels are just static pieces of text that the user can't interact with). Buttons are often called `UIButton`s after their class.

### Segmented Controls

Here's a UI element you haven't seen in previous lessons: the _segmented control_. A segmented control is actually several buttons that are placed together as one unit. The user can press the control and select one—and only one—of the buttons at a time. They can be useful as a way to present mutually-exclusive choices to a user. For instance, you could use them to present sorting options for a table of data to the user.

Try adding a segmented control to your main view. Remember, you can search for "segmented control" in the object library:

![Segmented control in the object library](http://i.imgur.com/ltXCjLG.png)

Did you find it? When you do, drag it to your main view and put it under your button, so your interface looks like this:

![Segmented controls](http://i.imgur.com/AIBGa5b.png)

Segmented controls aren't as commonly used as buttons and labels, but they can be very useful. In future lessons, you'll see how they can be used to control views and other elements of the user interface.

### Text Fields

A _text field_ allows users to type text into your application. They are very useful for getting free-form text from the user. Your application can then grab that text and do something interesting or userful with it.

Find a text field in the object library and drag it to your main view. (Make sure you don't add a _text view_ instead!) Put it under your segmented control, so your UI looks like this:

![Text fields](http://i.imgur.com/i2sbpCf.png)

In future lessons, you'll see how you can grab the text the user entered in the text field and use it within your app's code. They're not the most interesting UI control, but they are very useful and commonly used.

### Sliders

iOS apps often have sliders, too. Here's what they look like:

![Sliders](https://upload.wikimedia.org/wikipedia/commons/d/d2/A_party_tray_of_sliders_at_a_restaurant.jpg)

Just kidding. We're not talking about the little hamburgers you get from White Castle. A _slider_ is a control that has a range of values that the user can _slide_ between. For example, you can use a slider to allow the user to set a duration, or perhaps change colors within a certain range. They look pretty cool, too. Drag a slider from the object library and position it under your text field, so your UI looks like this:

![Horizontal sliders](http://i.imgur.com/4Tt1ckZ.png)

This control might not seem terribly useful, but in future lessons you'll see just how handy it can be.

### Switches

A _switch_ lets the user select between two boolean values, generally either "on" or "off". You seem them a lot in app preferences, where a user can select whether an option is on or off, but they can be used other places than just preference panes as well. Add a switch to your user interface from the object library. Put it below the horizontal slider, so your UI looks like this:

![Switches](http://i.imgur.com/Pd9CXtr.png)

In a real app, you can wire up a switch to an IB action, so your app is notified when the user toggles the switch on and off.

### Progress Indicators

Sometimes your app is doing a task that takes a while to complete. It's nice to let your users know that your app is, in fact, doing something. You can indicate this activity using a _progress indicator_. A progress indicator is a bar that is filled as the task completes. When you create a progress indicator, you can change the max value, and then your app's code can change the progress indicator's value, so that the bar fills up as more work is done. Drag a progress indicator from the object library to your main view, below the slider you created:

![Progress indicators](http://i.imgur.com/iBnO1Ou.png)

Progress indicators are a very useful way to let your users know that your app is going to take a while to do something. In future lessons, you'll see how to use them effectively. They may seem like magic, but they're actually quite straightforward to use!

### Activity Indicators

Like progress indicators, _activity indicators_ are used to let your users know that your app is doing some work. The major difference between progress indicators and activity indicators is that activity indicators are _indeterminate_; that is, they don't display progress, they just let the user know that _something_ that can take a variable or unknown amount of time to complete is being done. For example, your app may have to contact a web service, but you have no idea how long that could take (the web service could even be down). You can display an activity indicator to let your user know you're contacting the web service, but because you don't know how long the request will take to complete, you can only show an indication that _something_ is happening.

Drag an activity indicator from the library and put it below your progress indicator:

![Progress indicators](http://i.imgur.com/7vKbmTR.png)

You've no doubt seen progress indicators many times when using iOS apps. They're rarely something a user _wants_ to see, but they at least let the user know that your app is busy doing something useful.

### Page Controls

A _page control_ is a weird little UI control. It allows users to see how many _pages_ into a view they are. Imagine you're writing a photo album application, and you can display nine photos at a time. Users may have any number of photos: 1, 10, 100, maybe even more. And they may be adding and deleting photos on a regular basis. You'll probably provide a way to swipe through those photos. A page control can be used to show how many pages of 9 photos per page the user has, so they can see how far they have to swipe to get to the middle or end of their photos.

Drag a page control from the object library and put it below the activity indicator you just created:

![Page controls](http://i.imgur.com/v0VJOB0.png)

It's a bit hard to see in this screenshot, but you can sort of see the two little square boxes that appear when it is selected. The thing about page controls is that they're not terribly userful until they're configured and attached to another view. They're very much a navigation element, and you won't see them that often, but occasionally they can be very useful.

### Steppers

A _stepper_ is a set of two buttons that allow a user to quickly increment or decrement a value. This value could be nearly anything. You could use it in an app that controls you home's thermostat, for example. Drag a stepper control from the object library to your view, placing it under the page control you created, like so:

![Steppers](http://i.imgur.com/dqdiWHE.png)

Much like the page control, steppers are generally used in conjunction with some kind of view, such as a label, that can show the value of the stepper. You'll see that in action in future lessons.

## Testing Out the UI

That's all the UI elements we're going to cover in this lesson, although there are plenty more that you'll be introduced to later on. For now, go ahead and build and run your application. Play with the elements you created a bit to see how you can interact with them. They won't do anything useful yet, but it's good to know what's provided by UIKit so you can make good use of these elements in your own apps.

![UI elements in action](http://i.imgur.com/9c9J9uW.png)

<a href='https://learn.co/lessons/uiElements' data-visibility='hidden'>View this lesson on Learn.co</a>
