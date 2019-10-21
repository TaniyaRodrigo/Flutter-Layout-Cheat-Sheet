# Flutter Layout Cheat Sheet

This repo includes identified Flutter Layouts which anyone can refer as their layout cheat sheet.

## USEFUL WIDGET & LIBRARIES IN FLUTTER

## WIDGETS
Flutter widgets are built using a modern framework that takes inspiration from React. The central idea is that you build your UI out of widgets. Widgets describe what their view should look like given their current configuration and state. When a widget’s state changes, the widget rebuilds its description, which the framework diffs against the previous description in order to determine the minimal changes needed in the underlying render tree to transition from one state to the next.

### BASIC WIDGETS

Flutter comes with a suite of powerful basic widgets, of which the following are commonly used:

**Text**

The *Text* widget lets you create a run of styled text within your application.

**Row**

These flex widgets let you create flexible layouts in both the horizontal and vertical directions. The design of these objects is based on the web’s flexbox layout model.

**Stack**

Instead of being linearly oriented (either horizontally or vertically), a *Stack* widget lets you place widgets on top of each other in paint order. You can then use the  "Positioned" widget on children of a  *Stack*  to position them relative to the top, right, bottom, or left edge of the stack. Stacks are based on the web’s absolute positioning layout model.

**Container**

The  *Container* widget lets you create a rectangular visual element. A container can be decorated with a  "BoxDecoration", such as a background, a border, or a shadow. A  *Container*  can also have margins, padding, and constraints applied to its size. In addition, a  *Container*  can be transformed in three dimensional space using a matrix.

**Appbar**

A Material Design app bar. An app bar consists of a toolbar and potentially other widgets, such as a TabBar and a FlexibleSpaceBar.

**Column**

Layout a list of child widgets in the vertical direction.

**FlutterLogo**

The Flutter logo, in widget form. This widget respects the IconTheme.

**Placeholder**

A widget that draws a box that represents where other widgets will one day be added.

**RaisedButton**

A Material Design raised button. A raised button consists of a rectangular piece of material that hovers over the interface.

**Scaffold**

Implements the basic Material Design visual layout structure. This class provides APIs for showing drawers, snack bars, and bottom sheets.

Create beautiful apps faster with Flutter’s collection of visual, structural, platform, and interactive widgets.

**Accessibility**

Make your app accessible.

 *1. ExcludeSemantics*

 - A widget that drops all the semantics of its descendants. This can be
   used to hide sub-widgets that would otherwise be reported but that
   would only be confusing. For example, the Material Components Chip
   widget hides the avatar since it is redundant with the chip label.

 *2. MergeSemantics*

 - A widget that merges the semantics of its descendants

*3. Semantics*

 - A widget that annotates the widget tree with a description of the
   meaning of the widgets. Used by accessibility tools, search engines,
   and other semantic analysis software to determine the meaning of the
   application.
   
**Animation and Motion**

Bring animations to your app.

*1. AnimatedBuilder*

 - A general-purpose widget for building animations. AnimatedBuilder is
   useful for more complex widgets that wish to include an animation as
   part of a larger build function. To use AnimatedBuilder, simply
   construct the widget and pass it a builder function.

*2. AnimatedContainer*

 - A container that gradually changes its values over a period of time.

*3. AnimatedCrossFade*

 - A widget that cross-fades between two given children and animates
   itself between their sizes.

**Text**

Display and style text.

*1. DefaultTextStyle*

 - The text style to apply to descendant Text widgets without explicit
   style.

*2. RichText*

 - The RichText widget displays text that uses multiple different
   styles. The text to display is described using a tree of TextSpan
   objects, each of which has an associated style that is used for that
   subtree. The text might break across multiple lines or might all be
   displayed on the same line depending on the layout constraints.

**Styling**

 - Manage the theme of your app, makes your app responsive to screen
   sizes, or add padding.

*1. MediaQuery*

 - Establishes a subtree in which media queries resolve to the given
   data.

*2. Padding*

 - A widget that insets its child by the given padding.
   
 *3. Theme*
  
 - Applies a theme to descendant widgets. A theme describes the colors
   and typographic choices of an application.
   
## LIBRARIES

5 Libraries that make Flutter development easier and faster.

**1. get_it**

*Get_it* is a simple Inversion of Control Containers and the Dependency Injection pattern implementation.

 - Extremely important if you use GetIt: ALWAYS use the same style to
   import your project files either as relative paths OR as package
   which I recommend. DON’T mix them because currently Dart treats types
   imported in different ways as two different types although both
   reference the same file.

***Different ways of registration.***

![enter image description here](https://miro.medium.com/max/1679/1*g63Bjic1C5oy6dweXLjKDA.png)

***To access the registered objects call  `get<Type>()`  on your  `GetIt` instance.***

![enter image description here](https://miro.medium.com/max/1654/1*G6Rkbk6RqQmln3dhCO37OQ.png)

**2. dio**

*Dio* a powerful Http client for Dart, which supports Interceptors, Global configuration, FormData, Request Cancellation, File downloading, Timeout etc.

![enter image description here](https://miro.medium.com/max/1589/1*VySz33qAb-gBILX1YN47XA.png)

# 3. rxdart

[RxDart](https://github.com/ReactiveX/rxdart) is a reactive functional programming library for Google Dart, based on  [ReactiveX](http://reactivex.io/). Google Dart comes with a very decent  [Streams](https://api.dartlang.org/stable/1.21.1/dart-async/Stream-class.html)  API out-of-the-box; rather than attempting to provide an alternative to this API, RxDart adds functionality on top of it.

**4. flutter_secure_storage**

*flutter_secure_storage*  is a Flutter plugin to store data in secure storage:

-   Keychain is used for iOS.
-   AES encryption is used for Android. AES secret key is encrypted with RSA and RSA key is stored in KeyStore
```
// Create storage  
final storage = new FlutterSecureStorage();  
  
// Read value   
String value = await storage.read(key: key);  
  
// Read all values  
Map<String, String> allValues = await storage.readAll();  
  
// Delete value   
await storage.delete(key: key);  
  
// Delete all   
await storage.deleteAll();  
  
// Write value   
await storage.write(key: key, value: value);
```
**5. flushbar**

With  *flushbar* can create quick information messages, error messages, warning message, etc. Notifying users about certain actions is a must in the world of mobile apps.
