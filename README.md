# Flutter-Layout-Cheat-Sheet

This repo includes identified Flutter Layouts which anyone can refer as their layout cheat sheet.

Useful widgets and libraries in Flutter.

Widgets.

Flutter widgets are built using a modern framework that takes inspiration from React. The central idea is that you build your UI out of widgets. Widgets describe what their view should look like given their current configuration and state. When a widget’s state changes, the widget rebuilds its description, which the framework diffs against the previous description in order to determine the minimal changes needed in the underlying render tree to transition from one state to the next.

SafeArea – Use to wrap another widget with SafeArea , it adds any necessary padding needed to keep your widget from being blocked by the system status bar, notches, holes, rounded corners and other "creative" features by manufactures.

Expanded widget - Expands a child of a Row, Column, or Flex so that the child fills the available space. Expanded widget makes a child of a Row, Column, or Flex expand to fill the available space along the main axis.

AnimatedContainer - Use for Implicit animations in Flutter.

 PageView Widget - Scrollable list but rather works as a page.
 
Opacity widget - used to hide your widget from view or you want to make it partially transparent.

Table Widget- Use for directly showing table from a json(Map).

 FadeTransition - Use to perform a fade animation on its child widget.
 
Wrap – This widget is similar to Row or a Column widget with an added advantage that it can adjust its children according to the space available to it on the Screen. A widget that displays its children in multiple horizontal or vertical runs.

SliverAppBar - Use to create an app bar with various scrolling effects.

FutureBuilder-Widget that builds itself based on the latest snapshot of interaction with a Future.The future must have been obtained earlier, e.g. during State.initState, State.didUpdateConfig, or State.didChangeDependencies. It must not be created during the State.build or StatelessWidget.build method call when constructing the FutureBuilder. If the future is created at the same time as the FutureBuilder, then every time the FutureBuilder's parent is rebuilt, the asynchronous task will be restarted.

FloatingActionButton -A FloatingActionButton in material design is a button on a screen that is tied to an obvious action which a user would usually do on that specific screen. This button floats above the content of the screen and usually resides on one corner of the screen. For example, in Gmail, the main screen has a FloatingActionButton to compose emails. The purpose of the FAB must be something the user might frequently want or needs to do. Flutter offers two types of FloatingActionButtons out-of-the-box.
1.	FloatingActionButton
2.	FloatingActionButton.extended

SliverList -SliverList is useful when you want to scroll through a large number of items. Like all Slivers, this must also be a part of CustomScrollView. You can have a SliverAppBar widget on top of your list to create that beautiful collapsing app bar animation as you scroll through your list.

SliverGrid-Just like a SliverList, this widget is useful when you want to scroll through a large number of items but want them to be arranged in a Grid fashion. Like all Slivers, this must also be a part of CustomScrollView. Yes, you can have a SliverAppBar widget on top of this widget to create that beautiful collapsing app bar animation as you scroll through your list.

FadeInImage-This widget will let you place a placeholder image in the view while you wait for the image to download. All you have to do is specify a placeholder image and the image URL to it and you are done. The placeholder image is replaced by the downloaded image with a smooth animation.

StreamBuilder -Widget that can convert a stream of user defined objects, to widgets. This takes two arguments
•	A stream
•	A builder, that can convert the elements of the stream to widgets
Suppose, you have a Stream, that updates if there is any UI update (may be from user interaction, or may be resulted from network updates). If your “main” widget, includes a StreamBuilder, which listens to the stream, it can act as the element in charge of translating your states to views.

InheritedModel - An InheritedWidget that's intended to be used as the base class for models whose dependents may only depend on one part or "aspect" of the overall model.An inherited widget's dependents are unconditionally rebuilt when the inherited widget changes per InheritedWidget.updateShouldNotify. This widget is similar except that dependents aren't rebuilt unconditionally.Widgets that depend on an InheritedModel qualify their dependence with a value that indicates what "aspect" of the model they depend on. When the model is rebuilt, dependents will also be rebuilt, but only if there was a change in the model that corresponds to the aspect they provided.The type parameter T is the type of the model aspect objects

ClipRRect - A widget that clips its child using a rounded rectangle. It's very similar to ClipRect, but with rounded corners. You can set the border radius using borderRadious option which is of type BorderRadius. A widget that clips its child using a rounded rectangle.By default, ClipRRect uses its own bounds as the base rectangle for the clip, but the size and location of the clip can be customized using a custom clipper.

Hero - A Hero Animation in one sentence is simply an element of one screen “flying” to the next when the app goes to the next page. You can create this animation in Flutter with Hero widgets. As the hero animates from the source to the destination route, the destination route (minus the hero) fades into view. Typically, heroes are small parts of the UI, like images, that both routes have in common. From the user’s perspective the hero “flies” between the routes.

CustomPaint-A widget that provides a canvas on which to draw during the paint phase.When asked to paint, CustomPaint first asks its painter to paint on the current canvas, then it paints its child, and then, after painting its child, it asks its foregroundPainter to paint. The coordinate system of the canvas matches the coordinate system of the CustomPaint object. The painters are expected to paint within a rectangle starting at the origin and encompassing a region of the given size. (If the painters paint outside those bounds, there might be insufficient memory allocated to rasterize the painting commands and the resulting behavior is undefined.) To enforce painting within those bounds, consider wrapping this CustomPaint with a ClipRect widget.

Tooltip - A material design tooltip.Tooltips provide text labels that help explain the function of a button or other user interface action. Wrap the button in a Tooltip widget to show a label when the widget long pressed (or when the user takes some other appropriate action).

FittedBox - Widget to help in creating a quick and neater way to contain a child inside a parent. The main purpose of using the FittedBox is to make the App UI look neater for dynamic children with varying length. In this tutorial, we will look at this simple widget and also, in addition, see how it can be used.

LayoutBuilder - Builds a widget tree that can depend on the parent widget's size.Similar to the Builder widget except that the framework calls the builder function at layout time and provides the parent widget's constraints. This is useful when the parent constrains the child's size and doesn't depend on the child's intrinsic size. The LayoutBuilder's final size will match its child's size. The child should be smaller than the parent, consider wrapping the child in an Align widget. If the child might want to be bigger, consider wrapping it in a SingleChildScrollView.

AbsorbPointer - A widget that absorbs pointers during hit testing. When absorbing is true, this widget prevents its subtree from receiving pointer events by terminating hit testing at itself. It still consumes space during layout and paints its child as usual. It just prevents its children from being the target of located events, because it returns true from RenderBox.hitTest. 

Transform - A widget that applies a transformation before painting its child.Unlike RotatedBox, which applies a rotation prior to layout, this object applies its transformation just prior to painting, which means the transformation is not taken into account when calculating how much space this widget's child (and thus this widget) consumes. A Transform widget “transforms” (i.e. changes the shape, size, position and orientation) its child widget before painting it. This is extremely useful for custom shapes and many different kinds of animations in Flutter.

BackdropFilter  - A widget that applies a filter to the existing painted content and then paints child. Flutter — BackdropFilter. In the top part of the screenshot, we are using the Flutter image. ImageFilter.blur is responsible for blurring. A widget that applies a filter to the existing painted content and then paints child. The filter will be applied to all the area within its parent or ancestor widget's clip. If there's no clip, the filter will be applied to the full screen.

Align - A widget that aligns its child within itself and optionally sizes itself based on the child's size.For example, to align a box at the bottom right, you would pass this box a tight constraint that is bigger than the child's natural size, with an alignment of Alignment.bottomRight. This widget will be as big as possible if its dimensions are constrained and widthFactor and heightFactor are null. If a dimension is unconstrained and the corresponding size factor is null then the widget will match its child's size in that dimension. If a size factor is non-null then the corresponding dimension of this widget will be the product of the child's dimension and the size factor. For example if widthFactor is 2.0 then the width of this widget will always be twice its child's width.

Positioned - A widget that controls where a child of a Stack is positioned. A Positioned widget must be a descendant of a Stack, and the path from the Positioned widget to its enclosing Stack must contain only StatelessWidgets or StatefulWidgets (not other kinds of widgets, like RenderObjectWidgets). If a widget is wrapped in a Positioned, then it is a positioned widget in its Stack. If the top property is non-null, the top edge of this child will be positioned top layout units from the top of the stack widget. The right, bottom, and left properties work analogously.
If both the top and bottom properties are non-null, then the child will be forced to have exactly the height required to satisfy both constraints. Similarly, setting the right and left properties to non-null values will force the child to have a particular width. Alternatively the width and height properties can be used to give the dimensions, with one corresponding position property (e.g. top and height).If all three values on a particular axis are null, then the Stack.alignment property is used to position the child. If all six values are null, the child is a non-positioned child. The Stack uses only the non-positioned children to size itself.

AnimatedBuilder - A general-purpose widget for building animations. AnimatedBuilder is useful for more complex widgets that wish to include an animation as part of a larger build function. To use AnimatedBuilder, simply construct the widget and pass it a builder function.
For simple cases without additional state, consider using AnimatedWidget. f your builder function contains a subtree that does not depend on the animation, it's more efficient to build that subtree once instead of rebuilding it on every animation tick.If you pass the pre-built subtree as the child parameter, the AnimatedBuilder will pass it back to your builder function so that you can incorporate it into your build.Using this pre-built child is entirely optional, but can improve performance significantly in some cases and is therefore a good practice.

Dismissible - A widget that can be dismissed by dragging in the indicated direction. Dragging or flinging this widget in the DismissDirection causes the child to slide out of view. Following the slide animation, if resizeDuration is non-null, the Dismissible widget animates its height (or width, whichever is perpendicular to the dismiss direction) to zero over the resizeDuration. Backgrounds can be used to implement the "leave-behind" idiom. If a background is specified it is stacked behind the Dismissible's child and is exposed when the child moves. The widget calls the onDismissed callback either after its size has collapsed to zero (if resizeDuration is non-null) or immediately after the slide animation (if resizeDuration is null). If the Dismissible is a list item, it must have a key that distinguishes it from the other items and its onDismissed callback must remove the item from the list.

SizedBox - A box with a specified size. If given a child, this widget forces its child to have a specific width and/or height (assuming values are permitted by this widget's parent). If either the width or height is null, this widget will size itself to match the child's size in that dimension. If not given a child, SizedBox will try to size itself as close to the specified height and width as possible given the parent's constraints. If height or width is null or unspecified, it will be treated as zero. The new SizedBox.expand constructor can be used to make a SizedBox that sizes itself to fit the parent. It is equivalent to setting width and height to double.infinity.

ValueListenableBuilder - A widget whose content stays synced with a ValueListenable. Given a ValueListenable<T> and a builder which builds widgets from concrete values of T, this class will automatically register itself as a listener of the ValueListenable and call the builder with updated values when the value changes. If your builder function contains a subtree that does not depend on the value of the ValueListenable, it's more efficient to build that subtree once instead of rebuilding it on every animation tick. If you pass the pre-built subtree as the child parameter, the ValueListenableBuilder will pass it back to your builder function so that you can incorporate it into your build. Using this pre-built child is entirely optional, but can improve performance significantly in some cases and is therefore a good practice.

Draggable - A widget that can be dragged from to a DragTarget. When a draggable widget recognizes the start of a drag gesture, it displays a feedback widget that tracks the user's finger across the screen. If the user lifts their finger while on top of a DragTarget, that target is given the opportunity to accept the data carried by the draggable. On multitouch devices, multiple drags can occur simultaneously because there can be multiple pointers in contact with the device at once. To limit the number of simultaneous drags, use the maxSimultaneousDrags property. The default is to allow an unlimited number of simultaneous drags. This widget displays child when zero drags are under way. If childWhenDragging is non-null, this widget instead displays childWhenDragging when one or more drags are underway. Otherwise, this widget always displays child.

AnimatedList - A scrolling container that animates items when they are inserted or removed. This widget's AnimatedListState can be used to dynamically insert or remove items. To refer to the AnimatedListState either provide a GlobalKey or use the static of method from an item's input callback. This widget is similar to one created by ListView.builder.
Flexible - A widget that controls how a child of a Row, Column, or Flex flexes.Using a Flexible widget gives a child of a Row, Column, or Flex the flexibility to expand to fill the available space in the main axis (e.g., horizontally for a Row or vertically for a Column), but, unlike Expanded, Flexible does not require the child to fill the available space. A Flexible widget must be a descendant of a Row, Column, or Flex, and the path from the Flexible widget to its enclosing Row, Column, or Flex must contain only StatelessWidgets or StatefulWidgets (not other kinds of widgets, like RenderObjectWidgets).

MediaQuery - Establishes a subtree in which media queries resolve to the given data. For example, to learn the size of the current media (e.g., the window containing your app), you can read the MediaQueryData.size property from the MediaQueryData returned by MediaQuery.of: MediaQuery.of(context).size. Querying the current media using MediaQuery.of will cause your widget to rebuild automatically whenever the MediaQueryData changes (e.g., if the user rotates their device). If no MediaQuery is in scope then the MediaQuery.of method will throw an exception, unless the nullOk argument is set to true, in which case it returns null.

Spacer - Spacer creates an adjustable, empty spacer that can be used to tune the spacing between widgets in a Flex container, like Row or Column. The Spacer widget will take up any available space, so setting the Flex.mainAxisAlignment on a flex container that contains a Spacer to MainAxisAlignment.spaceAround, MainAxisAlignment.spaceBetween, or MainAxisAlignment.spaceEvenly will not have any visible effect: the Spacer has taken up all of the additional space, therefore there is none left to redistribute.

InheritedWidget - Base class for widgets that efficiently propagate information down the tree. To obtain the nearest instance of a particular type of inherited widget from a build context, use BuildContext.inheritFromWidgetOfExactType. Inherited widgets, when referenced in this way, will cause the consumer to rebuild when the inherited widget itself changes state.

AnimatedIcon - Shows an animated icon at a given animation progress.
The available icons are specified in AnimatedIcons.




