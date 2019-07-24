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

In a single measurement, a negative potential is applied to the probe end, induces redox reaction near the sensitive part of sample. This produces an influx of negative charge current.


### Line Scan ###

<div style="float:right; font-size:55%; width:27%; margin:0px 0 0 10px">
	<img src="/assets/fig_single_scan.png">
	<i> Redox reaction between probe and sample.</i>
</div>

The line probe (gray) "sweeps" through the sample (green and yellow) in a predefined direction (arrow). The contact surface between probe and sample constitutes a straight line, from which the line probe measures the integrated electric current as a single measurement. 

The line probe takes equispaced steps in its proceeding direction, generates a *line scan* (orange),  as the function from steps distance to electric currents.


### Schematic ###

The full microscopic scanning procedure is comprised of multiple line scans. After a line scan sweep finishes, the sample is rotated by an assigned angle, then another line scan proceeds; this scanning procedure repeats until required amount of line scan measurements at different angles are obtained.

The final microscopic image is reconstructed via these line scan measurements. 

![](/assets/schematic.png)
<figcaption>Schematic of scanning microscope with line probe. After the scan angles are assigned, the line probe sweep through the sample as it is rotated at different angle, generates multiple line scans. The final microscopic image is constructed from these line scans via algorithmic approach. </figcaption>



### Related works ###

The microscopic line scans as an imaging methodology is closely related to **tomography** [[1]](/pages/intro_clp#references). 


## Experiment Demo ##

We begin this study on a dataset with strong structure, in which the samples consist some number of small particles. This is an image modality appears in applications related to  microscopy  [[2]](/pages/intro_clp#references), [[3]](/pages/intro_clp#references). We assume the image of particles $\mathbf Y = \mathbf D*\mathbf X$ is the convolution of a known particle function $\mathbf D\in  L[\mathbb R^2]$ with  location with map $\mathbf X$. The $m$-line scans of image $\mathbf Y$ generates lines $\mathbf R$ as

\\[  \mathbf R = \mathcal S[\mathbf \psi * \mathcal L_{\Theta}[\mathbf D*\mathbf X]],  \\]

where $\mathcal S$ is the sampling operator, $\mathbf \psi$ is the  point spread function (PSF) of a line scan, and $\mathcal L_{\Theta}$ is line projections with respect to  angles $\Theta$.


### Reconstruction Algorithm ###
Image reconstruction from line scans under this scenario can be cast as finding the unknown location $\mathbf X$, which is a well understood sparse recovery problem. Due to physical limitation, we only have partial information for PSF $\mathbf \psi$, therefore we solve for $\mathbf X$ while simultaneously calibrate $\mathbf \psi(p)$ with parameters $p$

\\[ \min_{p,\mathbf X} \lambda\lVert\mathbf X\rVert_1 + \tfrac12 \lVert\mathcal S[\mathbf \psi(p) * \mathcal L_{\Theta}[\mathbf D*\mathbf X]] - \mathbf R\rVert_2^2 \tag{1}\\]


The algorithm (1) serves as a good cornerstone for the reconstruction method; it is advised to modify (1) accordingly to accommodate several properties of line scans to achieve satisfactory image reconstruction results.  


### Demo ###

We demonstrate an example of scan line image reconstruction from lab made SECM microscope. The top row compares the image from of point probe and line probe over a sample with 3 particles. The bottom row shows the result of line probe over a larger sized sample with 10 particles. Image resolution is $10\mu m$ per pixel. 

![](/assets/fig_demo.png)
*Top row: 3 particle sample. Bottom row: 10 particle sample. Image pixel width/height are $10\mu m $.*
{: style="width:80%; align:center; margin-left:auto; margin-right: auto; font-size: 60%"}



## Resources ##


### Selected Papers ###

[Compressed Sensing Microscopy with Scanning Line Probes](/assets/neurips_2019.pdf)
{:.title}
 **Han-wen Kuo**, Anna E. Dorfi, Daniel V. Esposito, John Wright, 
{:.author}
In review, 2019
{:.booktitle}

<span class="glyphicon glyphicon-download-alt"></span><span style="margin-right:5px"><a role="button" href="/assets/neurips_2019.pdf" > preprint </a></span> <span class="glyphicon glyphicon-paperclip"></span>
<span style="margin-right:5px"><a role="button" onclick="toggle_block('bibtex-csclp-long')" >bibtex</a></span><span class="glyphicon glyphicon-picture"></span> <span style="margin-right:5px"><a role="button" href="/assets/poster_secmclp.pdf">poster</a></span>

<div id="bibtex-csclp-long" class="bibtex">
@article{kuo2019compressed,
  title={Compressed Sensing Microscopy with Scanning Line Probes},
  author={Kuo, Han-Wen and Dorfi, Anna E. and Esposito, Daniel V. and Wright, John},
  journal={Preprint},
  year={2019}
}
</div>


[Scanning Line Probe Microscopy: Beyond the Point Probe](https://pubs.acs.org/doi/pdf/10.1021/acs.analchem.8b02852)
{:.title}
Glen D O’Neil, **Han-Wen Kuo**, Duncan N. Lomax, John Wright, Daniel V. Esposito
{:.author}
Analytical chemistry, 2018
{:.booktitle}

<span class="glyphicon glyphicon-download-alt"></span><span style="margin-right:5px"><a role="button" href="/assets/acs.analchem.8b02852.pdf"> paper </a></span> <span class="glyphicon glyphicon-paperclip"></span>
<span><a role="button" onclick="toggle_block('bibtex-scanning')" >bibtex</a></span>

<div id="bibtex-scanning" class="bibtex">
@article{oneil2018scanning,
  title={Scanning Line Probe Microscopy: Beyond the Point Probe},
  author={O’Neil, Glen D and Kuo, Han-wen and Lomax, Duncan N. and Wright, John and Esposito, Daniel V.},
  journal={Analytical chemistry},
  volume={90},
  number={19},
  pages={11531--11537},
  year={2018},
  publisher={ACS Publications}
}
</div>


### Code Package ###

The package for both simulation and real data reconstruction for microscopic line scans (Matlab) can be downloaded via the following github link: 

<https://github.com/clpsecm/clpsecm_imaging>
{:style="text-align:center"}



-------------------------------------------------------
{: style="height:2px; color:#aaa; background-color:#aaa; margin-top: 3em; margin-bottom:-0.2em"}

#### References ####

{:.ref}
[1]. G. T. Herman, Fundamentals of computerized tomography: image reconstruction from projections. *Springer Science & Business Media*, 2009.

{:.ref}
[2]. M. E. Davis, J. E. Zuckerman, C. H. J. Choi, D. Seligson, A. Tolcher, C. A. Alabi, Y. Yen, J. D. Heidel, and A. Ribas, Evidence of rnai in humans from systemically administered sirna via targeted nanoparticles, *Nature*, vol. 464, no. 7291, p. 1067, 2010.

{:.ref}
[3]. C. A. S. Batista, R. G. Larson, and N. A. Kotov, “Nonadditivity of nanoparticle interactions”, *Science*, vol. 350, no. 6257, p. 1242477, 2015.



