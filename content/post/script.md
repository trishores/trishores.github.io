+++
title = "Glowscript"
subtitle = "asynchronous programming language"
date = "2018-10-06"
desc = "asynchronous programming language"
+++

Glowscript is a simple yet powerful asynchronous multithreaded [procedural](https://en.wikipedia.org/wiki/Procedural_programming) programming language for creating multilayered (superimposed) animations on smart LED strips, such as [DotStars](https://learn.adafruit.com/adafruit-dotstar-leds/overview) and [NeoPixels](https://www.adafruit.com/category/168).

<!--more-->

<p style="margin-top:40px"></p>

---

<p style="margin-top:30px"></p>

## **Features**

* A single glowscript program can run 256 independent animation threads and drive over 1000 LEDs.

* LEDs can be grouped and assigned to multiple animation threads to create complex light patterns.

* Animation z-ordering allows superimposed animations.

* Timing instructions permit LED color changes as rapidly as every millisecond or as slowly as every month.

* Color data compression reduces complex animations to a compact footprint.

<p style="margin-top:40px"></p>

---

<p style="margin-top:30px"></p>

## **Syntax**
<br>
**glowImmediate**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>glowImmediate: [led1,led2,...] color</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Instantly sets the color of the specified LEDs.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>glowImmediate: [led5] green</code></td>
    </tr>
    <tr>
      <td><i>e.g. 2</i></td>
      <td><code>glowImmediate: [led1,led2,led7] red</code></td>
    </tr>
  </tbody>
</table>

**glowRamp**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>glowRamp: [led1,led2,...] color1 to color2 in timeDuration</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Instantly sets color1 on the specified LEDs, then transitions color1 to color2 over the specified time duration.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>glowRamp: [led15,led4] green to blue in 100ms</code></td>
    </tr>
    <tr>
      <td><i>e.g. 2</i></td>
      <td><code>glowRamp: [led19] red to orange in 5s</code></td>
    </tr>
  </tbody>
</table>

**pause**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>pause: duration</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Pause current thread for the specified duration. Time units can be milli-seconds, seconds, minutes, hours, or ticks. Minimum pause duration is 1 millisecond. Maximum pause duration is 1080 hours (45 days). The pause duration must be a multiple of the <code>device:tickIntervalMillisecs</code> parameter value, which is the time interval between animation update cycles.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>pause: 5ms</code></td>
    </tr>
    <tr>
      <td><i>e.g. 2</i></td>
      <td><code>pause: 30s</code></td>
    </tr>
    <tr>
      <td><i>e.g. 3</i></td>
      <td><code>pause: 20m</code></td>
    </tr>
    <tr>
      <td><i>e.g. 4</i></td>
      <td><code>pause: 1h</code></td>
    </tr>
    <tr>
      <td><i>e.g. 5</i></td>
      <td><code>pause: 40t</code></td>
    </tr>
  </tbody>
</table>

**here**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>here: bookmarkName</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Bookmark a location in the current function.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>here: strobeStart</code></td>
    </tr>
  </tbody>
</table>

**goto**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>goto: bookmarkName</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Jump to a bookmark in the current function.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>goto: strobeStart</code></td>
    </tr>
  </tbody>
</table>

**call**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>call: @targetFunction</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Synchronously runs the target function (current function pauses until the target function completes). The z-order is 0 and cannot be modified.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>call: @redStrobeFunction</code></td>
    </tr>
  </tbody>
</table>

**repeat**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>call: @targetFunction (repeat=N)</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Synchronously runs the target function N times (current function pauses until all repetitions of the target function completes). Using the repeat parameter is optional. Minimum repeat value is 1 (same as omitting repeat parameter). Maximum repeat value is 2 billion. Repeat is used in conjuction with the <i>call</i> instruction.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>call: @redStrobeFunction (repeat=50)</code></td>
    </tr>
  </tbody>
</table>

**callAsync**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>callAsync: @targetFunc</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Asynchronously runs the target function (current function continues immediately after launching the target function). The <code>callAsync</code> instruction can be nested at any level of your code.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>callAsync: @blueStrobeFunc</code></td>
    </tr>
  </tbody>
</table>

**zOrder**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>callAsync: @targetFunc (zOrder=N)</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Asynchronously runs the target function with a z-order of N (current function continues immediately after launching the target function). When different animation functions act on the same LED(s), the function with the highest z-order controls the LED(s). If threads have the same z-order, then the last-launched thread wins. Z-order values do not need to be consecutive as the compiler uses them as relative values. Using the z-order parameter is optional. Minimum z-order value is 0 (default z-order parameter). Maximum z-order value is 1000. Z-order is used in conjuction with the <i>callAsync</i> instruction.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>callAsync: @blueStrobeFunc (zOrder=2)</code></td>
    </tr>
    <tr>
      <td><i>e.g. 2</i></td>
      <td><code>callAsync: @lightBeamFunc (zOrder=35)</code></td>
    </tr>
  </tbody>
</table>

**define**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>define: alias=&#39;value&#39;</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Sets a user-friendly alias for the specified string value. This helps with readability and code-maintenance.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>define: strobeLeds=&#39;[2,3,4,5,9]&#39;</code></td>
    </tr>
    <tr>
      <td><i>e.g. 2</i></td>
      <td><code>define: purple=&#39;(255,0,255,1)&#39;</code></td>
    </tr>
  </tbody>
</table>

**comments**<br>
<table>
  <tbody>
    <tr>
      <td>syntax</td>
      <td><b>//</b></td>
    </tr>
    <tr>
      <td>action</td>
      <td>Add a single-line comment.</td>
    </tr>
    <tr>
      <td><i>e.g. 1</i></td>
      <td><code>// this is a comment line</code></td>
    </tr>
  </tbody>
</table>

<br>
**Specifying LEDs**<br>
LEDs are specified by their numeric position from the start of the LED strip (i.e. `1`,`2`,`3` and so on) in the following format: [1,2,3] or [1-3] or [1,2-3]).

**Specifying colors/brightness**<br>
A color is specified by its red value (0-255), green value (0-255), blue value (0-255), & brightness value (0-31) in the following format: `(redVal, greenVal, blueVal, brightVal)`.

**Case sensitivity**<br>
Glowscript is case-insensitive.

<p style="margin-top:40px"></p>

---

<p style="margin-top:30px"></p>

## **Animation Examples**

<p style="margin-top:40px;font-size:1.2em;"><b>Synchronous Code Example</b></p>

Synchronous code executes sequentially and each code instruction completes before the next one is executed. This basic code sample uses synchronous code to toggle all LEDs on and off in a continuous loop.

<img style="float:left;margin-left:0px;" src="/img/simpleBeacon_350.png" /><br clear="both"/>

<html>

<head>
<meta http-equiv=Content-Type content="text/html; charset=utf-8">
<meta name=Generator content="Microsoft Word 14 (filtered)">
<style>
<!--
 /* Font Definitions */
 @font-face
	{font-family:Calibri;
	panose-1:2 15 5 2 2 2 4 3 2 4;}
@font-face
	{font-family:Consolas;
	panose-1:2 11 6 9 2 2 4 3 2 4;}
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{margin:0in;
	margin-bottom:.0001pt;
	font-size:11.0pt;
	font-family:"Calibri","sans-serif";}
.MsoChpDefault
	{font-family:"Calibri","sans-serif";}
@page WordSection1
	{size:8.5in 11.0in;
	margin:1.0in 1.0in 1.0in 1.0in;}
div.WordSection1
	{page:WordSection1;}
-->
</style>

</head>

<body lang=EN-US>

<div class=WordSection1>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// DEVICE
PARAMETERS (modify with care)</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Elektra
simulator</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>name</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>simulator-elektra-20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>type</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>sim</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>tickIntervalMillisecs</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>     </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// increase to
reduce CPU load.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>protocolVersion</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1.0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ledCount</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ramSpaceBytes</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25000</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>          </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set an animation
size limit in memory.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>romSpaceBytes</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>200000</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>         </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set an animation
size limit on disk.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// DEFINES (modify
as needed)</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// LED defines:</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1-4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// alias for
inner-ring leds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5-12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>13-20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> allLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1-20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Color defines:</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>250</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>250</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>250</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>165</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>255</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// CODE</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
loops.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Each loop cycle
has a 1.5 second duration.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>start&nbsp;&nbsp;                          
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
mandatory entry-point function name.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag1               </span><span style='font-size:10.5pt;font-family:Consolas;
color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> allLeds yellow  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set all LEDs to
yellow.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 750</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                   </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// pause for 750
milliseconds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> allLeds off     </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// turn all LEDs
off.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 750</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                   </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// pause for 750
milliseconds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag1               </span><span style='font-size:10.5pt;font-family:Consolas;
color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

</div>

</body>

</html>

The *DEVICE PARAMETERS* section should not normally be modified. 
The *DEFINES* section specifies the label `allLeds` as an alias for all 20 LEDS (to make CODE section instructions more readable). Most defines are unused and can be deleted. Further defines may be added as necessary.

The *CODE* section contains executable instructions organized in functions. In this example, only a single function exists, which is the mandatory `@start` function. `@start` executes its code instructions in a continuous synchronous loop of 1.5 seconds duration. During each loop cycle, all LEDs turn on for 750ms then turn off for 750ms. The final `goto` instruction ensures that the code continuously loops, otherwise the simulation will terminate after the first animation cycle.

<p style="margin-top:40px;font-size:1.2em;"><b>Asynchronous Code Example</b></p>

Asynchronous code can execute in parallel with other code. A CPU with one core executing multiple threads achieves asynchronous code execution. A CPU with multiple cores each executing a single thread also achieves asynchronous code execution. This asynchronous code sample uses 4 threads: 1 for the `@start` function, and 1 for each LED ring.

<img style="float:left;margin-left:0px;" src="/img/bicycle_rear_light_350.gif" /><br clear="both"/>

Glowscript:
<html>

<head>
<meta http-equiv=Content-Type content="text/html; charset=utf-8">
<meta name=Generator content="Microsoft Word 14 (filtered)">
<style>
<!--
 /* Font Definitions */
 @font-face
	{font-family:Calibri;
	panose-1:2 15 5 2 2 2 4 3 2 4;}
@font-face
	{font-family:Consolas;
	panose-1:2 11 6 9 2 2 4 3 2 4;}
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{margin:0in;
	margin-bottom:.0001pt;
	font-size:11.0pt;
	font-family:"Calibri","sans-serif";}
.MsoChpDefault
	{font-family:"Calibri","sans-serif";}
@page WordSection1
	{size:8.5in 11.0in;
	margin:1.0in 1.0in 1.0in 1.0in;}
div.WordSection1
	{page:WordSection1;}
-->
</style>

</head>

<body lang=EN-US>

<div class=WordSection1>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// DEVICE (modify
with care)</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Elektra
simulator</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>name</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>simulator-elektra-20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>type</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>sim</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>tickIntervalMillisecs</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>     </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// increase to
reduce CPU load.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>protocolVersion</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1.0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ledCount</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ramSpaceBytes</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25000</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>          </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set an animation
size limit in memory.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>device</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>romSpaceBytes</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>200000</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>         </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set an animation
size limit on disk.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// DEFINES (modify
as needed)</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// LED defines:</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1-4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// alias for
inner-ring leds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5-12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>13-20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> allLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1-20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Color defines:</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> turquoise </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>30</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// CODE</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Simultaneously
launches 3 functions then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>start                            
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
mandatory entry-point function name.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>strobeInnerRing    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// launch function
asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>pulseMiddleRing     </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// launch function
asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>strobeEdgeRing     </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// launch function
asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
runs inner-ring light strobe. Each loop cycle has a 1-second duration.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>strobeInnerRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                     </span><span style='font-size:10.5pt;font-family:
Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds
red        </span><span style='font-size:10.5pt;font-family:Consolas;
color:#6A9955'>// set led(s) to red.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>call</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>flashInnerRing </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>repeat</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// synchronously
call function 5 times.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 500</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                       
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
pause for 500 milliseconds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> start_tag                     </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// loop back to
bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Flashes
inner-ring LED(s) once then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>flashInnerRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                   
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
pause for 50 milliseconds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds off   </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// turn led(s) off.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds red   </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set led(s) to
red.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Pulses
middle-ring LED(s) in a continuous loop. Each loop cycle has a 1-second
duration.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>pulseMiddleRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                          </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 500</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// gradually
brighten led(s) to red.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 500</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set led(s) to
red then fade off.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                          </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
runs edge-ring light strobe. Each loop cycle has a 1-second duration.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>strobeEdgeRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                     </span><span style='font-size:10.5pt;font-family:
Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds
off         </span><span style='font-size:10.5pt;font-family:Consolas;
color:#6A9955'>// set led(s) to off.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 500</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                       
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
pause for 500 milliseconds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>call</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>flashEdgeRing </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>repeat</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>     </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// synchronously
call function 5 times.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                     </span><span style='font-size:10.5pt;font-family:
Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Flashes
edge-ring LED(s) once then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>flashEdgeRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                        
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
pause for 50 milliseconds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds
off         </span><span style='font-size:10.5pt;font-family:Consolas;
color:#6A9955'>// turn led(s) off.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                        
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
pause for 50 milliseconds.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowImmediate</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds
red         </span><span style='font-size:10.5pt;font-family:Consolas;
color:#6A9955'>// set led(s) to red.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

</div>

</body>

</html>

Code execution begins with the mandatory `@start` function, which simultaneously launches 3 functions (`@strobeInnerRing`, `@pulseMiddleRing`, `@strobeEdgeRing`) before exiting. The 3 functions execute in parallel as described below:

- `@strobeInnerRing` executes in a continuous synchronous loop of 1-second duration. During each loop cycle, all inner ring LEDs strobe on-off rapidly for 500ms (through repeated synchronous calls to the `@flashInnerRing` function), then are steady on for 500ms.

- `@strobeEdgeRing` executes in a continuous synchronous loop of 1-second duration. During each loop cycle, all edge ring LEDs are off for 500ms, then strobe on-off rapidly for 500ms (through repeated synchronous calls to the `@flashEdgeRing` function).

- `@pulseMiddleRing` executes in a continuous synchronous loop of 1-second duration. During each loop cycle, all middle ring LEDs gradually transition from off to red in 500ms, then gradually transition from red to off in 500ms.

<p style="margin-top:40px"></p>

---

<p style="margin-top:30px"></p>

See [animation samples](/sample/spinner/) for further usage examples.