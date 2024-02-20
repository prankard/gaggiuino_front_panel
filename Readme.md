# Gaggiuino Front Panel for Older Gaggia Classic

Designed after I messed up and broke my buttons. If you do this mod, sell your buttons because dang, that is expensive to buy new.

Designed for 19mm ultra short metal led buttons (non-led's would also work, but needs to be ultra short for clearance).

I ordered these to fit in them:
https://www.aliexpress.com/item/1005001683893211.html?spm=a2g0o.order_list.order_list_main.5.7d0218027ARwXe



## Power Button

These buttons I suggested don't carry high voltage **SO DO NOT RUN HIGH VOLTAGE POWER THROUGH THEM** thanks!

I'm using a Sonoff Mini as a power switch to control the mains, and have a low power momentary switch to turn on/off the gaggia classic. **Be careful of the amps the power wifi switch can support in your region, I'm on 240v here so lower amps than in USA**. Perhaps a Shelly 16A would be a better choice for USA, but please do your research, I'm not an electrician.



## Momentary switches

I've forked the main repo, and have made a **branch** called **feature/momentary_buttons**. You can find that here (difference in Perhiperals.h):
https://github.com/prankard/gaggiuino/tree/feature/momentary-buttons

You need to compile with that, and add the build flags to allow for momentary steam and brew buttons (and any extra flags you want too for your device/system):

	[extra]
	build_flags =
		-DSTEAM_MOMENTARY
		-DBREW_MOMENTARY

# Parts

#### Front panel 

This was laser cut on mine (you can 3d print this too, it's in the source). I would combine that with the side panel into 1 piece if you wanted. The etching was done with protective plastic on, then spray painted after and then peeled off to get the 2 tone effect. You can also buy engraving plastic which is great, but is expensive.

##### 3d File

![](/images/FrontPanel.png)

##### Laser Cut Template

![GaggiuinoFrontPanel4](/vector/GaggiuinoFrontPanel4.svg)

#### Front Edge (Use mirror file)

Is glued to the front panel, houses the screen and buttons. It's mirrored as i got it wrong at first.

![FrontEdgeMirror](/images/FrontEdgeMirror.png)

#### Connecting Clip

Clips into the hole in the main Gaggia frame where switches were, it has small clips for a thin flexible panel to save the electronics from steam/water and screws into the Front Edge.

![ConnectingClip](/images/ConnectingClip.png)

#### Flexible Panel

Goes over the connecting panel, and bends into clips. Has a small hole for wires.

![FlexiblePanel](/images/FlexiblePanel.png)

# Assembly

- Wire screen first with wires in the correct holes, and put wires through gaggia classic hole, connecting clip, frontedge and front panel before plugging in.
- Then put screen into front edge mirror and screw with m3 screws (same as HW scales mod 3mm screws with 6mm length)

- Screw connecting clip to front edge mirror (same screws)

- Clip in front panel with connecting clip into gagguino (I used a thin flat metal object to help guide and squeeze the clip to the base propertly)

Pieces in a sandwich should be in this order:

- Front panel -> FrontEdgeMirror -> Connecting Clip -> Flexible Panel





# Improvements

- Lasered with 3mm plastic, would be nice to be thinner to help with thickness of model

- Cutout for screen could use a chamfer and possibly more room to allow for easier pressing buttons in the corners

- Could be moved down a notch for better aesthetics (more spacing at top of Gaggia)

- Maybe backplate to stop shorting of lose components/or rely of pcb holder

- Could lose about 1-2mm on the connecting piece height for ease of entry

- Could lose about 2-3mm on middle connecting piece to lessen gap between the gaggia frame and 3d printer edges on the front.

- Would be cool to add extra geometry for routing wires, and also space for placing internal pcbs for the buttons.

- Can we design something to house the original metal frame piece that went with the original switches?

- Clip could be made slightly easier to snap in the 2 sides, I had to use a thin blade to pull in the clip fully.
- Laser cut outer edge need to account for laser cutting size, (so make the outside edge slightly thicker)



# Attribution

Thanks to of course the [Gaggiuino](https://gaggiuino.github.io/#/) project

And thanks to @Loogle with their [Gaggiuino Logo](https://www.printables.com/model/261455-gaggiuino-branding) vector file 