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



