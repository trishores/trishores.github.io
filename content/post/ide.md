+++
title = "Glow IDE"
subtitle = "integrated development environment"
date = "2018-10-07"
+++

Microsoft's free cross-platform open-source [Visual Studio Code](https://code.visualstudio.com/) editor together with the free open-source [Glow IDE](https://marketplace.visualstudio.com/items?itemName=ledmakerorg.glow-ide#overview) extension provides an all-in-one editor, compiler, and simulator to create and view animations.

<!--more-->

Refer to the [Install](/post/ide#install_id) and [Usage](/post/ide#usage_id) sections below to start creating animations.

<br>

## **IntelliSense features**

* Syntax coloring to provide at-a-glance syntax validation.
* Auto-closing brackets & quotes.
* Code snippets to rapidly insert commands.

<img style="float:left;margin-top:15px;" src="/img/editor.png" /><br clear="both"/>

<br>

## **Compiler features**

* Generates binary output interpretable by devices running [Glow OS](/post/os/).
* Line-specific warning/error messages.
* Checks the rom/ram/thread usage of your animation.

`Starting build...`<br>
`Device threads usage: 19.5% (50 of 256 threads).`<br>
`Device RAM usage: 2.4% (608 of 25,000 bytes).`<br>
`Device ROM usage: 1.3% (2,624 of 200,000 bytes).`<br>
`Build completed successfully.`

<br>

## **Simulator features**

* Integrated within [Visual Studio Code](https://code.visualstudio.com/).
* LED layout is specified in a customizable [svg](https://www.w3schools.com/graphics/svg_intro.asp).

<img style="float:left;margin-top:15px" src="/img/lightbeamLava_200.gif" />
<img style="float:left;margin-top:15px;margin-left:15px" src="/img/matrixLava10x10_200.gif" /><br clear="both"/>

<br>

## **Cross-platform**

[Glow IDE](https://marketplace.visualstudio.com/items?itemName=ledmakerorg.glow-ide#overview) extension is a cross-platform project for Linux, Windows 7, Windows 8.1, Windows 10.

<div id="system_id" style="display:block;position:relative;top:-50px; visibility:hidden;margin-bottom:50px;"></div>

## **Minimum system requirements**

* 2 GHz dual core processor.
* 8 GB system memory.
* 64-bit operating system.

<div id="install_id" style="display:block;position:relative;top:-50px; visibility:hidden;margin-bottom:50px;"></div>

## **Install**

1. If you haven't already, download and install Microsoft's [Visual Studio Code](https://code.visualstudio.com/) editor.
1. On Microsoft's [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=ledmakerorg.glow-ide) Glow IDE page, click on the **Install** button and follow installation instructions.

<div id="usage_id" style="display:block;position:relative;top:-50px; visibility:hidden;margin-bottom:50px;"></div>

## **Usage**

Refer to this <a target="_self" href="/tutorial/installation.mp4">tutorial</a> or the directions below:

1. Open the Visual Studio Code editor.
1. Type **Ctrl+Alt+S** to open the glowscript samples folder.
1. Several glowscript files (ending with .glows) are listed. Each contains code for a different animation. Double-click a glowscript filename to load it into the editor. When the glowscript file is fully loaded (takes a few seconds) a **Build** button will appear in the [status bar](https://code.visualstudio.com/docs/getstarted/userinterface).
1. Click the **Build** button to compile the glowscript file (takes a few seconds). On completion, the build status and any compilation warnings/errors will be displayed in the [panel](https://code.visualstudio.com/docs/getstarted/userinterface). On successful build, **Play**, **Stop** and **Resume** buttons appear in the [status bar](https://code.visualstudio.com/docs/getstarted/userinterface).
1. Click the **Play** button to run the glowscript code in the simulator.
1. Change existing glowscript files (e.g. modify colors), or create new animations (see [Glowscript syntax](/post/script/)).

<br>

## **Notes**

* Depending on the animation complexity, the simulator may stutter/delay/not-render if your computer's processor speed or memory is insufficient. Troubleshoot by running *test.glows* to confirm whether a basic animation will render. For more complex animations, glowscript's `tickIntervalMillisecs` value can be increased to reduce CPU load. however, the time values in your animation code will probably need to be adjusted since they must be a multiple of the `tickIntervalMillisecs` value.
* LED color gamma correction is not yet supported.
* Animation code stepping is not yet supported.
* On Linux only: compiler & simulator executables will by default not have execute permission. To grant execute permissions, run the following commands in a linux terminal:<br>
    `chmod +x ~/.vscode/extensions/ledmakerorg.glow-ide-0.0.3/lib/compiler/linux/x64/glow-compiler`<br>
    `chmod +x ~/.vscode/extensions/ledmakerorg.glow-ide-0.0.3/lib/simulator/linux/x64/simulator-elektra-20`<br>
    `chmod +x ~/.vscode/extensions/ledmakerorg.glow-ide-0.0.3/lib/simulator/linux/x64/simulator-matrix-10x10`