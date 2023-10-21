+++
title = "matrix lava"
subtitle = "sample animation for matrix 10x10 simulator"
date = "2018-11-25"
+++

This animation uses 7 threads: 1 for launch and 6 for the lava background.

&nbsp;![Loading animation...](/img/matrixLava10x10_350.gif)

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
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Matrix simulator</span></p>

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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>simulator-matrix-10x10</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>100</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>100</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring1Leds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>45</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>46</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>55</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>56</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring2Leds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>34-37</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>44</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>47</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>54</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>57</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>64-67</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring3Leds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>23-28</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>33</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>38</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>43</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>48</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>53</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>58</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>63</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>68</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>73-78</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring4Leds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>12-19</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>22</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>29</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>32</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>39</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>42</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>49</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>52</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>59</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>62</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>69</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>72</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>79</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>82-89</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring5Leds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1-11</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>20</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>21</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>30</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>31</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>40</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>41</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>50</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>51</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>60</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>61</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>70</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>71</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>80</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>81</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>90-100</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>]'</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>define</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> allLeds </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>=</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>'[</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>1-100</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>127</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>128</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>155</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>100</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>127</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>0</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>,</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>128</span><span
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
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Asynchronously
launches 1 function then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>start                       
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
mandatory function name for code launch.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLava      </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// launch function
asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Asynchronously
launches 5 functions at staggered intervals then exits.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLava</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> allLeds off </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 800</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing1                </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// launch function
asynchronously.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 300</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>                            
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
tickIntervalMillisecs multiple (3 * 50ms =&gt; 150ms).</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 300</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 300</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>pause</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 300</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>ms</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>callAsync</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles ring1 colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing1</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring1Leds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>       </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring1Leds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring1Leds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring1Leds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring1Leds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring1Leds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles ring2 colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing2</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring2Leds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>       </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring2Leds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring2Leds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring2Leds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring2Leds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring2Leds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> start_tag                              
</span><span style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>//
loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles ring3 colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing3</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring3Leds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>       </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition led(s)
color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring3Leds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring3Leds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring3Leds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring3Leds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring3Leds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> start_tag                               </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// loop back to
bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles ring4 colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing4</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring4Leds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>       </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring4Leds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring4Leds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring4Leds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring4Leds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring4Leds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// Continuously
cycles ring5 colors.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>@</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>funcLavaRing5</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>here</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// set bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring5Leds red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>       </span><span
style='font-size:10.5pt;font-family:Consolas;color:#6A9955'>// transition
led(s) color.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring5Leds orange </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring5Leds yellow </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring5Leds green </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring5Leds blue </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>glowRamp</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> ring5Leds purple </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>to</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> red </span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>in</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'> 2</span><span
style='font-size:10.5pt;font-family:Consolas;color:#B5CEA8'>s</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>    </span><span
style='font-size:10.5pt;font-family:Consolas;color:#569CD6'>goto</span><span
style='font-size:10.5pt;font-family:Consolas;color:#CE9178'>:</span><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>
start_tag                               </span><span style='font-size:10.5pt;
font-family:Consolas;color:#6A9955'>// loop back to bookmark.</span></p>

<p class=MsoNormal style='line-height:14.25pt;background:#1E1E1E'><span
style='font-size:10.5pt;font-family:Consolas;color:#D4D4D4'>&nbsp;</span></p>

<p class=MsoNormal>&nbsp;</p>

</div>

</body>

</html>
