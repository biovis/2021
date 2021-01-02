
<!-- WELCOME --->
<div>
    <div class="sumTime2">10:15 - 10:20</div>
    <div>
        <div class="sumContent">BioVis Welcome</div>
          <div class="sumDetail" style="padding-left:120px;"><i>TBA</i></div>
    </div>
</div>

<hr class="style-one">


<!-- SESSION 1 --->

<div>
    <div class="sumTime2"> 10:20 - 12:40</div>
    <div>
        <div class="sumContent">1st Session</div>
    </div>
    <div class="sumDetail" style="padding-left:120px;"><i>Session Chair: TBA</i> </div>
    <!-- <div class="sumDetail" style="padding-left:120px;font-size:12px;"><i>(* indicates presenting author)</i> </div> -->
</div>

{% for paper in site.data.program2018%}
{% if paper.session == "session1"%}
  <div>
      <div class="sumTime" style="padding-top:5px;"> {{paper.start}} - {{paper.end}}</div>
      {% if paper.doi != nil %}
      <div>
          <div class="ttile" style="padding-left:120px; padding-top:5px;">
          <b><!--<a href="{{paper.doi}}">--> [{{paper.type}}] <!--</a>--></b> <b>{{paper.title}}</b></div>
      </div>
      {% else %}
      <div>
          <div class="ttile" style="padding-left:120px; padding-top:5px;"> <b>[{{paper.type}}] {{paper.title}}</b></div>
      </div>
      {% endif %}
      <div class="sumDetail" style="padding-left:120px;"> <em>Authors:</em> {{paper.authors}}</div>
  </div>
{% endif %}
{% endfor %}

<!-- SESSION 2 -->
<hr class="style-one">

<div>
    <div class="sumTime2">2:00 - 4:00</div>
    <div>
        <div class="sumContent">2nd Session</div>
    </div>
    <div class="sumDetail" style="padding-left:120px;"><i>Session Chair: TBA</i> </div>
     <!-- <div class="sumDetail" style="padding-left:120px;font-size:12px;"><i>(* indicates presenting author)</i> </div> -->
</div>

{% for paper in site.data.program2018%}
{% if paper.session == "session2"%}
  <div>
      <div class="sumTime" style="padding-top:5px;"> {{paper.start}} - {{paper.end}}</div>
      {% if paper.doi != nil %}
      <div>
          <div class="ttile" style="padding-left:120px; padding-top:5px;">
          <b><!--<a href="{{paper.doi}}">--> [{{paper.type}}] <!--</a>--></b> <b>{{paper.title}}</b></div>
      </div>
      {% else %}
      <div>
          <div class="ttile" style="padding-left:120px; padding-top:5px;"> <b>[{{paper.type}}] {{paper.title}}</b></div>
      </div>
      {% endif %}
      <div class="sumDetail" style="padding-left:120px;"> <em>Authors:</em> {{paper.authors}}</div>
  </div>
{% endif %}
{% endfor %}

<!-- SESSION 3 -->
<hr class="style-one">

<div>
    <div class="sumTime2">4:40 - 5:50</div>
    <div>
        <div class="sumContent">3rd Session</div>
    </div>
    <div class="sumDetail" style="padding-left:120px;"><i>Session Chair: TBA</i> </div>
     <!-- <div class="sumDetail" style="padding-left:120px;font-size:12px;"><i>(* indicates presenting author)</i> </div> -->
</div>

{% for paper in site.data.program2018%}
{% if paper.session == "session3"%}
  <div>
      <div class="sumTime" style="padding-top:5px;"> {{paper.start}} - {{paper.end}}</div>
      {% if paper.doi != nil %}
      <div>
          <div class="ttile" style="padding-left:120px; padding-top:5px;">
          <b><!--<a href="{{paper.doi}}">--> [{{paper.type}}] <!--</a>--></b> <b>{{paper.title}}</b></div>
      </div>
      {% else %}
      <div>
          <div class="ttile" style="padding-left:120px; padding-top:5px;"> <b>[{{paper.type}}] {{paper.title}}</b></div>
      </div>
      {% endif %}
      <div class="sumDetail" style="padding-left:120px;"> <em>Authors:</em> {{paper.authors}}</div>
  </div>
{% endif %}
{% endfor %}

<!-- CLOSING REMARKS AND POSTER SESSION -->
<hr class="style-one">
<div>
    <div class="sumTime2">5:50 - 6:00</div>
    <div>
        <div class="sumContent">Closing Remarks</div>
          <div class="sumDetail" style="padding-left:120px;"><i>TBA</i></div>
    </div>
</div>

<hr class="style-one">


<div>
    <div class="sumTime2">6:00 - 7:00</div>
    <div>
        <div class="sumContent">Poster Session</div>
       
		<div class="sumDetail" style="padding-left:120px;"><a href="">BioVis posters</a></div>
		
    </div>
</div>