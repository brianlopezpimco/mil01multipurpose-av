# **MIL 01-Multipurpose Room: AV Systems Files**

[Biamp DSP System Files](https://github.com/brianlopezpimco/mil01multipurpose-av#biamp-dsp-system-files) contain the audio dsp program that controls how the AV system's audio is proccessed. To replace or upload a new DSP program to a processor, follow the [Biamp DSP System Files Installation](https://github.com/brianlopezpimco/mil01multipurpose-av#biamp-dsp-system-files-installation) section below.

[Cisco User Interface Extension Files](https://github.com/brianlopezpimco/mil01multipurpose-av#cisco-user-interface-extension-files) contain the room controls ui for the Cisco navigator touch panel. To replace or upload new user interface extensions to a codec, follow the [Cisco User Interface Extension Files Installation](https://github.com/brianlopezpimco/mil01multipurpose-av#cisco-user-interface-extension-files-installation) section below.

[Crestron Control System Files](https://github.com/brianlopezpimco/mil01multipurpose-av#crestron-control-system-files) contain the control system program that controls the behavior of the AV system and it's components. To replace or upload new control system code to a processor, follow the [Crestron Control System Files Installation](https://github.com/brianlopezpimco/mil01multipurpose-av#crestron-control-system-files-installation) section below.

## **TABLE OF CONTENTS:**

- [Biamp DSP System Files](https://github.com/brianlopezpimco/mil01multipurpose-av#biamp-dsp-system-files)
- [Biamp DSP System Files Installation](https://github.com/brianlopezpimco/mil01multipurpose-av#biamp-dsp-system-files-installation)
- [Cisco User Interface Extension Files](https://github.com/brianlopezpimco/mil01multipurpose-av#cisco-user-interface-extension-files)
- [Cisco User Interface Extension Files Installation](https://github.com/brianlopezpimco/mil01multipurpose-av#cisco-user-interface-extension-files-installation)
- [Crestron Control System Files](https://github.com/brianlopezpimco/mil01multipurpose-av#crestron-control-system-files)
- [Crestron Control System Files Installation](https://github.com/brianlopezpimco/mil01multipurpose-av#crestron-control-system-files-installation)
- [Additional Resources](https://github.com/brianlopezpimco/mil01multipurpose-av#additional-resources)

## **BIAMP DSP SYSTEM FILES:**

Biamp DSP program accepts preset commands from the control system. There is a mixer block preset for each room configuration.

![tesira-dsp.png](/IMAGES/tesira-dsp.png)

## **CISCO USER INTERFACE EXTENSION FILES:**

### **01-Multipurpose Room Controls: Combine**

![mil01multipurpose-combine-pg.jpg](/IMAGES/mil01multipurpose-combine-pg.jpg)

| USER INTERFACE ELEMENT        | WIDGET ID                |
| ----------------------------- | ------------------------ |
| Room Controls Panel           | roomcontrols-pnl         |
| Combine Page                  | combine-pg               |
| Standalone Mode Button        | combine-standalone-btn   |
| Combine Mode Button           | combine-combine-btn      |

![mil01multipurpose-combine-msg.jpg](/IMAGES/mil01multipurpose-combine-msg.jpg)

## **CISCO USER INTERFACE EXTENSION FILES INSTALLATION:**

To upload a user interface extension file; first login to the codec...

![<Login Screen>](/IMAGES/endpoint-login-screen.PNG)

Browse to "User Interface Extensions" from the main menu...

![<User Interface Extensions>](/IMAGES/ui-extension-zoomtools.PNG)

Select hamburger menu at top right, and select "Merge from File". NOTE: If you select "Import from File" any existing UI extensions will be overwitten when the new extension is loaded...

![<User Interface Extensions>](/IMAGES/ui-extension-merge-file.PNG)

Confirm your UI is loaded correctly, and select "Uploade to Device" from the top right menu to push the UI elements to the endpoint...

![<User Interface Extensions>](/IMAGES/ui-extension-loaded.PNG)

## **CRESTRON CONTROL SYSTEM FILES:**

Crestron SIMPL Windows program registers the CP4 with the endpoint for feedback, and maintains "heartbeat" of communication. Widgets from the room controls panel are handled and commands are executed by the applicable module (e.g. cisco-codec, lutron-qs, etc.). 

![simpl-code.png](/IMAGES/simpl-code.png)

**SIMPL+ Codec Module:** Registers codec for feedback and maintains heartbeat...

![simpl-plus-cisco-codec.png](/IMAGES/simpl-plus-cisco-codec.png)

**SIMPL+ Displays Module:** Handles display widgets and executes Samsung display commands...

![simpl-plus-samsung.png](/IMAGES/simpl-plus-samsung.png)

**SIMPL+ Combine Module:** Handles room combine widgets, generates feedback for touch screens, executes biamp DSP presets, and nvx stream locations...

![simpl-room-combine.png](/IMAGES/simpl-plus-room-combine.png)

## **CRESTRON CONTROL SYSTEM FILES INSTALLATION:**

In order to load compiled code to a Crestron processor, you must install Crestron Toolbox. You may need to register with Crestron and request access the software. Once installed, open Toolbox, then open the "Easy Config" tool. (tools menu). Once open, click the pencil at bottom, enter address of processor to connect...

![toolbox-connect.png](/IMAGES/toolbox-connect.png)

Once connected. select the "Program" button. Browse your computer for the file and select send to load the file...

![toolbox-send-code.png](/IMAGES/toolbox-send-code.png)

## **ADDITIONAL RESOURCES:**

- [Cisco Room Controls Design Guide](https://www.cisco.com/c/dam/en/us/td/docs/telepresence/endpoint/ce915/sx-mx-dx-room-kit-boards-customization-guide-ce915.pdf)
- [Cisco RoomOS API References](https://roomos.cisco.com/xapi)
