---
layout: page
ketex: true
---

**Line Scan Microscopy**  
{: style="color:gray; font-size:210%; text-align: left; font-family:"Goudy Old Style"; margin-top:-35px; margin-bottom:0px" }
---delocalized, efficient microscopic imaging 
{: style="color:gray; font-size:160%; text-align: right; font-family:"Goudy Old Style"; margin-bottom:10px"}
--------------------------------------------------------
{: style="height:2px; color:#d0d0d0; background-color:#d0d0d0; margin-bottom:15px"}


![fig1](/assets/fig_probe_closeup2.png)
*Closeup side view of a lab-made line probe near sample with glued specimen.*
{: style="float:right; height:27%; width:27%; margin:4px 0 0 10px; font-size: 60%"}

We study the use of line probe in microscopy for structured signal. Unlike the conventional use of point probe, by which the scanning probe microscopy takes pointwise samples; each of the line probe measurement is  accumulated electric current generated between the contact surface of line shaped probe and sample. The line probe measurements are <b> delocalized </b> and hence more <b>efficient</b>, reducing the scanning time for structured signal by orders of magnitude.

Here, we will study it in the context of a particular microscopy modality known as *scanning electrochemical microscopy* (SECM).


## Imaging Modality ##

### Chemical Probe  ###

<div style="float:right; font-size:55%; width:27%; margin:4px 0 0 10px">
	<img style="border:1px solid gray" src="/assets/probe_sideview.png">
	<i> Redox reaction between probe and sample.</i>
</div>

The SECM line probe measures the redox reaction between the probe and the electroactive parts of the sample. The line probe consists of a thin conductive layer (dark gray) sandwiched by two insulating layers (light gray). The sensitive area between probe and sample is a thin line of width $t_E$. The distance $d_m$ between the probe and sample is stable by keeping contacting angle $\theta_{\text{CLP}}$ the same though out the scanning procedure.

During a single measurement, a negative potential is applied to the probe end, induces redox reaction near the sensitive part of sample. This produces an influx of negative charge current.

<br/>

### Line Scan ###

<div style="float:right; font-size:55%; width:27%; margin:0px 0 0 10px">
	<img src="/assets/fig_single_scan.png">
	<i> Redox reaction between probe and sample.</i>
</div>

The line probe (gray) "sweeps" through the sample (green and yellow) in a predefined direction (arrow). The contact surface between probe and sample constitutes a straight line, from which the line probe measures the integrated current as a single measurement. 

The line probe takes equispaced steps in its proceeding direction, generates a *line scan* (orange),  as the function from steps distance to electric currents.


<br/>

### Schematic ###

The full microscopic scanning procedure consists of multiple line scans. After a line scan sweep finishes, the sample is rotated by an assigned angle, then another line scan proceeds; this scanning procedure repeats until required amount of line scan measurements are obtained.

The final microscopic image is reconstructed via these line scan measurements. 

![](/assets/schematic.png)

### Related Modalities ###


## Simulation Package ##

### Reconstruction Algorithm ###

### Code ###

The solver of short-and-sparse deconvolution (Matlab) can be downloaded from the following github link: 

<https://github.com/clpsecm/clpsecm_imaging>
{:style="text-align:center"}




## Resources ##





-------------------------------------------------------
{: style="height:2px; color:#aaa; background-color:#aaa; margin-top: 3em; margin-bottom:-0.2em"}

#### References ####

{:.ref}
[1]. Hubel, David H., and Torsten N. Wiesel. "Receptive fields of single neurones in the cat's striate cortex." *The Journal of physiology* 148.3 (1959): 574-591.




