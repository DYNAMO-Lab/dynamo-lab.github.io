---
layout: page
permalink: /team.html
title: team
page-title: Team 
description:
nav: true
nav_order: 2
nav_rank: 2
---
    
<style>
  .group-section {
      margin-bottom: 2rem; 
  }
  
  .team-image {
      display: block;
      margin: 0 auto 2rem auto; 
      max-width: 70%;
      height: auto;
  }
</style>

<!-- Team Image at the Start -->
<div class="text-center my-4">
    <img src="{{ '/assets/img/team/IMG_2570.JPG' | relative_url }}" alt="Team Image" class="team-image img-fluid">
</div>

{% assign groups = site.members | sort: "group_rank" | map: "group" | uniq %}
{% for group in groups %}
## {{ group }}

<!-- Add Bootstrap spacing class or custom class for additional margin -->
<div class="group-section">

 {% assign members = site.members | sort: "group_order" | where: "group", group %}
    {% for member in members %}
<p>
    <div class="card {% if member.inline == false %}hoverable{% endif %} mb-3">
        <div class="row no-gutters">
            <div class="col-sm-4 col-md-3">
                <img src="{{ '/assets/img/team/' | append: member.profile.image | relative_url }}" class="card-img img-fluid" alt="{{ member.profile.name }}" />
            </div>
            <div class="team col-sm-8 col-md-9">
                <div class="card-body">
                    {% if member.inline == false %}
                        <a href="{{ member.profile.website }}" {% if member.external %}target="_blank"{% endif %}>
                    {% endif %}
                        <h5 class="card-title">{{ member.profile.name }}</h5>
                        {% if member.profile.position %}
                            {% if member.profile.team-position %}
                                <h6 class="card-subtitle mb-2 text-muted">{{ member.profile.team-position }}</h6>
                            {% else %}
                                <h6 class="card-subtitle mb-2 text-muted">{{ member.profile.position }}</h6>
                            {% endif %}
                        {% endif %}
                        <p class="card-text">
                            {{ member.teaser }}
                        </p>
                    {% if member.inline == false %}
                        </a>
                    {% endif %}
                    {% if member.profile.email %}
                        <a href="mailto:{{ member.profile.email }}" class="card-link"><i class="fas fa-envelope"></i></a>
                    {% endif %}
                    {% if member.profile.phone %}
                        <a href="tel:{{ member.profile.phone }}" class="card-link"><i class="fas fa-phone"></i></a>
                    {% endif %}
                    {% if member.profile.orcid %}
                        <a href="https://orcid.org/{{ member.profile.orcid }}" class="card-link" target="_blank"><i class="fab fa-orcid"></i></a>
                    {% endif %}
                    {% if member.profile.twitter %}
                        <a href="https://twitter.com/{{ member.profile.twitter }}" class="card-link" target="_blank"><i class="fab fa-twitter"></i></a>
                    {% endif %}
                    {% if member.profile.github %}
                        <a href="https://github.com/{{ member.profile.github }}" class="card-link" target="_blank"><i class="fab fa-github"></i></a>
                    {% endif %}
                    {% if member.profile.website %}
                        <a href="{{ member.profile.website }}" class="card-link" target="_blank"><i class="fas fa-globe"></i></a>
                    {% endif %}
                    <p class="card-text">
                        <small class="text-muted"><i></i> {{ member.profile.address | replace: '<br />', ', ' }}</small>
                    </p>
                </div>
            </div>
        </div>
    </div>
</p>
    {% endfor %}
</div> <!-- End of group-section -->
{% endfor %}

---

## Undergraduate Students

<div class="table-responsive my-5">
    <table class="table table-striped table-hover table-bordered">
        <thead class="thead-dark">
            <tr>
                <th>Name</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Will Corcoran</td>
            </tr>
            <tr>
                <td>Sterling Hsu</td>
            </tr>
            <tr>
                <td>Ben Monastyrsky</td>
            </tr>
            <tr>
                <td>Eirini Schoinas</td>
            </tr>
            <tr>
                <td>Sohom Dutta</td>
            </tr>
            <tr>
                <td>Susan Clay</td>
            </tr>
              <tr>
                <td>Victor Nardi</td>
            </tr>
        </tbody>
    </table>
</div>

---

## Alumni

<div class="table-responsive my-5">
    <table class="table table-striped table-hover table-bordered">
        <thead class="thead-dark">
            <tr>
                <th>Name</th>
                <th>Degree</th>
                <th>Year</th>
                <th>Current Employer</th>
            </tr>
        </thead>
        <tbody>
                     <tr>
                <td>Joseph Foster</td>
                <td>MS</td>
                <td>2025</td>
                <td>-</td>
            </tr>

                     <tr>
                <td>Jeffrey Chen</td>
                <td>MS</td>
                <td>2025</td>
                <td>-</td>
            </tr>




             <tr>
                <td>Kha-Dinh Luong</td>
                <td>PhD</td>
                <td>2025</td>
                <td><a href="https://www.amazon.com" target="_blank">Amazon.com</a></td>
            </tr>

                         <tr>
                <td>Esha Gupta</td>
                <td>MS</td>
                <td>2025</td>
                <td><a href="https://www.amazon.com" target="_blank">Amazon.com</a></td>
            </tr>

                     <tr>
                <td>Qiming Wu</td>
                <td>MS</td>
                <td>2024</td>
                <td><a href="https://www.nvidia.com" target="_blank">NVIDIA</a></td>
            </tr>

                    <tr>
                <td>Sean Jaffe</td>
                <td>PhD</td>
                <td>2024</td>
                <td>Celonis</td>
            </tr>

            <tr>
                <td>Nikunj Baid</td>
                <td>MS</td>
                <td>2023</td>
                <td><a href="https://www.arista.com" target="_blank">Arista Networks</a></td>
            </tr>
            <tr>
                <td>Zexi Huang</td>
                <td>PhD</td>
                <td>2023</td>
                <td><a href="https://www.tiktok.com" target="_blank">TikTok</a></td>
            </tr>
            <tr>
                <td>Mert Kosan</td>
                <td>PhD</td>
                <td>2023</td>
                <td><a href="https://usa.visa.com/about-visa/visa-research.html" target="_blank">Visa Research</a></td>
            </tr>
            <tr>
                <td>Sikun Lin</td>
                <td>PhD</td>
                <td>2022</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Yuning Shen</td>
                <td>MS</td>
                <td>2022</td>
                <td><a href="https://www.bytedance.com" target="_blank">ByteDance</a></td>
            </tr>
            <tr>
                <td>Furkan Kocayusufoglu</td>
                <td>PhD</td>
                <td>2021</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Hongyuan You</td>
                <td>PhD</td>
                <td>2021</td>
                <td><a href="https://www.ebayinc.com" target="_blank">eBay</a></td>
            </tr>
            <tr>
                <td>Omid Askarisichani</td>
                <td>PhD</td>
                <td>2020</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Haraldur Hallgrimsson</td>
                <td>PhD</td>
                <td>2020</td>
                <td><a href="https://www.apple.com" target="_blank">Apple</a></td>
            </tr>
            <tr>
                <td>Aneesha Mathur</td>
                <td>MS</td>
                <td>2020</td>
                <td><a href="https://www.oracle.com" target="_blank">Oracle</a></td>
            </tr>
            <tr>
                <td>Koa Sato</td>
                <td>MS</td>
                <td>2020</td>
                <td><a href="https://www.marvell.com" target="_blank">Marvell Semiconductor</a></td>
            </tr>
            <tr>
                <td>Wei Ye</td>
                <td>Postdoc</td>
                <td>2020</td>
                <td><a href="https://www.tongji.edu.cn/en/" target="_blank">Tongji University</a></td>
            </tr>
                                    <tr>
                <td>Sourav Medya</td>
                <td>PhD</td>
                <td>2019</td>
                <td><a href="https://www.uic.edu" target="_blank">University of Illinois - Chicago</a></td>
            </tr>

                        <tr>
                <td>Arlei Silva</td>
                <td>PhD</td>
                <td>2019</td>
                <td><a href="https://www.rice.edu" target="_blank">Rice University</a></td>
            </tr>
            <tr>
                <td>Sai Nikhil Maram</td>
                <td>MS</td>
                <td>2019</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Ashwini Patil</td>
                <td>MS</td>
                <td>2019</td>
                <td><a href="https://www.apple.com" target="_blank">Apple</a></td>
            </tr>
            <tr>
                <td>Richika Sharan</td>
                <td>MS</td>
                <td>2019</td>
                <td><a href="https://www.microsoft.com" target="_blank">Microsoft</a></td>
            </tr>
            <tr>
                <td>Chandana Upadhyaya</td>
                <td>MS</td>
                <td>2019</td>
                <td><a href="https://www.microsoft.com" target="_blank">Microsoft</a></td>
            </tr>
            <tr>
                <td>Victor Amelkin</td>
                <td>PhD</td>
                <td>2018</td>
                <td><a href="https://www.amazon.com" target="_blank">Amazon.com</a></td>
            </tr>
            <tr>
                <td>Xuan-Hong Dang</td>
                <td>Postdoc</td>
                <td>2017</td>
                <td><a href="https://www.research.ibm.com/" target="_blank">IBM Research, NY</a></td>
            </tr>
            <tr>
                <td>Minh Hoang</td>
                <td>PhD</td>
                <td>2017</td>
                <td><a href="https://about.facebook.com/" target="_blank">Facebook</a></td>
            </tr>
            <tr>
                <td>Roman Kazarin</td>
                <td>MS</td>
                <td>2016</td>
                <td><a href="https://about.facebook.com/" target="_blank">Facebook</a></td>
            </tr>
            <tr>
                <td>Bo Zong</td>
                <td>PhD</td>
                <td>2015</td>
                <td><a href="https://www.salesforce.com" target="_blank">Salesforce</a></td>
            </tr>
            <tr>
                <td>Petko Bogdanov</td>
                <td>PhD</td>
                <td>2014</td>
                <td><a href="https://www.albany.edu" target="_blank">State University of New York, Albany</a></td>
            </tr>
            <tr>
                <td>Nazli Dereli</td>
                <td>MS</td>
                <td>2014</td>
                <td><a href="https://www.ticketmaster.com" target="_blank">Ticketmaster</a></td>
            </tr>
            <tr>
                <td>Yilei Wang</td>
                <td>MS</td>
                <td>2014</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Nick Larusso</td>
                <td>PhD</td>
                <td>2012</td>
                <td><a href="https://www.amazon.com" target="_blank">Amazon</a></td>
            </tr>
            <tr>
                <td>Kathy Macropol</td>
                <td>PhD</td>
                <td>2012</td>
                <td><a href="https://www.arcadia.edu" target="_blank">Arcadia University</a></td>
            </tr>
            <tr>
                <td>Misael Mongiovi</td>
                <td>Postdoc</td>
                <td>2012</td>
                <td><a href="https://www.istec.cnr.it/" target="_blank">Institute of Science and Technology of Cognition at CNR (Italy)</a></td>
            </tr>
            <tr>
                <td>Sayan Ranu</td>
                <td>PhD</td>
                <td>2012</td>
                <td><a href="https://www.iitd.ac.in" target="_blank">IIT Delhi</a></td>
            </tr>
            <tr>
                <td>Brian Ruttenberg</td>
                <td>PhD</td>
                <td>2012</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Kyle Chipman</td>
                <td>PhD</td>
                <td>2011</td>
                <td><a href="https://waymo.com" target="_blank">Waymo</a></td>
            </tr>
            <tr>
                <td>Vishwakarma Singh</td>
                <td>PhD</td>
                <td>2011</td>
                <td><a href="https://www.pinterest.com" target="_blank">Pinterest</a></td>
            </tr>
            <tr>
                <td>Arnab Bhattacharya</td>
                <td>PhD</td>
                <td>2007</td>
                <td><a href="https://www.iitk.ac.in/" target="_blank">IIT Kanpur</a></td>
            </tr>
            <tr>
                <td>Huahai He</td>
                <td>PhD</td>
                <td>2007</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Swaroop Jagadish</td>
                <td>MS</td>
                <td>2007</td>
                <td><a href="https://www.linkedin.com" target="_blank">LinkedIn</a></td>
            </tr>
            <tr>
                <td>Vebjorn Ljosa</td>
                <td>PhD</td>
                <td>2007</td>
                <td><a href="https://www.resilience.com/" target="_blank">Resilience</a></td>
            </tr>
            <tr>
                <td>Anand Meka</td>
                <td>PhD</td>
                <td>2007</td>
                <td><a href="https://www.oracle.com" target="_blank">Oracle</a></td>
            </tr>
            <tr>
                <td>Orhan Camoglu</td>
                <td>PhD</td>
                <td>2006</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Pei-Ching Lu</td>
                <td>MS</td>
                <td>2006</td>
                <td><a href="https://www.apple.com" target="_blank">Apple</a></td>
            </tr>
            <tr>
                <td>Ahmet Bulut</td>
                <td>PhD</td>
                <td>2005</td>
                <td><a href="https://www.carbonhealth.com" target="_blank">Carbon Health</a></td>
            </tr>
            <tr>
                <td>Tolga Can</td>
                <td>Postdoc</td>
                <td>2005</td>
                <td><a href="https://www.metu.edu.tr/" target="_blank">Middle East Technical University, Turkey</a></td>
            </tr>
            <tr>
                <td>Chunghau Lee</td>
                <td>MS</td>
                <td>2005</td>
                <td><a href="https://www.amgen.com" target="_blank">Amgen</a></td>
            </tr>
            <tr>
                <td>Tamer Kahveci</td>
                <td>PhD</td>
                <td>2004</td>
                <td><a href="https://www.ufl.edu" target="_blank">University of Florida</a></td>
            </tr>
            <tr>
                <td>Kris Kvilekval</td>
                <td>PhD</td>
                <td>2004</td>
                <td>Entrepreneur</td>
            </tr>
            <tr>
                <td>Roman Vitenberg</td>
                <td>Postdoc</td>
                <td>2004</td>
                <td><a href="https://www.uio.no/" target="_blank">University of Oslo</a></td>
            </tr>
            <tr>
                <td>Gilad Benjamin</td>
                <td>MS</td>
                <td>2003</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Maureen Heymans</td>
                <td>MS</td>
                <td>2003</td>
                <td><a href="https://www.google.com" target="_blank">Google</a></td>
            </tr>
            <tr>
                <td>Christian Lang</td>
                <td>PhD</td>
                <td>2003</td>
                <td>Entrepreneur</td>
            </tr>
            <tr>
                <td>Hao Sun</td>
                <td>MS</td>
                <td>2003</td>
                <td><a href="https://www.microsoft.com" target="_blank">Microsoft</a></td>
            </tr>
            <tr>
                <td>Jeff Bogda</td>
                <td>PhD</td>
                <td>2002</td>
                <td>Entrepreneur</td>
            </tr>
            <tr>
                <td>Fengliang Hu</td>
                <td>MS</td>
                <td>2001</td>
                <td><a href="https://www.hp.com" target="_blank">HP</a></td>
            </tr>
            <tr>
                <td>Greg Johnson</td>
                <td>MS</td>
                <td>2001</td>
                <td><a href="https://www.microsoft.com" target="_blank">Microsoft</a></td>
            </tr>
            <tr>
                <td>Sandeep Bhatia</td>
                <td>MS</td>
                <td>1999</td>
                <td><a href="https://www.cisco.com" target="_blank">Cisco</a></td>
            </tr>
            <tr>
                <td>Jerry James</td>
                <td>PhD</td>
                <td>1999</td>
                <td><a href="https://www.ku.edu" target="_blank">University of Kansas</a></td>
            </tr>
            <tr>
                <td>K V Ravi Kanth</td>
                <td>PhD</td>
                <td>1999</td>
                <td><a href="https://www.firsthelpfinancial.com" target="_blank">First Help Financial</a></td>
            </tr>
            <tr>
                <td>Raimondas Lencevicius</td>
                <td>PhD</td>
                <td>1999</td>
                <td><a href="https://www.nuance.com" target="_blank">Nuance Communications</a></td>
            </tr>
            <tr>
                <td>Sean Brydon</td>
                <td>MS</td>
                <td>1998</td>
                <td><a href="https://www.oracle.com/java/" target="_blank">Sun (Now part of Oracle)</a></td>
            </tr>
            <tr>
                <td>Suk Lee</td>
                <td>MS</td>
                <td>1998</td>
                <td><a href="https://www.oracle.com" target="_blank">Oracle</a></td>
            </tr>
            <tr>
                <td>Jing Wang</td>
                <td>MS</td>
                <td>1998</td>
                <td><a href="https://www.microsoft.com" target="_blank">Microsoft</a></td>
            </tr>
            <tr>
                <td>Chris Jones</td>
                <td>MS</td>
                <td>1996</td>
                <td><a href="https://www.tandem.net" target="_blank">Tandem (Now part of Hewlett Packard Enterprise)</a></td>
            </tr>
            <tr>
                <td>Manhoi Choy</td>
                <td>PhD</td>
                <td>1994</td>
                <td><a href="https://www.ust.hk/" target="_blank">HKUST</a></td>
            </tr>
        </tbody>
    </table>
</div>

