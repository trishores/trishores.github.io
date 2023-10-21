+++
title = "lightbeam over lava"
subtitle = "sample animation for elektra simulator"
date = "2018-10-05"
+++

This animation uses 50 threads: 1 for launch, 4 for the lava background, and 45 for the lightbeam overlay. The lightbeam overlay has the highest z-order to make it topmost.

&nbsp;![Loading animation...](/img/lightbeamLava_350.gif)

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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Color defines:</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>16</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>25</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
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
launches 2 functions then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>start&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
mandatory function name for code launch.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> &nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLava </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>zOrder</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
launch function asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLightbeam </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>(</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>zOrder</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>)</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
launch function asynchronously (top animation).</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Asynchronously
launches 3 functions at staggered intervals then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLava</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 400</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaInnerRing&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
launch function asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 400</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaMiddleRing&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// launch
function asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 400</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaEdgeRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles inner-ring colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaInnerRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>       </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> innerLeds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles middle-ring colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaMiddleRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>       </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> middleLeds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles edge-ring colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaEdgeRing</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>        </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> edgeLeds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Periodically
runs the directional lightbeam animations.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLightbeam</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                     </span><span style='font-size:10.5pt;font-family:
Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>call</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeam&nbsp;&nbsp;&nbsp;&nbsp;   
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function synchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>call</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeam  
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function synchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>call</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeam&nbsp;&nbsp;   
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function synchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>call</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeam   
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function synchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                     </span><span style='font-size:10.5pt;font-family:
Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Illuminates
vertical lightbeam path then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeam</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep1 
      </span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Illuminates
horizontal lightbeam path then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeam</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep1&nbsp;&nbsp;&nbsp;&nbsp; 
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Illuminates
diagonalLeft lightbeam path then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeam</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep1&nbsp;&nbsp; 
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Illuminates
diagonalRight lightbeam path then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeam</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep1&nbsp; 
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
call function asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Functions that
pulse LED(s) along the vertical lightbeam path.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep1</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>13</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>11</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>14</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>19</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>3</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>6</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>15</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>18</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>7</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>9</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>8</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcVerticalLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>16</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>17</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Functions that
pulse LED(s) along the horizontal lightbeam path.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep1</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>14</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>15</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>6</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>7</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>13</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>16</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>3</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>8</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>17</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>9</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>11</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcHorizontalLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>18</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>19</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Functions that
pulse LED(s) along the diagonal-left lightbeam path.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep1</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>15</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>16</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>7</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>6</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>8</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>14</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>17</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>9</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>3</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>13</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>18</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>11</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalLeftLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>19</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Functions that
pulse LED(s) along the diagonal-right lightbeam path.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep1</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>17</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>18</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>9</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>10</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>8</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>16</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>19</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep6</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>11</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>4</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>7</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep7</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>3</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep8</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>15</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep9</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>6</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep10</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>5</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcDiagonalRightLightbeamStep11</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>13</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>14</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> white </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal>&nbsp;</p>

</div>

</body>

</html>
