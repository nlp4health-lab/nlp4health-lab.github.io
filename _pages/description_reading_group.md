---
permalink: /reading-group-meetings/
layout: page
---
## NLP4Health Reading Group
Our reading group is an opportunity for members of the lab to come together and discuss research papers relevant to our projects.
The major goals of our reading group meetings are:
* To stay abreast of the recent trends and developments in NLP.
* To discuss fundamental concepts and the mathematical foundations of AI.
* To broaden our perspective by getting to know each other's research interest.
* To share ideas and adapt discussed concepts to our own work/research.
* To develop presentation and communication skills.

Upcoming events in the Reading group series are listed in the agenda below.
  
<h3>Next meetings</h3>

<table class="reading-group-agenda">
  <thead>
    <tr>
      <th>Date</th>
      <th>Paper Name</th>
      <th>Presenter</th>
    </tr>
  </thead>
  <tbody>
    {% assign sorted_meetings = site.reading_group_meetings | sort: 'date' %}
    {% for meeting in sorted_meetings %}
      {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
      {% assign nowunix = nowunix | plus: 0 %}
      {% capture meetingtime %}{{ meeting.date | date: '%s'}}{% endcapture %}
      {% assign meetingtime = meetingtime | plus: 0 %}
      {% if meetingtime > nowunix %}
      <tr>
        <td>{{ meeting.date | date: "%B %d, %Y" }}</td>
        <td>
          <a href="{{ meeting.link }}">{{ meeting.title }}</a>
          {% if meeting.pdf %}
            (<a href="{{ meeting.pdf }}">PDF</a>)
          {% endif %}
          {% if meeting.slides %}
            (<a href="{{ meeting.slides }}">Slides</a>)
          {% endif %}
        </td>
        <td>{{ meeting.presenter }}</td>
      </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>

<br/>
<br/>

<h3>Previous meetings</h3>

<table class="reading-group-agenda">
  <thead>
    <tr>
      <th>Date</th>
      <th>Paper Name</th>
      <th>Presenter</th>
    </tr>
  </thead>
  <tbody>
    {% assign sorted_meetings = site.reading_group_meetings | sort: 'date' | reverse %}
    {% for meeting in sorted_meetings %}
      {% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
      {% assign nowunix = nowunix | plus: 0 %}
      {% capture meetingtime %}{{ meeting.date | date: '%s'}}{% endcapture %}
      {% assign meetingtime = meetingtime | plus: 0 %}
      {% if meetingtime <= nowunix %}
      <tr>
        <td>{{ meeting.date | date: "%B %d, %Y" }}</td>
        <td>
          <a href="{{ meeting.link }}">{{ meeting.title }}</a>
          {% if meeting.pdf %}
            (<a href="{{ meeting.pdf }}">PDF</a>)
          {% endif %}
          {% if meeting.slides %}
            (<a href="{{ meeting.slides }}">Slides</a>)
          {% endif %}
        </td>
        <td>{{ meeting.presenter }}</td>
      </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>

<p>
  Note: You are welcome to attend our reading group meetings online (via Teams) or in person if you are at the Amsterdam UMC. Please email
  <a href="mailto:a.testoni@amsterdamumc.nl">the reading group organiser for this cycle</a> for details.
</p>
 
