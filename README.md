# Chrysler-Dodge-Jeep-Mygig-radio
I created code for using mygig radio on workbench or in non can bus vehicle
using an Arduino Nano and MCP 2515 can bus shield (plus a buck converter if in vehicle with alternator output above 12 volts) 
I created sketches to control a mygig radio either low Speed Can B 83.3Kbps or high speed Can IHS 125Kbps
Will work on all mygig radios 
Harmon Becker REN (non nav) and RER (navigational radio) and RHR (navigational radio)
Mitsubishi RBZ (non nav) and RHB (navigational radio) 
Will turn radio on and radio turns off shortly after nano powered down and no longer sending messages
Will allow grounding of single digital pin on nano to switch radio to back up camera mode and display back up camera composite video input
Will allow selection of VES so that externally supplied audio and composite video inputs will display on screen
Will allow on screen display of DVD playing in the mygig radio

The Mygig radios were first offered in select Chrysler/Dodge/Jeep radios in 2007 and continued to be an option thru at least 2018
The RER and RHR version included voice control hands free calling and Sirius sat radio with a subscription
The RHR also including bluetooth music streaming
All mygig radios had a HDD capable of storing MP3 music files either provided via front USB port or via the CD/DVD drive with included the ability to Rip Album CD songs to MP3s stored on the HDD
Most mygig radios have a replaceable PATA HDD but the newer years of RBZ and RHB utilize an SATA replaceable HDD
Cloning of the HDD is fairly straight forward except that the PATA disk in the RBZ and RHB is locked
Only RBZ and RHB have been found to be compatible with a SSD replacement HDD and some of these do not lock
The RER REN and RHR discs are not locked and are all the PATA type and no one has found a way to use a SSD in these units

Typically options like rear screen video (VES) output and back up camera capability requite dealer can bus programming of the vehicle powertrain module or expensive aftermarket adapter boxes but I  determined what code needs to be sent from the arduino to activate these options with out outside help alowing anyone with a nano and can bus shield to DIY their own adapter box

I should also mention that for the RBZ and RHB just adding a switched 12 volt lead to an unused pin in the 22 pin gray harness plug will alow radio turn and off based on if that wire has power and also allow on screen viewing of any DVD playing and for the RHB the navigation feature even works (no can bus required) but to add the backup camera feature and the external composite audio input for display (VES capability) the Nano and can Bus shield and sketch are needed

I will freely share my working sketches for both high speed Can IHS and Low speed can Bus B mygig radios but understand I am a novice programmer with arduino so my approach while effective is not as slick and refined as others could produce as the real work for me was figuring which can bus messages were needed

I also added some code to allow oem steering wheel switch resistances to control the radio

now if I just knew how to post my working sketches









