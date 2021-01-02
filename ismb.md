---
layout: map_page
logo: ismb.svg
title: BioVis at ISMB (BioVis@ISMB)
location: July 15, Montreal, Canada
main_venue_rln: Co-located
main_venue: ISMB 2020
main_venue_url: https://www.iscb.org/ismb2020
permalink: /ismb/
---
<!--<br>
<div style="background-color: #f2f2f2; border-style: solid; border-color: #009e9d; padding: 5px;">
<h4> Additional details for BioVis@ISMB 2018 will be announced soon. In the meantime check out last year's event <a href="http://biovis.net/2017/ismb">BioVis@ISMB</a> and our co-located meeting with <a href= "http://biovis.net/2017/ieeevis">IEEE VIS 2017</a> </h4>
</div>-->

<div class="row center-align">
    <div class="col m4 s12 event-page-menu-block">
     <i class="material-icons large">people</i>
     <h3>Call for Participation</h3>
     <a class="btn waves-effect waves-light" href="{{site.baseurl}}/cfp_ismb" type="submit" name="action">View CfP</a>
    </div>

    <!--<div class="col m4 s12 event-page-menu-block">
     <i class="material-icons large">file_upload</i>
     <h3>Submission Info</h3>
     <a class="btn waves-effect waves-light disabled" href="{{site.baseurl}}/submission_ismb" type="submit" name="action">View Submission Info </a>
    </div>-->

    <div class="col m4 s12 event-page-menu-block">
        <i class="material-icons large">border_color</i>
        <h3>Registration</h3>
        <a class="btn waves-effect waves-light" href="https://www.iscb.org/ismb2020-registration" type="submit" name="action">Register</a>
    </div>

    <div class="col m4 s12 event-page-menu-block">
     <i class="material-icons large">list</i>
     <h3>Main Program</h3>
     <a class="btn waves-effect waves-light" href="{{site.baseurl}}/program_ismb" type="submit" name="action">View Main Program</a>
    </div>
</div>

<br/>

<br/>

<div class="row left-align">    
      <div class="col s12 m6">
            <h4 id="ismbImportantDates">Important Dates</h4>
             <p><strong>ISMB COSI date:</strong>  {{ site.ISMBconferencedate }} </p>
            <p><strong>ISMB Proceedings Paper Submission Deadline:</strong>  {{ site.ismb_paper_submission_deadline }}</p>
			<p><strong>Talk Submission Deadline:</strong> {{ site.ismb_abstract_submission_deadline}}</p>  
            <p><strong>Poster Submission Deadline:</strong>  {{ site.ismb_poster_submission_deadline }}</p>
			<p><a href="http://www.iscb.org/ismb2020-keydates">See ISMB Key Dates for more details</a></p>
      </div>


      <div class="col s12 m6">
          <h4>Latest News</h4>
          <ul class="post-list">
           {% for post in site.posts %}
             {% capture category %}{{post.event}}{% endcapture %}
              {% if category == "ismb" %}
              <li class="post-list-item-event">
                 <span class="date">{{ post.date | date: "%-d %b %Y" }}</span>
                 <span class="post-list-title">
                   <a class="post-list-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                 </span>
                 <p class="post-list-excerpt">
                   {{ post.excerpt }}
                 </p>              
               </li>
              {% endif %}
             {% endfor %}
           </ul>
      </div>
</div>

<br/>
<br/>
