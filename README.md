# AOModalStatusView

Create an AO Modal Status View for light actions in iOS Apps.

AO Modal Status View is a framework created to recreate Apple's private Modal Status View. 

While designing iOS apps we may want to alert the user to a successful completion of a task.
Many different methods have arrived to do just this, from a subtle drop down notification covering the status bar to a more interfering UIAlertView.

Apple's solution is to display a self-removing and small modal view to the screen.

![alt text](https://user-images.githubusercontent.com/20458718/31577957-33ec53ce-b0dd-11e7-8b50-0031889040fd.PNG "Apple's custom use of Modal Status Views")

With uses in the News app, the Apple Music app, and the Podcasts app, developers have been wanting access to this view for a while now. 
That is what this framework solves.

## Design

![minipic](https://user-images.githubusercontent.com/20458718/31578023-a6b69166-b0de-11e7-8446-7ef0d22da452.png "AOModalStatusView Design and Implementation")
![minipic](https://user-images.githubusercontent.com/20458718/31578226-7cd123b2-b0e2-11e7-8f46-0b00cc8ad865.gif "AOModalStatusView Animation Gif (not jif)")

<style>
img[alt="minipic"] { 
  max-width: 250px; 
  display: block;
}
</style>

The animation lasts two seconds, but I had trouble getting the gif to perform at the correct speed.

## Instructions

Simply import the framework and add the following code to get started.

    let modalView = AOModalStatusView(frame: self.view.bounds)
    view.addSubview(modalView)

Further customize the AOModalStatusView with the following functions:

    modalView.set(image: downloadImage)
    modalView.set(headline: "Downloaded")
    modalView.set(subheading: "The photo was successfully saved to your library")

## Features

### Animations

The AOModalStatusView will appear and disappear with a fast fading and scaling effect to match Apple's implementation.

### Timer

The AOModalStatusView will only appear for a couple seconds so as not to interfere with the UX of your app.

### Style

The AOModalStatusView is designed to match the style and aesthetics of Apple's implementation.

This includes slightly rounded corners,
a blurred visual effects view as the background,
heading and subheading options in addition to an image,
and placement in the center of the view. 
The animations were designed to match Apple's original design.

