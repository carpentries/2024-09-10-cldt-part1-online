---
layout: workshop      # DON'T CHANGE THIS.
root: .               # DON'T CHANGE THIS EITHER.
curriculum: "Collaborative Lesson Development Training" # DON'T CHANGE THIS EITHER. (THANK YOU.)
part: "1"         # The part of the lesson development training curriculum being taught at this event: "1" or "2"
venue: ""        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "W3"      # "W3" for centrally organized online trainings or lowercase two-letter ISO country code such as "fr" of the host institution if applicable (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latitude: "45"        # decimal latitude of training venue (use https://www.latlong.net/)
longitude: "-1"       # decimal longitude of the training venue (use https://www.latlong.net)
humandate: "10-13 September, 2024"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "09:00-13:00 CEST"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2024-09-10      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2024-09-13        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Toby Hodges", "Aleksandra Nenadic"] # boxed, comma-separated list of trainers' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: [""]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
contact: ["tobyhodges@carpentries.org"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
etherpad: https://codimd.carpentries.org/2024-09-10-cldt-part1-online            # optional: URL for the workshop CodiMD/Etherpad if there is one
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<!-- See instructions in the comments below for how to edit specific sections of this training event template. When you are done, rename the file to index.md (replacing the default version of that file, used for Instructor Trainig events)-->

<!--
  HEADER

  Edit the values in the block above to be appropriate for your event.
  If the value is not 'true', 'false', 'null', or a number, please use
  double quotation marks around the value, unless specified otherwise.
  And run 'tools/check' *before* committing to make sure that changes are good.
-->

<img src="fig/CLDT-hex-sticker.svg" alt="" width="20%"/>{: style="float: right"}

<!--
  EVENTBRITE

  This block includes the Eventbrite registration widget if
  'eventbrite' has been set in the header.  You can delete it if you
  are not using Eventbrite, or leave it in, since it will not be
  displayed if the 'eventbrite' field in the header is not set.
-->
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="248px"
  scrolling="auto">
</iframe>
{% endif %}

<h2 id="general">General Information</h2>

<!--
  INTRODUCTION

  Edit the general explanatory paragraph below if you want to change
  the pitch.
-->

<p>
<a href="{{ site.carpentries_site }}">The Carpentries</a> is a community of practice centered around teaching foundational
  coding and data science skills to researchers worldwide.
  This Lesson Developer Training teaches good practices in lesson design and development, and collaboration skills, using open source infrastructure.
  The target audience is groups of collaborators with an idea for a new lesson they would like to create together, especially if that lesson is intended for short-format training (e.g. part or all of a two-day workshop).
</p>

<h3>What is taught in this training?</h3>

<p>After attending Carpentries Lesson Developer Training, participants will be able to:</p>

* collaboratively develop and publish lessons using The Carpentries lesson infrastructure (aka [The Carpentries Workbench](https://carpentries.github.io/workbench/))
* identify and characterise the target audience for a lesson.
* define SMART learning objectives.
* explain the pedagogical value of authentic tasks.
* create exercises for formative assessment.
* explain how considerations of cognitive load can influence the pacing, length, and organisation of a lesson.
* configure and maintain accessible and usable lesson repositories using best practices, readily available for collaboration.
* identify and correct accessibility issues in a Carpentries lesson.
* update and improve lesson material guided by feedback and reflection from teaching.
* review and provide constructive feedback on lessons.

<h3>What is <em>not</em> taught in this training?</h3>

<p> Because we have only limited time, some things are beyond the scope of this training. We will
not be learning:</p>

* How to track changes and manage branches with Git. To learn these skills, we recommend that you follow the lessons from Library Carpentry and Software Carpentry:
    * [Library Carpentry: Introduction to Git](https://librarycarpentry.org/lc-git/)
    * [Version Control with Git](https://swcarpentry.github.io/git-novice/)
* How to teach a lesson in a workshop. [The Carpentries Instructor Training]({{ site.training_site }}) teaches foundational skills for excellent teaching.


<h3>What to expect in this part of the training</h3>

<p> Lesson Developer Training events are hands-on throughout:
short lessons are interspersed with frequent practical exercises, through which trainees construct the basic outline of their lesson and begin to fill in some of the detail.
For more information, see <a href="{{ site.lessondev_training_site }}">the Lesson Developer Training Curriculum</a>.
</p>

<p>
The training takes place in two parts separated by an extended break.
</p>

{% if page.part == "1" %}
<p>
This first part focusses on backward lesson design and techniques for the development of effective exercises and accessible lesson content.
Trainees will define the target audience and intended learning outcomes of their lesson,
produce an outline of the lesson content and narrative,
prepare exercises and examples for a chosen section,
and start building this material into an open source lesson website.
</p>
<p>
Trainees are required to trial part of their new lesson with a real audience during the break between this first part and the conclusion of the training.
When they return for the second and final part of the training, participants will reflect on this experience and discuss how they will approach the remaining stages of lesson development.
</p>
{% elsif page.part == "2" %}
<p>
In this second and final part of the training, participants will reflect on the experience of trialling their new lesson content,
the remaining stages of lesson development,
and some techniques and tools they can use to collaborate more effectively on their open source lesson project.
</p>
{% else %}
<div class="alert alert-warning">
You have not specified which part of Lesson Developer Training will be taught at this event.
The training part is configured in the <code>part</code> field of the YAML header for this page (<code>index.md</code>).
Expected values for <code>part</code> are <code>"1"</code> and <code>"2"</code>.
The current value is: <code>{{ page.part }}</code>.
</div>
{% endif %}

<h3>Code of Conduct</h3>

All participants are required to abide by The Carpentries <a href="{{
site.swc_site }}/conduct/">Code of Conduct</a>.



{% assign begin_address = page.address | slice: 0, 4 | downcase  %}
{% if page.address == "online" %}
{% assign online = "true_private" %}
{% elsif begin_address contains "http" %}
{% assign online = "true_public" %}
{% else %}
{% assign online = "false" %}
{% endif %}
<!--
  LOCATION

  This block displays the address and links to maps showing directions
  if the latitude and longitude of the event have been set.  You
  can use http://itouchmap.com/latlong.html to find the lat/long of an
  address.
  -->
<h3 id="where">Where</h3>


{% if online == "false" %}
<p id="venue">
  {{page.address}}.
  {% if page.latitude and page.longitude %}
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latitude}}&mlon={{page.longitude}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latitude}},{{page.longitude}}">Google Maps</a>.
  {% endif %}
</p>
{% elsif online == "true_public" %}
<p id="venue">
  Online at <a href="{{page.address}}">{{page.address}}</a>.
  The training will be conducted using the Zoom video conferencing platform. No log-in is needed.
  However, if you have not used Zoom before, please click the link a few minutes early as it may prompt you to
  install the Zoom app or browser extension. You should have received a connection link in the same email that
  directed you to this website. If you found this page by another means and did not receive the connection link,
  please check your spam folder and email instructor.training@carpentries.org with your Trainers (contact details below) on cc.
</p>
{% elsif online == "true_private" %}
<p id="venue">
  This training will take place online.
  The instructors will provide you with the information you will need to connect to this meeting.
</p>
{% endif %}

<h4 id="accessibility">Accessibility</h4>

We are committed to making this training
accessible to everybody.
{% if online == "false" %}Organisers have checked that:

<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
{% endif %}

Materials will be provided in advance of the event.

We do not require participants to provide documentation of disabilities or disclose any unnecessary personal information. 
However, we do want to help create an inclusive, accessible experience for all participants.
We encourage you to share any information that would be helpful to make your Carpentries experience accessible.
To request an accommodation for this training, please fill out the
<a href="https://carpentries.typeform.com/to/B2OSYaD0">accommodation request form</a>.
If you have questions or need assistance with the accommodation form please <a href="mailto:team@carpentries.org">email us</a>.

<h3>How to Prepare for Lesson Developer Training</h3>

<p>
Before the training, please <strong>complete our pre-training survey</strong>.
You will receive a custom link for your event when you receive your connection information.
</p>
<p>Before joining the first training session, take a few minutes to think about and note down your answers to the following questions:
<ol>
    <li>What is the topic of the lesson that you plan to develop based on this training?</li>
    <li>Have you created training material on this topic before?</li>
    <li>What is motivating you to create this lesson?</li>
</ol>
</p>
<h4>Prerequisite Knowledge</h4>
<p>
Before joining Collaborative Lesson Development Training, participants should be able to:
<ol>
  <li>write formatted text - bold and italic, headings, links, bullet point and numbered lists - with Markdown.</li>
  <li>log into <a href="https://github.com/" target="_blank">GitHub.com</a> and create and edit files using the GitHub web interface.</li>
</ol>
</p>
<p>
If you need to learn or refresh these skills before the training,
visit our <a href="https://carpentries.github.io/lesson-development-training/markdown-github-primer.html">Primer on Markdown and GitHub</a> for links to resources to help learn these skills.
</p>

<h3>Attendance and Cancellation</h3>
Trainees who miss more than 1 hour of the training may be marked absent.
Lesson Developer certification cannot be completed without full attendance at
an Instructor Training event. If you unexpectedly need to miss more than
1 hour of your event, please contact your Trainers (contact info below).

For events in which registration occurs through The Carpentries via Eventbrite,
cancellation may be performed in Eventbrite up to the start of the event.
Cancelled seats cannot be filled after the 1 week registration deadline for these events,
so we ask that you only cancel if absolutely necessary.

<h3 id="contact">Contact</h3>
<p>
Please email
{% if page.contact %}
  {% for contact in page.contact %}
    {% if forloop.last and page.contact.size > 1 %}
      or
    {% else %}
      {% unless forloop.first %}
      ,
      {% endunless %}
    {% endif %}
    <a href='mailto:{{contact}}'>{{contact}}</a>
  {% endfor %}
{% else %}
  to-be-announced
{% endif %}
for more information.
</p>

<hr/>


<hr/>

<h2 id="materials" name="materials">Training Materials and Schedule</h2>

<p>
  Please see <a href="{{ site.lessondev_training_site }}/instructor/index.html#schedule">the Lesson Developer Training Curriculum</a> for course material and sample schedule for a 6 half-day event.
</p>
<p>
  The training is divided into two parts and includes an extended break between the two parts.
  Part 1 ends with a wrap-up session after the section on <em>Preparing to Teach</em>.
  Part 2 begins with a reflection on the lesson trial runs trainees completed during the break, then switches focus to discuss effective strategies and tools for collaboration.
</p>


<!--
  CODIMD FOR LESSON DEVELOPER TRAINING
  A template CodiMD for notetaking at Collaborative Lesson Development Training
  is available at https://codimd.carpentries.org/cldt-notes-template.
  To create a CodiMD for your training, navigate to
      http://codimd.carpentries.org/YYYY-MM-DD-cldt-site
  where 'YYYY-MM-DD-cldt-site' is the identifier for your training,
  e.g., '2015-06-10-cldt-esu'.
  Then copy the contents of the template CodiMD and paste it into your new document.
  If you find that the template is outdated or needs fixing, please open an issue
  on the training curriculum repository: https://github.com/carpentries/lesson-development-training/issues/new
-->

{% if page.etherpad %}
<hr/>

<p id="codimd">
  <strong>CodiMD:</strong> <a href="{{page.etherpad}}">{{page.etherpad}}</a>.
  <br/>
  We will use this CodiMD document for chatting, taking notes, and sharing URLs and bits of code during the training.
</p>

{% endif %}

<h2 id="pre_workshop_survey">Surveys</h2>

<p>
  Before attending the training, please fill out <a href="{{ site.lessondev_pre_survey }}{{ site.github.project_title }}">our pre-training survey</a>.
</p>


<p>
  After the training, please fill out <a href="{{ site.lessondev_post_survey }}{{ site.github.project_title }}">our post-training survey</a>.
</p>
