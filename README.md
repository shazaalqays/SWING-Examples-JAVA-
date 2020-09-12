# task1
Swing overview and a simple example.
# Getting started
In order to learn swing we have to work on netbeans IDE.
## Prerequisites
Install netbeans IDE on your PC.
# Swing
Swing API is a set of extensible GUI Components to ease the developer's life to create JAVA based Front End/GUI Applications. It is build on top of AWT API and acts as a replacement of AWT API, since it has almost every control corresponding to AWT controls. Swing component follows a Model-View-Controller architecture to fulfill the following criterias.
* A single API is to be sufficient to support multiple look and feel.
* API is to be model driven so that the highest level API is not required to have data.
* API is to use the Java Bean model so that Builder Tools and IDE can provide better services to the developers for use.
# Swing Features
* Light Weight − Swing components are independent of native Operating System's API as Swing API controls are rendered mostly using pure JAVA code instead of underlying operating system calls.
* Rich Controls − Swing provides a rich set of advanced controls like Tree, TabbedPane, slider, colorpicker, and table controls.
* Highly Customizable − Swing controls can be customized in a very easy way as visual apperance is independent of internal representation.
* Pluggable look-and-feel − SWING based GUI Application look and feel can be changed at run-time, based on available values.
# Swing Controls
Every user interface considers the following three main aspects −
* UI Elements − These are the core visual elements the user eventually sees and interacts with.
* Layouts − They define how UI elements should be organized on the screen and provide a final look and feel to the GUI (Graphical User Interface). 
* Behavior − These are the events which occur when the user interacts with UI elements.
<br/><br/>
Every SWING controls inherits properties from the following Component class hiearchy.
* Component: a component is the abstract base class for the non menu user-interface controls of SWING. Component represents an object with graphical representation.
* Container: a container is a component that can contain other SWING components.
* JComponent: a JComponent is a base class for all SWING UI components. In order to use a SWING component that inherits from JComponent, the component must be in a containment hierarchy whose root is a top-level SWING container.
