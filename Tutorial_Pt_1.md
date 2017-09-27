### Let's talk General Layout
*5 minute read*
#### layout
Causecade can be divided up into four general regions. 
These regions help users get to what they want quickly, and in consistent places.
The regions are: main header, variable viewer, network canvas, and the contextual zone.

##### Main Header
This region is the top bar running along the full width of the screen in pink or blue. 
To the top left we find the page name, which will refresh the page, which can be helpful if something goes wrong. To the right of that we find a prominent button labeled *learning mode*. Since the UI is currently all blue, it means learning mode is enabled. Try <span class="lessonGoal" id="goal_1">switching it off and on</span> by pressing the button and see what happens. If everything has gone according to plan, you will have seen this text menu dissapear when you turned it off and have seen the UI shift back to the pink that you were greeted with. Switching with this button will preserve progress in lessons, so dont hestitate to hide it temporarily.

To the right of this, we find three more buttons. Hovering over them will give you some more info. The *help* menu will open up a small dialog window with some information which may be useful if you are experiences issues or have questions about CauseCade. *blog* will direct you to the blog page of CauseCade, which will hold some information about changes to CauseCade, milestones and other general meta-information about it. Then finally, *report bug* will direct you to a page where you can report bugs or leave general comments about CauseCade if they are not urgent.
Even further right, we find an icon, which can be pressed to reveal the notification bar. This notification bar will display all executed commands within CauseCade. This allows you to trace what you have done and find possible mistakes. Clicking it <span class="lessonGoal" id="goal_2">(try it)</span> will hide/reveal the notifications. Clicking Clear will clear all notifications. At the current time it is not possible to clear individual notifications.

Then, moving one layer down, we find a set of tabs with labels: 1) overview, 2) details, and 3) edit. These tabs will control what is displayed in the **variable viewer** section. As they are tabs, only one can be selected at a time. If you press them <span class="lessonGoal" id="goal_3">(try clicking details)</span>, you will see that nothing happens. This is because in order for the **variable viewer** to be displayed, you must have a variable selected. We will go into more detail on this in the next lesson. 
In the middle of this row, we find the network name input. When you load a network in, it will set the name of the network to this loaded network name (provided you didnt set anything yet). The primary use of this is to name your network before you save it so you can keep track of it. As of now, this feature does not do anything particularly important. Try <span class="lessonGoal" id="goal_4">setting the name</span> to something you like (it doesn't matter what).
Finally, on the far right, we find the network display tabs. These control what the **network canvas** displays. As of now, only one mode is available (Network), so you can ignore this.

##### Variable Viewer

Then, moving one layer down we find a set of tabs with labels 1) overview, 2) details, and 3) edit. These tabs will control what is displayed in the **variable viewer** section. As they are tabs, only one can be selected at a time. If you press them (try clicking details), you will see that nothing happens. This is because in order for the **variable viewer** to be displayed, you must have a variable selected. We will go into more detail on this in the next lesson. 
This section will take up the left third of the screen when a variable is selected. As mentioned before, it can be in one of three different modes. (overview,details,edit) These sections will be important to inspect the network and to go from a network depiction to a quantitative representation.

##### Network Canvas

This is everything that is not the main header (i.e. everything below the main header). On this white *canvas* the network will de displayed for you to interact with. Elements such as the **variable viewer** and **contextual zone** will be drawn on top of this. 

##### Contextual zone

This region (opposite the **variable viewer**) will hold various menus, depending on the context. As of right now, it is holding the learning menu, which is what you are reading in right now! In the future, other menus will be able to be displayed here, such as a network meta information menu and more. Note how this menu is indeed drawn over the **Network Canvas**. Remember this *particular* contextual menu (learning mode) can be hidden by pressing the learning mode button.

#### Now Visually

<img src="https://static.planetminecraft.com/files/resource_media/screenshot/1529/colourtv9142868.jpg" height="200" width="200">
