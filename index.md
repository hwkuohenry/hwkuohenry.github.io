---
layout: page
ketex: true
---

<!-- ![](/assets/profile-color.jpg)
Photoed in 2018 watching champions league final (in Liverpool FC supporter's pub).
{:style="float:right; width:26%; margin:5px 10px 10px 15px; font-size:50%; font-style:italic"}
 -->

*Hi! I am Henry,...* <br />
an ML scientist with PhD form Columbia University advised by professor [John Wright](http://www.columbia.edu/~jw2966/) and involved in active research with professor [Daniel Esposito](https://cheme.columbia.edu/faculty/daniel-esposito). My research is focused on developing and understanding methodologies for data analysis, I am specifically interested in analyzing machine learning algorithms for scientific or visual data processing, and understanding effective optimization methods in large scale.

*My projects...* <br />
during my graduate study involved building [mathematical understanding toward deconvolution problems](https://deconvlab.github.io), which is a challenging, recurrent, and long-standing problem in engineering and science; in addition I conducted interdisciplinary research with chemistry department on [efficient microscopic imaging](/pages/intro_clp) in which we built a novel microscope that accellerate the scanning speed many times faster. Technically speaking, these projects are intersection of high-dimensional data analysis,  non-convex optimization, statistics of large sample phenomenon, and theories of inverse problem. 

*About what I am doing...* <br />
after finishing my graduate study, and the ever longest year of 2020, I join Google and focus on the development of online and reinforment machine learning model, as well as on the research studies of the related optimization algorithms with practical applications in large scale. In the future, I will keep updating my new none-work-related findings on online optimization in my pages and hopefully you will find interest in.


<br/>

## Projects ##
### [Short-and-Sparse Deconvolution](https://deconvlab.github.io) ###

<table>
	<col width="25%">
	<col width="75%">
	<tr>
    	<td> <a href="https://deconvlab.github.io"><img src="/assets/fig_realdata_rec.png" > </a> </td>
    	<td>  Datasets in many areas can be effectively expressed as convolution of a <b> short </b> pattern and <b> sparse </b> map represents occurrences of the pattern. We study an algorithm for solving <a href="https://deconvlab.github.io"> deconvolution of short-and-sparse signal</a>, providing a theoretical understanding and general purposed computational method. </td>
  	</tr>
</table>

### [Microscope with Line Probe](/pages/intro_clp) ###
                 
<table>
	<col width="25%">
	<col width="75%">
	<tr>
    	<td> <a href="/pages/intro_clp"><img src="/assets/fig_probe_closeup2.png" > </a> </td>
    	<td>We study the use of <a href="/pages/intro_clp"> line probe in microscopy </a> for structured signal. Unlike conventional point probe, a single line probe measurement is the accumulated electric current between the contact surface of the line shaped probe and sample. The line probe measurements are <b> delocalized </b> and hence more <b>efficient</b>.</td>
  	</tr>
</table>




## Selected Papers ##

[Geometry and Symmetry in Short-and-Sparse Deconvolution](https://epubs.siam.org/doi/abs/10.1137/19M1237569)
{:.title}
**Han-Wen Kuo**, Yuqian Zhang, Yenson Lau,  John Wright
{:.author}
SIAM Journal on Mathematics of Data Science, 2020 
{:.booktitle}
<span class="glyphicon glyphicon-download-alt"></span><span style="margin-right:5px"><a role="button" href="/assets/siam_2020.pdf"> paper </a></span> <span class="glyphicon glyphicon-download-alt"></span><span style="margin-right:5px"><a role="button" href="https://arxiv.org/pdf/1901.00256.pdf"> arXiv </a></span> <span class="glyphicon glyphicon-paperclip"></span>
<span style="margin-right:5px"><a role="button" onclick="toggle_block('bibtex-sas-long')" >bibtex</a></span> <span> <span class="glyphicon glyphicon-picture"></span> <span style="margin-right:5px"><a role="button" href="/assets/poster_SaSD.pdf">poster</a></span> <span class="glyphicon glyphicon-film"></span> <span style="margin-right:5px"><a role="button" href="/assets/slides_SaSD.pdf">slides</a></span> 

<div id="bibtex-sas-long" class="bibtex">
@article{kuo2020geometry,
  title={Geometry and symmetry in short-and-sparse deconvolution},
  author={Kuo, Han-Wen and Zhang, Yuqian and Lau, Yenson and Wright, John},
  journal={SIAM Journal on Mathematics of Data Science},
  volume={2},
  number={1},
  pages={216--245},
  year={2020},
  publisher={SIAM}}
</div>


[Compressed Sensing Microscopy with Scanning Line Probes](https://arxiv.org/abs/1909.12342)
{:.title}
 **Han-wen Kuo**, Anna E. Dorfi, Daniel V. Esposito, John Wright, 
{:.author}
In review, 2019
{:.booktitle}

<span class="glyphicon glyphicon-download-alt"></span><span style="margin-right:5px"><a role="button" href="https://arxiv.org/pdf/1909.12342.pdf" > preprint </a></span> <span class="glyphicon glyphicon-paperclip"></span>
<span style="margin-right:5px"><a role="button" onclick="toggle_block('bibtex-csclp-long')" >bibtex</a></span><span class="glyphicon glyphicon-picture"></span> <span style="margin-right:5px"><a role="button" href="/assets/poster_secmclp.pdf">poster</a></span>

<div id="bibtex-csclp-long" class="bibtex">
@article{kuo2019compressed,
  title={Compressed Sensing Microscopy with Scanning Line Probes},
  author={Kuo, Han-Wen and Dorfi, Anna E. and Esposito, Daniel V. and Wright, John},
  journal={arXiv preprint arXiv:1909.12342},
  year={2019}
}
</div>


[Scanning Line Probe Microscopy: Beyond the Point Probe](https://pubs.acs.org/doi/pdf/10.1021/acs.analchem.8b02852)
{:.title}
Glen D. O’Neil, **Han-Wen Kuo**, Duncan N. Lomax, John Wright, Daniel V. Esposito
{:.author}
Analytical Chemistry, 2018
{:.booktitle}

<span class="glyphicon glyphicon-download-alt"></span><span style="margin-right:5px"><a role="button" href="/assets/acs.analchem.8b02852.pdf"> paper </a></span> <span class="glyphicon glyphicon-paperclip"></span>
<span><a role="button" onclick="toggle_block('bibtex-scanning')" >bibtex</a></span>

<div id="bibtex-scanning" class="bibtex">
@article{oneil2018scanning,
  title={Scanning Line Probe Microscopy: Beyond the Point Probe},
  author={O’Neil, Glen D. and Kuo, Han-Wen and Lomax, Duncan N. and Wright, John and Esposito, Daniel V.},
  journal={Analytical Chemistry},
  volume={90},
  number={19},
  pages={11531--11537},
  year={2018},
  publisher={ACS Publications}
}
</div>


## Contacts ##

Email: <hk2673@columbia.edu>
