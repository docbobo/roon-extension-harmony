## Controlling Logitech Harmony from Roon

In my current living room setup, I am using a Logitech Harmony remote control to control all my devices. This means that there are "Activities" like "Watch TV", "Play Games", and also "Listen to Music". Since I am lazy, I didn't want to use both the Harmony remote control as well as Roon to control my audio equipment...

## Source Control

Roon offers an extension that is called "Source Control", which allows Roon to control external devices to a certain degree. Mainly, switching the input of such a controlled device and putting it into standby.

This extension exposes each of the "Activities" registered on the Harmony as its own Source Control extension. In my case, there are extensions for "Watching TV", "Play Games", and "Listen to Music". Each of those extensions can be bound to a specific output zone - in my case "Living Room". The result is exactly what I was looking for: if I am watching TV and press the play button in Roon, the TV is turned off, the AV receiver switches its input, and Roon starts to play. In addition, if I am using the Harmony remote control to turn off everything, Roon stops its playback.

## Installation

1. Install Node.js from https://nodejs.org.

   * On Windows, install from the above link.
   * On Mac OS, you can use [homebrew](http://brew.sh) to install Node.js.
   * On Linux, you can use your distribution's package manager, but make sure it installs a recent Node.js. Otherwise just install from the above link.

   The extension has been developed with Node v8.0.0. While it may work with older versions, it's not something that I've tested.

1. Install Git from https://git-scm.com/downloads.
   * Following the instructions for the Operating System you are running.

1. Download the Logitech Harmony extension.

   * Go to the [roon-extension-harmony](https://github.com/docbobo/roon-extension-harmony) page on [GitHub](https://github.com).
   * Click the green 'Clone or Download' button and select 'Download ZIP'.

1. Extract the zip file in a local folder.

1. Change directory to the extension in the local folder:
    ```
    cd <local_folder>/roon-extension-harmony
    ```
    *Replace `<local_folder>` with the local folder path.*

1. Install the dependencies:
    ```bash
    npm install
    ```

1. Run it!
    ```bash
    node .
    ```

    The extension should appear in Roon now. See Settings->Setup->Extensions and you should see it in the list.

## Notes

* Setups with more than one Roon Core on the network are not currently tested.
