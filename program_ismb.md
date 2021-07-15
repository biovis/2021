---
layout: page
title: Program BioVis@ISMB
permalink: /program_ismb/
back_title: ISMB
back_url: ismb
---


## BioVis@ISMB 2021 Program

### July 26-27, 2021

## Invited Speakers
<div class="talk">
    <div class="ttitle">Theories of inference for visualization interactions</div>
    <div><span class="tspeaker"><a href="http://users.eecs.northwestern.edu/~jhullman/">Jessica Hullman</a></span>, <span>Northwestern University</span></div>

<div class="tportrait"><img src="{{ site.baseurl}}/images/speakers/jessicahullman.jpg" style="width: 250px;" alt="Jessica Hullman">
</div>

<div class="tbioabstract" style="min-height: 310px">
        <div class="tabstract"><b>Abstract:</b>
Research and development in computer science and statistics have produced increasingly sophisticated software interfaces for interactive and exploratory analysis, optimized for easy pattern finding and data exposure. But design philosophies that emphasize exploration over other phases of analysis risk confusing a need for flexibility with a conclusion that exploratory visual analysis is inherently “model free” and cannot be formalized. We describe how without a grounding in theories of human statistical inference, research in exploratory visual analysis can lead to contradictory interface objectives and representations of uncertainty that can discourage users from drawing valid inferences. We discuss how the concept of a model check in a Bayesian statistical framework unites exploratory and confirmatory analysis, and how this understanding relates to other proposed theories of graphical inference. Viewing interactive analysis as driven by model checks suggests new directions for software and empirical research around exploratory and visual analysis.</div>

<div class="tbio"><b>Bio:</b>
		Jessica Hullman is an Associate Professor of Computer Science and Journalism at Northwestern University. Her research develops new representations, interactions, and evaluation methods for aiding people in analyzing and visualizing data to amplify cognition and decision making. Her recent research also addresses theories of data analysis and science reform. She founded and co-directs the Midwest Uncertainty Collective, a lab devoted to better visualization techniques, tools, evaluations, and theory around how to communicate uncertainty in data. Jessica is the recipient of a Microsoft Faculty Fellowship, NSF CAREER Award, and multiple best papers at top visualization and human-computer interaction conferences, among other awards.   
        </div>
		<br/>
    </div>
</div>


<div class="talk">

<div class="ttitle">Inter-disciplinary practices in BioVis </div>
<div><span class="tspeaker"><a href="https://www.garvan.org.au/people/seaodo">Seán O’Donoghue</a></span>, <span> Garvan Institute of Medical Research </span></div>
<div class="tportrait"><img src="{{ site.baseurl}}/images/speakers/sean_odonoghue.jfif" style="width: 250px;" alt="Seán O’Donoghue"></div>

<div class="tbioabstract" style="min-height: 270px"> 
        <div class="tabstract"><b>Abstract:</b>
	BioVis involves a diverse community; while many of us are computer scientists, bioinformaticians, or bench biologists, our field also engages designers and illustrators, and our outcomes are used by students, educators, and science communicators. In this talk, I will highlight work practices used in inter-disciplinary collaborations to address key BioVis challenges. In addition to drawing on historical exemplars, I will showcase how I have used these practices in recent collaborative work on (a) human genetic variations, (b) multi-omics time-series studies, (c) the SARS-CoV-2 proteome, and (d) exploring protein structures with extended reality. I will also discuss how these practises influence the emergence of BioVis as a recognized discipline.</div>

<div class="tbio"><b>Bio:</b>
Seán O’Donoghue leads the BioVis Centre (<a href="http://odonoghuelab.org/">http://odonoghuelab.org/</a>) based at the Garvan Institute of Medical Research in Sydney, Australia. He is also chief editor of the Data Visualization section of the Frontiers in Bioinformatics journal. Formerly, he was also an OCE Science Leader and a Chief Research Scientist in Australia's CSIRO. Much of his career was spent at the EMBL in Heidelberg, Germany, and also at EMBL’s first spin-off company, Lion Bioscience AG, where he was Director of Scientific Visualisation. Seán's career has focused on using computational methods to advance the life sciences. His early work was on improving how bimolecular structures are calculated from NMR data; however since 2000 he has focused on data visualization methods. He is co-founder and chair of the 'VIZBI' initiative, aimed at raising the global standard of data visualisation in computational biology. His team have created bioinformatics resources used by tens of thousands of life scientists worldwide, as well as informative and inspirational biomedical animations seen by over half a million people. His current research interests centre on using bioinformatics and data visualisation to better understand the spatial organisation of the genome (e.g., <a href="http://rondo.ws/">http://rondo.ws/</a>),  dynamic changes in the epiproteome (e.g., <a href="https://minardo.org/">https://minardo.org/</a>), and the structural biology of the proteome (e.g., <a href="https://aquaria.app/">https://aquaria.app/</a>) - including the unknown or 'dark' proteome.
</div>
</div>
</div>


## Program
Please note that all the times listed here are in **Coordinated Universal Time (UTC)**.
<br/>

{% assign prevSession = "" %}
{% for paper in site.data.program2021 %}
  
  {% if prevSession != paper.session %}
	{% for next in (forloop.index0..site.data.program2021.size) %}
	    {% if site.data.program2021[next].session == paper.session %}
			{% assign sessionEnd = site.data.program2021[next].end%}
		{% else %}
			{% break %}
		{% endif %}
   	{% endfor %}

  <hr class="style-one" />
  <div>
	{% if paper.start != nil %}	
    <div class="sumTime2"> {{paper.start}} - {{sessionEnd}}</div>
	{% endif %}
    <div class="sumContent">{{paper.session}} {% if paper.chair != nil %}<div style="font-size:16px; padding-left:120px;">Chair: {{paper.chair}}</div>{%endif%}</div>
  </div>
  {% endif %}

  {% if paper.title != nil %}
  <div>
	  {% if paper.start != nil %}
      <div class="sumTime" style="padding-top:5px;"> {{paper.start}} - {{paper.end}}</div>
	  {% endif %}
	<div class="ttile" style="{% if paper.start != nil %}padding-left:120px;{%endif%}padding-top:5px;">
        <strong>
	 {% if paper.type != nil %}[{{paper.type}}]{% endif %}
	    {{paper.title}}
        </strong>
	</div>
	  {% if paper.presenter != nil %}
		<div class="sumDetail" {% if paper.start != nil %}style="padding-left:120px;"{%endif%}> <em>Speaker:</em> {{paper.presenter}}</div>
	  {% endif %}
          {% if paper.authors != nil %}
		<div class="sumDetail" {% if paper.start != nil %}style="padding-left:120px;"{%endif%}> <em>Authors:</em> {{paper.authors}}</div>
	  {% endif %}
  </div>
  {% endif %}
  
  {% assign prevSession = paper.session %}
  
{% endfor %}

<hr class="style-one">
