+++
title = "Glow OS"
subtitle = "embedded operating system for smart LED devices"
date = "2018-10-05"
desc = "embedded os for smart LED devices"
+++

[Glow operating system](https://github.com/ledmakerspace/ElektraFW-SAMD21E18A), written in C, is optimized for embedded devices driving smart LED strips.
<br><br>
<!--more-->

## **Features**

* Receives binary animation data sent over USB.

* Stores binary animation data in SRAM or ROM based on the `saveToRom` parameter in your glowscript.

* Services play/stop/resume commands sent over USB.
  
* Dynamically decodes binary animation data into LED strip color data.