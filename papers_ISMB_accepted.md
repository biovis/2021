---
layout: page
title: Accepted Papers for BioVis@ISMB 2017
permalink: /papers_ismb_accepted/
back_title: ISMB
back_url: ismb
---
<br>
<div style="background-color: #f2f2f2; border-style: solid; border-color: #009e9d; padding: 5px;">
<h3>BioVis@ISMB 2017 has now concluded</h3>
<p>Check back next year for more opportunities to participate in BioVis@ISMB. We also have a workshop being held in conjunction with IEEE VIS, <a href="http://biovis.net/2017/ieeevis/">BioVis@VIS</a>, that will take place in October 2017. </p>
</div>
<div style="background-color: #FFFFFF; border-style: solid; border-color: #FC5B3F; padding: 5px; margin-top:5px;">
<h4>All accepted papers are accessible via  <a href="https://bmcbioinformatics.biomedcentral.com/articles/supplements/volume-18-supplement-10"> BMC Bioinformatics</a> </h4>
</div>


{% for paper in site.data.program2017 %}
{% if paper.type == "PAPER" %}
<div class ="talk">
  <table>
  <tr>
    <td width="300px">
      <a href ="{{ site.baseurl}}/files/{{paper.image}}"> <img style="padding-right: 10px;" src="{{ site.baseurl }}/files/{{paper.image}}" alt="{{paper.title}}" height="250" width="250"></a>
    </td>
  <td>
    <div class="ttitle"> {{paper.title}}</div>
    <div>
      <br>
      <span class="tspeaker">{{paper.authors}}</span>
      <p>
      <em>Presentation Info: "{{paper.sessionTitle}}" session  between {{paper.start}} to {{paper.end}}</em>
      </p>
    </div>
    <div>
      <p>{{paper.abstract}}</p>
    </div>
    <div><span><a href="{{ paper.doi }}">Link to Full Paper</a></span></div>

  </td>
  </tr>
  </table>

</div>

{% endif %}
{% endfor %}
