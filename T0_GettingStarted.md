# iOS Crash Course vol. 2

Greetings, intern. Time to earn your worth and learn a thing or two about life. This is in no way an easy task. Luckily, I am here to guide your way into glory. Well, into creating cool mobile apps on [The Best Mobile Platform To Date™](https://www.apple.com/ios/) at least. Everybody needs to start somewhere. For you, this series of task documents will be it.

# [Learning the ropes](https://i.redd.it/hysjuqc5cpd11.jpg)

## Finding your way around the [interwebs](https://thenextweb.com/wp-content/blogs.dir/1/files/2015/02/keyboard_surfing_the_internet2-406x450.jpg)
[Mac OS](https://www.apple.com/macos) is not the most popular operating system. But if you've had the fortune to use it before, just download your [favourite](https://www.mozilla.org/en-US/firefox/new/) browser and you can safely skip to the [next section](#getting-started). Otherwise, prepare to be bored.
To begin with, everybody nowadays has a personal preference for when it comes to web browsing. [The Browser](https://www.mozilla.org/en-US/firefox/new/) is the application you will use most of the day, every day, so it would make sense that you installed the one that is most preferable to you. In no way am I condemning the use of [Apple's abomination](https://www.apple.com/safari/), but if you are reading this, chances are you have not used it, so you cannot be accustomed to it, right? And that's a good thing because Mac OS's Safari is literally the new Internet Explorer. So, enough talk, go ahead and open it, hopefully for the first and the last time, and download your browser of choice. The most popular browsers are available for Mac OS, but if you'd like to build the latest nightly of a particular fork of Chromium, please do. [I am not one to judge](https://i.imgflip.com/1vcivr.jpg). Go to the webpage of your favourite browser and download it. It automatically goes to the `Downloads` folder (a neat stack-view icon next to the `Bin`) in the `Dock`. Install files for Mac OS are usually distributed in either `.dmg` or `.pkg` format. A `.dmg` is an image file, which Mac OS natively supports. Applications on Mac OS are actually a special type of directories called 'bundles'. They have a predefined structure and the OS knows how to locate the executable when you attempt to open them. When opening the `.dmg` file you are probably prompted to drag and drop the applicaton to the `Applications` directory of your system. It's an act of simple **copy-paste**. In fact, this is mostly to keep things organized, as you can actually run signed applications from any directory. But as we will discuss further in this document, one of the most important things is to be organized, so to the `Applications` folder it goes. :)

## Before you start digging in
Hopefully I do not need to tell you that being organized is crucial when it comes to project management. Usually when the dependencies start piling up it becomes increasingly harder to manage them have your project not been set up correctly in the very beginning. So please create a folder in your home directory named `Projects`, which should contain each and every project you ever create. If you will, you can create a `Github` folder inside of it, just to keep the projects you have cloned from github separated from the (more basic) ones you have created during this course. I have conveniently installed [Github Desktop](https://desktop.github.com/) on your machines, because it is the client we are most accustomed to using here. If you do not feel comfortable with using a UI client for git, you

1. Probably look like [this](https://i.ytimg.com/vi/KEkrWRHCDQU/maxresdefault.jpg)
2. Will have to find a way to show us your changes in a manner *[an ape](https://ca.slack-edge.com/T03UCVDN2-U0CAAV0KB-6fba434e73a7-512) is able to comprehend

## On a more serious note
When working for a [big company](https://www.nemetschek.bg/), security is always a concern. Our clients depend on us being responsible and keeping source code secure. This is why it's essential to never leave your PC unlocked when you are not at your desk. On Mac OS simply press `^` + `⌘` + `Q` (that is `ctrl` + `cmd` + `Q`) to lock your computer. Soon enough you will build a habit of doing this, but before that, you should be prepared to [bear the consequences](https://external-preview.redd.it/RhTABATlWxdc482qm0ElC7MX6h98XWeQUAVpqO8C68E.jpg?auto=webp&s=2a1c1ea41e53d35580546e4108a040a2b647a62c) of your forgetfulness.

## The end of this chapter
After all that said, it's time you got your adorable little hands dirty.

# Really getting started
First: some [dry](https://i.kym-cdn.com/photos/images/original/000/880/042/28a.jpg) theory. Read [this](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/launching/), [this](https://developer.apple.com/documentation/xcode/improving_your_app_s_performance?language=objc) and [this](https://developer.apple.com/documentation/uikit/app_and_environment/managing_your_app_s_life_cycle?language=objc) page of the programming guide.

Applications for iOS are built mainly using [MVC](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller). Read the documantation page for [UIViewController](https://developer.apple.com/documentation/uikit/uiviewcontroller?language=objc).

Due to the fact that Objective C has somewhat of a quirky syntax, reading [this](http://blog.teamtreehouse.com/the-beginners-guide-to-objective-c-methods) page is also highly recommended before getting your pretty hands dirty. ;)

# Baby's first project
*[aka this](https://pics.me.me/looks-like-its-time-to-oil-up-10217844.png)*

## Requiremets
Create an iOS application which greets the user by taking into consideration their name, gender (we assume there are only two for now) and whether the person [has an (un)healthy obsession with Japanese culture](http://www.dictionary.com/e/slang/weeaboo/). The application uses the corresponding prefix _"Mr/Ms"_ for *Normal* users and the suffixes _"-san/-chan"_ for *Weeaboo* users. Also, the greeting _"Konnichiwa"_ replaces the standard _"Hello_" for the latter. *Protip: you can refer to [this](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/Strings/Articles/FormatStrings.html) for a neat solution.*

## Creating the project
Open Xcode (which was conveniently installed for you :) and create a new project. Select **App** (make sure **iOS** is selected at the top left corner).
![alt text](/resources/T0/0.png "Create project")
Give it a nice name and choose **Objective-C** from the *Language* dropdown.
![alt text](/resources/T0/1.png "A nice name")
Navigate to the previously created `Projects` folder in your *Home* directory and select `Create`. You will be greeted with this:
![alt text](/resources/T0/2.png "Welcome to Xcode")

## Creating the UI
Make sure the `Project Navigator` is visible (press `⌘` + `1` if not) and select the `Main.storyboard`. Click the `+` button in the top right corner.
![alt text](/resources/T0/3.png "Add UI controls")
Now drag and drop five **Label**-s, a **Button**, a **Text Field** and two **Swtich**-es onto the view controller from the menu. Arrange them to look something like this:
![alt text](/resources/T0/4.png "Create the UI")
*Protip: You can double-click on the respective control in order to edit its title.*

## Make things do stuff
Hooking up the actions actions/properties is really easy: while `Main.storyboard` is still selected in the `Project Navigator`, click on the `Add Editor on Right` icon (little book with a **+**) in the top right.
![alt text](/resources/T0/5.png "Add Editor on Right")
Xcode will duplicate the storyboard view. Sadly, a `Storyboard` can only be viewed in a single window at a time. Select the newly appeared window on the right and click on the `ViewController.h` file in the `Project Navigator`.
![alt text](/resources/T0/6.png "View the ViewController file")
Press `^⌘` + `↑` to switch to the implementation file. Now `^` + `Click` the first switch from the panel with `Main.storyboard` on the left and drag it under the `@interface` section in the `ViewController.m` file to the right. Give it a proper name.
![alt text](/resources/T0/7.png "@IBOutlet")
Congratulations, you have successfully created an `IBOutlet`! You can now create `@IBOutlet`-s for the rest of the controls. In order to create an `@IBAction` for the **Button**, `^` + `Click` and drag under the `@implementation` section. Give the `@IBAction` a name like **on_SomeNameHere_Tap**.
![alt text](/resources/T0/8.png "@IBAction")
Here, you place the code to get executed when the user touches-up the button. It is up to you to implement the funcionality from the **Requirements** section. _Protip: Want to be a little more advanced? Check [this](https://useyourloaf.com/blog/objective-c-class-properties/) out._

## Some insight
UI in Xcode is built in two ways. One is the more conventional Storyboard-based UI, the other is the brand new and shiny [SwiftUI](https://developer.apple.com/xcode/swiftui/). We will focus on the traditional Storyboard UI, as the other is yet to prove itself being robust and stable enough.

### A story-what?
A `Storyboard` is a collection of [nibs](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/LoadingResources/CocoaNibs/CocoaNibs.html), an ancient technology from days long gone (not really, nibs are awesome and still relevant in some cases). A nib is basically a special XML file, created and edited through Xcode's infamous Interface Builder. Contrary to what is somewhat common practice on Android, on iOS it isn't necessary to edit nibs manually. In this course we will use the Interface Builder to create pretty UI whenever's possible.

### I see header files, what's this, The C Programming Language®?
Yes and no. Objective-C is derived from C. The core of Objective-C is written in C. This means that you can actually use C syntax and primitives inside Objective C toll-free. This also means that you can use C++ inside of Objective-C files. This travesty is called Objective-C++ and is far more common than most people would like. But Objective-C is a higher-level language. For example, the memory in Objective-C is managed by [ARC](https://medium.com/@ITZDERR/ios-memory-management-arc-in-objective-c-and-swift-part2-f8d269c5e9c) (no garbage collection, 100% bullshit-free). This, however, means that you need to be smart about your memory usage, because it is eventually up to you to free up resources, which are not needed. In most cases (thanks to the MVC design pattern) we tend to structure the code in such way that this is actually automatically handled for us. But that's in most cases, not in all. You still need to pay attention.

### App and Scene delegate?
The `AppDelegate` is the entry point of your program. The methods there are important application lifecycle callbacks. Luckily they are properly named and well-documented. The `SceneDelegate` was introduced in iOS 13 when Apple decided to change the concept of a window to that of a scene. Some of the responsibilities of the `AppDelegate` have been moved to the `SceneDelegate`. For now we will rely on Xcode's autoamtically generated App and Scene delegates. Look at [this](https://learnappmaking.com/scene-delegate-app-delegate-xcode-11-ios-13/) for further details.

### I read all of this bullcrap, now what?
If you have any questions, though, please ask away. Any questions, about **anything**. Some of your questions might include:
- Q: Why is this document written in English
    - A: They make me.
- Q: Why is the next one in Bulgarian then?
    - A: [I felt like it.](https://imgur.com/a/TnXDVIg) And I [too] like to live dangerously.

Also, if you don't like something, prithee do tell and I will listen.
Now get your ass to work. :)