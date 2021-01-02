---
layout: home
---

<div class="row">
    <div class="blue-section col s12"> 
	
		<a href="{{site.baseurl}}/ismb">
			<div class="col s12 m4">
				<div class="row event center-align">
					<div class="col s12">
						<img src="{{ site.baseurl }}/images/logos/ismb.svg" width="30%">
					</div>

					<div class="col s12 event-details">
						<div class="event-name">ISMB {{ site.year }} - Main Conference Event</div>
						<div class="event-location">{{ site.ISMBconferenceplace }}</div>
						<div class="event-date">{{ site.ISMBconferencedate }}</div>
					</div>
				</div>
			</div>
		</a>
		
		<a href="{{site.baseurl}}/ieeevis">
			<div class="col s12 m4">
				<div class="row event center-align">
					<div class="col s12">
						<img src="{{ site.baseurl }}/images/logos/ieee.svg" width="30%">
					</div>

					<div class="col s12 event-details">
						<div class="event-name">IEEE VIS {{ site.year }} - Workshop</div>
						<div class="event-location">{{ site.IEEEconferenceplace }}</div>
						<div class="event-date">{{ site.IEEEconferencedate }}</div>
					</div>
				</div>
			</div>
		</a>
		
		<div class="col s12 m4">
			<div class="row event center-align">
				<div class="col s12">
					<img src="{{ site.baseurl }}/images/logos/dream.svg" width="20%">
				</div>

				<div class="col s12 event-details">
					<div class="event-name">Important Dates</div>
					<div class="event-date">
						<strong>ISMB COSI Date:</strong> {{ site.ISMBconferencedate }} <br/>
						<strong>ISMB Proceedings Paper Submission Deadline:</strong> {{ site.ismb_paper_submission_deadline }} <br/>
						<strong>ISMB Talk Submission Deadline:</strong>  {{ site.ismb_abstract_submission_deadline }} <br/>
						<strong>ISMB Poster Submission Deadline:</strong>  {{ site.ismb_poster_submission_deadline }} <br/>
						<a href="{{&$site.ismblink}}-keydates" style="color:#2c3e50; text-decoration: underline;">See ISMB Key Dates for more details</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<div class="row">
        <div class="home-info-section col s12">
              <p style="color: white;">The BioVis meetings are intended to educate, inspire, and engage visualization researchers in problems in biological data visualization, as well as bioinformatics and biology researchers in state-of-the-art visualization research</p>
        </div>

        <div class="home-info-container col s12">
        </div>
		

        <div class="blue-section col s12">
        <div class="container">
              <p class="hide-on-small-only">
			  There are multiple ways to participate in BioVis through conferences and ongoing events. This year, the main BioVis event will be at <a href="https://www.iscb.org/about-ismb">ISMB</a> as a <a href="https://www.iscb.org/communities-of-special-interest">Community of Special Interest (COSI)</a> in {{site.ISMBconferencedate}} in {{site.ISMBconferenceplace}}. A smaller workshop event will be held at <a href="http://ieeevis.org" >IEEE VIS</a> in {{site.IEEEconferencedate}} in {{site.IEEEconferenceplace}}.  These events serve as a platform for researchers from biology, bioinformatics, and information visualization fields to increase the impact of data visualization approaches in biology, and to initiate interdisciplinary collaborations. Get involved in our events at a conference or challenge (or all three!). Important dates for submissions are available below, and on the detailed pages for each event.
              </p>		  
			  
            

<!--
                <div class="col s12 m6">
                <div class="row">
                      <a href="{{site.baseurl}}/ieeevis">
                        <div class="col s12 eventSplit center-align">
                            <div class="col s6 center-align">
                              <span class="helper"></span><img src="{{ site.baseurl }}/images/logos/ieee.svg" width="70%">
                            </div>
                          <div class="col s6 event-details">
                            <div class="event-name" style="text-align:left;">IEEE VIS 2019</div>
                            <div class="event-subtitle" style="text-align:left;">Workshop</div>
                            <div class="event-location" style="text-align:left;">Vancouver Canada</div>
                            <div class="event-date" style="text-align:left;">October 2019</div>
                          </div>
                        </div>
                      </a>
                  </div>

                  <div class="row">
                  <a href="{{site.baseurl}}/dream">
                    <div class="row event center-align">
                        <div class="col s6 center-align">
                          <span class="helper"></span><img src="{{ site.baseurl }}/images/logos/dream.svg" style="vertical-align: middle;" width="70%">
                        </div>
                      <div class="col s6 event-details">
                      <div class="event-name" style="text-align:left;">DREAM </div>
                      <div class="event-subtitle" style="text-align:left;">SMC-RNA BioVis Data Visualization DREAM Challenge</div>
                      </div>
                    </div>
                  </a>
                  </div>
                 </div>

               
                  <a href="{{site.baseurl}}/dream">
                  <div class="col s12 m4">
                      <div class="row event center-align">
                          <div class="col s12">
                              <img src="{{ site.baseurl }}/images/logos/dream.svg" width="40%">
                          </div>

                          <div class="col s12 event-details">
                              <div class="event-name">DREAM 2016</div>
                              <div class="event-subtitle">SMC-RNA BioVis Data Visualization DREAM Challenge</div>

                          </div>
                      </div>
                    </div>
                    </a>
                </div>
-->
                <!--
                <p class="hide-on-small-only">The BioVis meetings are intended to educate, inspire, and engage visualization researchers in problems in biological data visualization, as well as bioinformatics and biology researchers in state-of-the-art visualization research. The workshops serve as a platform for researchers from these fields to increase the impact of data visualization approaches in biology, and to initiate interdisciplinary collaborations.</p>
                -->
                </div>
                </div>

               

                <!-- ADDING A NEWS FEED -->
                <div class="row blue-section center-align">
                    <div class="container">

                        <div class="col s12 m12 center-align">
                            <!-- <h4><i class="material-icons" style="font-size: .9em">announcement</i> News</h4> -->
                            <h4> News </h4>
                        </div>

                          <div class="col s12 m12">
                             <ul class="post-list">
                                 {% for post in site.posts limit:3%}
                                   {% capture category %}{{post.event}}{% endcapture %}
                                   <li class="col s12 m12 l12">
                                        <div class="post-list-item">

                                       <span class="type {{category}}">
                                            {% if category == "ismb" %}
                                                <a href="{{site.baseurl}}/ismb">@ ISMB</a>
                                            {% elsif category == "ieee" %}
                                                <a href="{{site.baseurl}}/ieeevis">@ IEEE</a>
                                            {% elsif category == "dream" %}
                                                <a href="{{site.baseurl}}/dataContest_dream">@ DREAM</a>
                                            {% endif %}
                                        </span>

                                        <span class="post-list-title">
                                            {{ post.date | date: "%-d %b %Y" }}
                                        </span>
                                        <h4><a class="post-list-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h4>
                                        <span class="post-list-excerpt">
                                            {{ post.excerpt }}
                                        </span>     
                                        </div>
                                  </li>

                                 {% endfor %}
                             </ul>
                          </div>
                    </div>
                </div>

                <!-- END ADDING A NEWS FEED -->

                    <div class="row center-align">
                    <div class="container">
                        <div class="col s12 m12">

                            <h4>Affiliates</h4>
                            <p> {{ site.conferenceshort }} is an official part of <a href="{{&$site.ismblink}}">ISMB {{$site.year}}</a></p>
                            <p>    <a href="https://www.iscb.org">
                                    <img src="{{site.baseurl}}/images/sponsors/ISCB.jpg" alt="ISCB"/>
                                </a>
                             </p>
                             <br/>
                    </div>
                </div>
        </div>
