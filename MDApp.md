<pre>
from kivymd.app import MDApp
from kivymd.uix.button import MDRectangleFlatButton
from kivymd.uix.screen import MDScreen


class Main(MDApp):
    def build(self):
        screen = MDScreen()
        btn = MDRectangleFlatButton(text="Hello World",
                                    pos_hint={'center_x': 0.5, 'center_y': 0.5}
                                    )
        screen.add_widget(btn) 
        return screen


Main().run()
</pre>


**def build** : function is the app entry point. All the things defined here will be built first and the first screen or the main screen is passed here


# 1. Key Elements of KivyMD

### A. Screen
All the things require a stage. The screen element is the first thing an app will have. All the activities, components are defined on a screen. It is defined simply by calling it in the KV file.
 <pre>
 Screen:
    components
    .
    .
    .
</pre>

### B. MDLabel
This component makes it possible to display any text on your app screen. We can display any component in many ways:


<pre>
from kivymd.app import MDApp
from kivy.lang import Builder


class Main(MDApp):
    def build(self):
        return Builder.load_file("label.kv")


Main().run()

#label.kv
#Screen:
#    MDLabel:
#        text: "[b]Thanks for reading my Medium article![/b]"
#        halign: "center"
#        font_style: "H4"
#        markup: True
</pre>


<pre>
from kivymd.app import MDApp
from kivymd.uix.screen import Screen
from kivymd.uix.label import MDLabel

class Main(MDApp):
    def build(self):
        screen = Screen()
        label = MDLabel(text="[b]Thanks for reading my Medium article![/b]",
                        halign='center',
                        font_style='H4',
                        markup=True)
        screen.add_widget(label)
        return screen


Main().run()
</pre>

*# As you can see above, it is hierarchically placed on the screen.*

And you can also see various properties of Label 


1. font_style: Available options are ‘H1’, ‘H2’, ‘H3’, ‘H4’, ‘H5’, ‘H6’, ‘Subtitle1’, ‘Subtitle2’, ‘Body1’, ‘Body2’, ‘Button’, ‘Caption’, ‘Overline’, ‘Icon’.
2. text
3. theme_text_color: Available options are ‘Primary’, ‘Secondary’, ‘Hint’, ‘Error’, ‘Custom’, ‘ContrastParentBackground’.
4. text_color: Text color is given in RGBA format 255
5. halign and valign: We can assign the position of the text horizontally and vertically. Available options are auto, left, center, right, and justify.
6. markup: We can use the markup language to customize the text. You need to specify markup = True to use the markup options. Check the kivy markup documentation for all the available actions.



### C. MDButton

It enables you to make the UI interactive by binding the button action with other widgets. These bindings are performed by referring to each other ids. There are various types of buttons available in Kivymd and you can choose any button which suits your requirements.

##### < Available options are >
+ MDIconButton
+ MDFloatingActionButton
+ MDFlatButton
+ MDRaisedButton
+ MDRectangleFlatButton
+ MDRectangleFlatIconButton
+ MDRoundFlatButton
+ MDRoundFlatIconButton
+ MDFillRoundFlatButton
+ MDFillRoundFlatIconButton
+ MDTextButton
+ MDFloatingActionButtonSpeedDial



















