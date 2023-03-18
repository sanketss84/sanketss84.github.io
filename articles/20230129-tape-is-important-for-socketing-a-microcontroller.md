# Why the tape is super important for socketing a microcontroller

Author: Sanket Sonavane   
Publish Date: 2023-01-29  
Last Updated: 2023-01-29  

<div style="color: #084298; background-color: #cfe2ff; padding: 10px; border: 1px solid #b6d4fe; border-radius: 5px;">  
Hello! Dear Visitor the site is now migrated to [sanketsjournal.com](https://www.sanketsjournal.com).  <br>
It has a better design, dark mode, article search and category pages.  <br>
All my findings and latest adventures will be published on the new address. <br>  
Hope you enjoy the new experience.  
</div> <br>

## Summary
When soldering your microcontroller make sure there is a tape (on all holes) sandwiched between socket and microcontroller. So that when you try to remove the microcontroller you are not surprised that the solder has passed through into the socket and your microcontroller is stuck. 

![](/assets/img/tape-socket-mc/socket-legs.jpg)

## Problem 
I was scrolling through discord of split keyboards and came across a user where he shared that the microcontroller even though socketed would not come out and then it struck me I might have made the same mistake as him while soldering. That lead me to write this and share the problem with everyone who might be new to socketing a microcontroller.

Thomas Bart from splitkb has written a fabulous article on how this is done [How do I socket a microcontroller? – splitkb.com](https://docs.splitkb.com/hc/en-us/articles/360011263059-How-do-I-socket-a-microcontroller-) so please read that article carefully before you solder your socket and microcontroller.

If you are building a custom mechanical keyboard which uses a microcontroller and you decided to socket it then 
- first solder the sockets to the pcb and use tape to hold the socket in place.
- ensure tape is applied to entire socket.
- insert mill max pins or diode legs piercing the tape.
    - for mill-max, how much you need to push the pins inside can be checked by placing your microcontroller on top of the pins to see you have enough of the pin exposed for soldering it.
- once all the pins are added to the sockets, seat the microcontroller on top and solder the microcontroller to the socketed legs.
- now post soldering, gently remove the microcontroller to remove remove the tape.
    - this tape ensures the solder does not pass into the socket below making removal of that microcontroller difficult in the future.
    - if you have used diode legs note they are a bit weaker so straigthen them if bent while reinserting.
- reinsert the microcontroller and you are good to go. 

this tape ensures that the solder does not pass through into the socket its super important part of this whole soldering process as you socket your microcontroller.

Hope this helps someone from making the mistakes I made.