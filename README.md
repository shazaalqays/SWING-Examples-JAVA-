# Task1
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
<br/><br/>Every SWING controls inherits properties from the following Component class hiearchy.
* Component: a component is the abstract base class for the non menu user-interface controls of SWING. Component represents an object with graphical representation.
* Container: a container is a component that can contain other SWING components.
* JComponent: a JComponent is a base class for all SWING UI components. In order to use a SWING component that inherits from JComponent, the component must be in a containment hierarchy whose root is a top-level SWING container.
# Simple Menu example
## Part of code
Method to change color of icons
```
public void changeColor(JPanel hover, Color rand){
        hover.setBackground(rand);
        
    }
```
Method to work with menu bar
```
public void clickmenu(JPanel h1, JPanel h2, int numberbool){
        if(numberbool == 1){
            h1.setBackground(new Color(85, 119, 140));
            h2.setBackground(new Color(0, 52, 83));
        }
        else{
            h1.setBackground(new Color(0, 52, 83));
            h2.setBackground(new Color(85, 119, 140));
        }
    }
```
Method to hide and show the menu bar
```
public void hideshow(JPanel showhide, boolean dashboard, JLabel button){
        if(dashboard == true){
            showhide.setPreferredSize(new Dimension(50,showhide.getHeight()));
               changeImage(button,"/icon/menu.png");
        }
        else{
            showhide.setPreferredSize(new Dimension(270,showhide.getHeight()));
            changeImage(button,"/icon/iconfinder_back-alt_134226.png");
        }
    }
```
Method to change the menu bar icon
```
    public void changeImage(JLabel button, String reimg){
        ImageIcon aimg = new ImageIcon(getClass().getResource(reimg));
        button.setIcon(aimg);
    }
```
Methods for close icon
```
    private void closeMouseExited(java.awt.event.MouseEvent evt) {                                  
        // TODO add your handling code here:
        changeColor(buttonclose, new Color(0, 52, 83));
    }                                 

    private void closeMouseEntered(java.awt.event.MouseEvent evt) {                                   
        // TODO add your handling code here:
        changeColor(buttonclose, new Color(85, 119, 140));
    }                                  

    private void closeMouseClicked(java.awt.event.MouseEvent evt) {                                   
        // TODO add your handling code here:
        System.exit(0);
    }                                  
```
Methods for maximize icon
```
    private void maxMouseClicked(java.awt.event.MouseEvent evt) {                                 
        if(this.getExtendedState()!= sw.MAXIMIZED_BOTH){
            this.setExtendedState(sw.MAXIMIZED_BOTH);
        }
        else{
            this.setExtendedState(sw.NORMAL);
        }
        
    }                                

    private void maxMouseEntered(java.awt.event.MouseEvent evt) {                                 
        // TODO add your handling code here:
        changeColor(buttonmax, new Color(85, 119, 140));
    }                                

    private void maxMouseExited(java.awt.event.MouseEvent evt) {                                
        // TODO add your handling code here:
        changeColor(buttonmax, new Color(0, 52, 83));
    }                               
```
Methods for menu bar
```
    private void hidemenubuttonMouseEntered(java.awt.event.MouseEvent evt) {                                            
        // TODO add your handling code here:
        changeColor(hidemenu, new Color(85, 119, 140));
    }                                           

    private void hidemenubuttonMouseExited(java.awt.event.MouseEvent evt) {                                           
        // TODO add your handling code here:
        changeColor(hidemenu, new Color(0, 52, 83));
    }                                          

    private void hidemenubuttonMouseClicked(java.awt.event.MouseEvent evt) {                                            
        // TODO add your handling code here:
        clickmenu(hidemenu,setting,1);
        if(a==true){
            hideshow(menu,a,hidemenubutton);
            SwingUtilities.updateComponentTreeUI(this);
            a = false;
        }
        else{
            hideshow(menu,a, hidemenubutton);
            SwingUtilities.updateComponentTreeUI(this);
            a = true;
        }
        
    }                                           
```
Methods to make red and green light above menu icon and setting icon
```
    private void listMouseEntered(java.awt.event.MouseEvent evt) {                                  
        // TODO add your handling code here:
        changeColor(list, new Color(247, 78, 105));
    }                                 

    private void listMouseExited(java.awt.event.MouseEvent evt) {                                 
        // TODO add your handling code here:
        changeColor(list, new Color(5, 10, 46));
    }                                

    private void listMouseClicked(java.awt.event.MouseEvent evt) {                                  
        // TODO add your handling code here:
        clickmenu(setting,hidemenu,1);
    }                                 

    private void linehideMouseEntered(java.awt.event.MouseEvent evt) {                                      
        // TODO add your handling code here:
        changeColor(linehide, new Color(8, 177, 150));
    }                                     

    private void linehideMouseExited(java.awt.event.MouseEvent evt) {                                     
        // TODO add your handling code here:
        changeColor(linehide, new Color(5, 10, 46));
    }                                    

    private void linehideMouseClicked(java.awt.event.MouseEvent evt) {                                      
        // TODO add your handling code here:
    }                                     
```
Methods for minimize icon
```
    private void minMouseEntered(java.awt.event.MouseEvent evt) {                                 
        // TODO add your handling code here:
        changeColor(buttonmin, new Color(85, 119, 140));
    }                                

    private void minMouseExited(java.awt.event.MouseEvent evt) {                                
        // TODO add your handling code here:
        changeColor(buttonmin, new Color(0, 52, 83));
    }                               

    private void minMouseClicked(java.awt.event.MouseEvent evt) {                                 
        // TODO add your handling code here:
        if(this.getExtendedState()!= sw.HIDE_ON_CLOSE){
            this.setExtendedState(sw.HIDE_ON_CLOSE);
        }
        else{
            this.setExtendedState(sw.NORMAL);
        }
    }                                

```
## Demo images
![Result1](https://github.com/shazaalqays/task1/blob/master/test/images/demo1.jpg) <br/><br/>
![Result2](https://github.com/shazaalqays/task1/blob/master/test/images/demo2.jpg) <br/><br/>
