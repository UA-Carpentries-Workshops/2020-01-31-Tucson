---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "dc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc").  
                      # Be sure to update the Carpentry type in _config.yml as well.  
venue: "The University of Arizona<br>Image Processing Data Carpentry Workshop: Come for the Tucson Rodeo Parade 2020, then learn how to wrangle image data!"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Please check your email for the workshop location"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latlng: "30.231901,88.9495000"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "Feb 22-23, 2020"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 am - 5:00 pm"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2020-02-22      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2020-02-23        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Trisha Adamus", "Mark Meysenburg"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Amirhossein Azami", "Ryan Carlson", "Courtney Comrie", "Gabriela De La Cruz Sanchez", "Reza Ehsani", "Kelsey Gonzalez", "Elaheh Hayati", "Chris Klimowski", "Jina Lee", "Shuailong Li", "Chuan Luo"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["hilgert@bio5.org"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: http://pad.software-carpentry.org/2020-02-22-Tucson # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<h2>Workshop Description</h2>
<p>
The <a href="https://bio5.org/">BIO5 Institute</a>, in partnership with <a href="https://cyverse.org/">CyVerse</a>, the <a href="https://datascience.arizona.edu/">D7 Data Science Institute</a> and the <a href="https://new.library.arizona.edu/">UArizona Libraries</a> is hosting a Data Carpentry workshop in image processing. This workshop will teach core computing and analysis skills to help researchers be more productive and effective.<p>
<p>
Alternating short tutorials with hands-on practical exercises participants will learn to:
<ul>
<li>Recognize scientific questions that could be solved with image processing / computer vision.</li>
<li>Recognize morphometric problems (those dealing with the number, size, or shape of the objects in an image).</li>
<li>Recognize colorimetric problems (those dealing with the analysis of the color or the objects in an image).</li>
</ul>
</p>
<p>
For more detail on workshop objectives see <a href="https://datacarpentry.org/image-processing/01-introduction/">this link</a>.
</p>

<h2>Pre-Requisites</h2>
<p>The workshop assumes you have a working-knowledge of Python and some previous exposure to the Bash shell (a.k.a. Unix, Command Line). These requirements can be fulfilled by:
<ul><li>completing a Software Carpentry Python workshop (such as the one at the UArizona on Feb. 15/16, 2020; see <a href="http://bit.ly/2LdkoMI">http://bit.ly/2LdkoMI</a> for details); or</li>
<li>completing a Data Carpentry Ecology workshop (with Python) and a Data Carpentry Genomics workshop; or</li>
<li>independent exposure to both Python and the Bash shell.</li></ul></p>

<p>If you’re unsure whether you have enough experience to participate in this workshop, please read over <a href="https://datacarpentry.org/image-processing/prereqs/" target='blank'>this detailed list</a>, which gives all of the functions, operators, and other concepts you will need to be familiar with.
</p>

<p><h4><center><strong>Apply for the workshop at <a href="http://bit.ly/2Pj8EcP" target='blank'>http://bit.ly/2Pj8EcP</a>.</strong></center></h4></p>


{% if page.carpentry != site.carpentry %}
<div class="alert alert-warning">
You specified <code>carpentry: {{page.carpentry}}</code> in <code>index.md</code> and
<code>carpentry: {{site.carpentry}}</code> in <code>_config.yml</code>. Make sure you edit both files. After editing <code>_config.yml</code>, you need to run <code>make serve</code> again to 
see the changes take effect locally.
</div>
{% endif %}




<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:
  {{page.address}}.</strong>
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}

<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on. They should have a few specific software packages installed (listed <a href="#setup">below</a>).
</p>

{% comment %}
CODE OF CONDUCT
{% endcomment %}
<p id="code-of-conduct">
<strong>Code of Conduct:</strong>  Everyone who participates in Carpentries activities is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. This document also outlines how to report an incident if needed.
</p>


{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
 If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>
<p>Information about the <a href="http://tucsonrodeo.com/schedule/"><b>Tucson Rodeo Week 2020</b></a></p>
<hr/>

{% comment %} 
SURVEYS - DO NOT EDIT SURVEY LINKS 
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
{% if site.carpentry == "swc" %} 
<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif site.carpentry == "dc" %}
<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif site.carpentry == "lc" %}
<p><a href="{{ site.lc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.lc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% endif %}

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}


<h2 id="schedule">Schedule</h2>
<p>
Day 1 morning
<ul>
  <li><a href="https://datacarpentry.org/image-processing/01-introduction/">Introduction</a></li>
  <li><a href="https://datacarpentry.org/image-processing/02-image-basics/">Image Basics</a></li>
<li><a href="https://datacarpentry.org/image-processing/03-skimage-images/">Image Representation in Skimage</a></li>
</ul>
</p>
<p>
Day 1 afternoon
<ul>
    <li><a href="https://datacarpentry.org/image-processing/04-drawing/">Drawing and Bitwise Operations</a></li>
    <li><a href="https://datacarpentry.org/image-processing/05-creating-histograms/">Creating Histograms</a></li>
</ul>
</p>
<p>
Day 2 morning
<ul>
  <li><a href="https://datacarpentry.org/image-processing/06-blurring/">Blurring Images</a></li>
  <li><a href="https://datacarpentry.org/image-processing/07-thresholding/">Thresholding</a></li>
</ul>
</p>
<p>
Day 2 afternoon
<ul>
  <li><a href="https://datacarpentry.org/image-processing/08-edge-detection/">Edge Detection</a></li>
  <li><a href="https://datacarpentry.org/image-processing/09-connected-components/">Connected Component Analysis</a></li>
  <li><a href="https://datacarpentry.org/image-processing/10-challenges/">Challenges</a></li>
 </ul>
</p>

<p><a href="http://bit.ly/37asaPD">Click for a list and map of nearby eateries.</a></p>

<p>Schedule subject to change if necessary.</p>
<hr/>


{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

<h2 id="setup">Setup</h2>

<p>
For installation instructions, please see the workshop's <a href="https://datacarpentry.org/image-processing/setup/">Setup page</a>.
</p>

<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>


