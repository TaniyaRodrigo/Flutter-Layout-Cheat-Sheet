# Flutter-Layout-Cheat-Sheet

This repo includes identified Flutter Layouts which anyone can refer as their layout cheat sheet.
Useful widgets and libraries in Flutter
Widgets.
Flutter widgets are built using a modern framework that takes inspiration from React. The central idea is that you build your UI out of widgets. Widgets describe what their view should look like given their current configuration and state. When a widget’s state changes, the widget rebuilds its description, which the framework diffs against the previous description in order to determine the minimal changes needed in the underlying render tree to transition from one state to the next.
SafeArea – Use to wrap another widget with SafeArea , it adds any necessary padding needed to keep your widget from being blocked by the system status bar, notches, holes, rounded corners and other "creative" features by manufactures.
Expanded widget - Expands a child of a Row, Column, or Flex so that the child fills the available space. Expanded widget makes a child of a Row, Column, or Flex expand to fill the available space along the main axis.
AnimatedContainer - Use for Implicit animations in Flutter
 PageView Widget - Scrollable list but rather works as a page
Opacity widget - used to hide your widget from view or you want to make it partially transparent.
Table Widget- Use for directly showing table from a json(Map)
 FadeTransition - Use to perform a fade animation on its child widget
Wrap – This widget is similar to Row or a Column widget with an added advantage that it can adjust its children according to the space available to it on the Screen. A widget that displays its children in multiple horizontal or vertical runs.
SliverAppBar - Use to create an app bar with various scrolling effects.
