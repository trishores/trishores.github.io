+++
title = "bicycle rear light"
subtitle = "sample animation for elektra simulator"
date = "2018-10-05"
+++

This animation uses 4 threads: 1 for launch and 1 for each LED ring. Full-on and side-mounted LEDS on the Elektra LED development board provide a wide viewing angle for this animation.

&nbsp;![Loading animation...](/img/bicycle_rear_light_350.gif)

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

<p class=MsoNormal>&nbsp;</p>

</div>

</body>

</html>
