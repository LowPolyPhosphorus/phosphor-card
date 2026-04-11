# LowPolyPhosphorus's Hacker Card

A custom NFC business card on a real PCB. Tap it with your phone and it opens my GitHub and socials. The card pulls energy straight from your phone's NFC field to light up the LED, no battery, no charging, nothing extra.

## How It Works

The NT3H2111 chip takes care of both the NFC communication and harvesting power from your phone's NFC field to run the LED. No battery required, no charging, nothing but your phone. There is no separate antenna here, it is simply a PCB trace. What you can see on the board is an actual coil antenna.

## Why I Made It

I wanted something that felt more like me than a paper business card. If I am handing someone my contact info it should at least be interesting. A PCB that lights up when you tap it is more interesting.

## Building One Yourself

Everything is in this repo. EasyEDA schematic, PCB layout, Gerbers ready to send to JLCPCB, BOM and CPL files for assembly. The silkscreen design is fully customizable so you can put your own info on it.

1. Grab the Gerber files from the gerbers folder
2. Upload to JLCPCB with PCBA enabled, the BOM and CPL files are in the same folder
3. When it arrives flash the chip following the steps below
4. Swap out the silkscreen in EasyEDA before ordering if you want your own info on it

## Flashing

The NT3H2111 chip needs to be initialized before it can be written to. Fresh from the factory it will not respond to standard NFC apps.

1. Install NFC Tools on [iOS](https://apps.apple.com/app/nfc-tools/id1252962749) or [Android](https://play.google.com/store/apps/details?id=com.wakdev.wdnfc)
2. Open the app and send this advanced NFC command to initialize the chip:
   `A2:03:E1:10:6D:00,A2:04:03:04:D8:00,A2:05:00:00:FE:00`
3. Once initialized write your URL or contact info to the card using NFC Tools

## Design Files
- Schematic and PCB layout in EasyEDA format in the source folder
- Gerber files ready for JLCPCB in the gerbers folder
- BOM and CPL files for JLCPCB assembly in the gerbers folder
- Silkscreen source file in Figma

## Bill of Materials
| Part | Quantity | Link |
|------|----------|------|
| NT3H2111W0FHKH NFC Chip | 1 | [JLCPCB Parts Library](https://jlcpcb.com/partdetail/NxpSemicon-NT3H2111W0FHKH/C710403) |
| 2V LED | 1 | [JLCPCB Parts Library](https://jlcpcb.com/partdetail/Hubei_KentoElec-17_21SUYCTR8/C2296) |
| 47 Ohm Resistor | 1 | [JLCPCB Parts Library](https://jlcpcb.com/partdetail/23909-0603WAF470JT5E/C23182) |
| 220nF Capacitor | 1 | [JLCPCB Parts Library](https://jlcpcb.com/partdetail/21832-CL10B224KA8NNNC/C21120) |

## Credits
- [Hack Club Hacker Card Jam](https://jams.hackclub.com/jam/hacker-card) for the base schematic and PCB design

### Gallery
<img width="347" height="276" alt="image" src="https://github.com/user-attachments/assets/3cbe7c2c-8cee-41a3-a009-4fbb2882e194" />
<img width="718" height="429" alt="image" src="https://github.com/user-attachments/assets/9e0d9b3c-ca8c-4aa0-ae1d-8db7555d4c9e" />
<img width="351" height="294" alt="image" src="https://github.com/user-attachments/assets/2b57aafb-3d7b-4fa8-98f0-50b12a965eee" />

> it should have these errors ^^ (AND ONLY THESE ERRORS)

<img width="800" height="478" alt="image" src="https://github.com/user-attachments/assets/daafc64c-3914-422a-bd98-802ac2606d39" />
<img width="1055" height="632" alt="image" src="https://github.com/user-attachments/assets/6e766d67-1169-4e43-976f-2147ccbf4a36" />
<img width="979" height="614" alt="image" src="https://github.com/user-attachments/assets/37fab178-6d06-4a7c-adf8-e6644f4e27ae" />

