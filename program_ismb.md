---
layout: page
title: Program BioVis@ISMB
permalink: /program_ismb/
back_title: ISMB
back_url: ismb
---


## BioVis@ISMB 2020 Program

### July 15, 2020

## Invited Speakers

<div class="talk">
    <div class="ttitle">Visualization and Human-AI collaboration for biomedical tasks
</div>
    <div><span class="tspeaker"><a href="http://hendrik.strobelt.com">Hendrik Stobelt</a></span>, <span> IBM Research & MIT </span></div>

    <div class="tportrait"><img src="{{ site.baseurl}}/images/speakers/stobelt.png" style="width: 250px;" alt="Hendrik Stobelt"></div>

    <div class="tbioabstract" style="min-height: 270px"> 
	
	<!--<div class="tabstract"><b>Abstract:</b>TBA</div>-->
	
	<div class="tbio"><b>Bio:</b>
		Hendrik Strobelt is the Explainability Lead at the MIT-IBM Watson AI Lab and Research Scientist at IBM Research. His recent research is on visualization for and human collaboration with AI models to foster explainability and intuition. The majority of his work is for NLP models and generative models while he is advocating to utilize a mix of data modalities to solve real-world problems. His work is applied to tasks in machine learning, in NLP, in the biomedical domain, and chemistry. Hendrik joined IBM in 2017 after postdoctoral positions at Harvard SEAS and NYU Tandon. He received a Ph.D. (Dr. rer. nat.) from the University of Konstanz in computer science (Visualization) and holds an MSc (Diplom) in computer science from TU Dresden. He received multiple best paper/honorable mention awards at EuroVis, BioVis, VAST, and ACL Demo. He received the Lohrmann medal from TU Dresden as the highest student honor. Hendrik has served in program committees and organization committees for IEEE VIS, BioVis, EuroVis. He was the virtual chair for ICLR 2020. Hendrik is affiliated as visiting researcher with MIT CSAIL.
	</div>
    </div>
</div>

<a name="sheelagh"></a>
<div class="talk">
    <div class="ttitle">Machine Learning for Drug Repurposing</div>
    <div><span class="tspeaker"><a href="https://dbmi.hms.harvard.edu/people/marinka-zitnik">Marinka Zitnik</a></span>, <span> Harvard Medical School </span></div>

    <div class="tportrait"><img src="{{ site.baseurl}}/images/speakers/marinka-zitnik.jpg" style="width: 250px;" alt="Marinka Zitnik">
    </div>

    <div class="tbioabstract" style="min-height: 310px">

        <!--<div class="tabstract"><b>Abstract:</b>TBA</div>-->

       <div class="tbio"><b>Bio:</b>
		Marinka Zitnik is an Assistant Professor of Biomedical Informatics at Harvard Medical School. She is a computer scientist studying applied machine learning with a focus on challenges brought forward by data in science, medicine, and health. Dr. Zitnik joined Harvard Medical School in December 2019. Before that, she was a postdoctoral scholar in Computer Science at Stanford University working with Jure Leskovec. She was also a member of the Chan Zuckerberg Biohub at Stanford. She received Ph.D. in Computer Science from University of Ljubljana in 2015 while also researching at Imperial College London, University of Toronto, Baylor College of Medicine, and Stanford University. She received my bachelor’s degree in 2012 double majoring in computer science and mathematics. Her algorithms and methods have had a tangible impact, which has garnered interests of government, academic, and industry researchers and has put new tools in the hands of practitioners. Some of her methods are used by major biomedical institutions, including Baylor College of Medicine, Karolinska Institute, Stanford Medical School, and Massachusetts General Hospital. Her work received several best paper, poster, and research awards from the International Society for Computational Biology. She has recently been named a Rising Star in EECS by MIT and also a Next Generation in Biomedicine by The Broad Institute of Harvard and MIT, being the only young scientist who received such recognition in both EECS and Biomedicine.
        </div>
		<br/>
    </div>
</div>

## Program

#### Please note that all the times listed here are in **Eastern Daylight Time**.

<br/>

{% assign prevSession = "" %}
{% for paper in site.data.program2020 %}
  
  {% if prevSession != paper.session %}
	{% for next in (forloop.index0..site.data.program2020.size) %}
	    {% if site.data.program2020[next].session == paper.session %}
			{% assign end = site.data.program2020[next].end%}
		{% else %}
			{% break %}
		{% endif %}
   	{% endfor %}

  <hr class="style-one" />
  <div>
	{% if paper.start != nil %}	
    <div class="sumTime2"> {{paper.start}} - {{end}}</div>
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
