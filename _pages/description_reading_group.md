---
permalink: /reading-group-meetings/
layout: page
---
## NLP4Health Reading Group
This reading group is an opportunity for members of the lab to come together and discuss recent(or old) research that is seminal in the field and/or relevant to their research while also being pertinent to the general theme of the lab.
The major goals of our reading group meetings are:
* To stay abreast of the recent trends and developments in NLP research.
* To discuss and understand fundamental concepts and mathematical foundations of AI.
* To broaden our persepective by getting to know each other's research interest
* To share ideas and use concepts discussed for own work/research.
* To build a collaborative and productive team environment.
* To develop presentation and communication skills.

The recent and upcoming events in the Reading group series are listed in the agenda below.
<p>
  Note: If you are interested in attending the reading group meetings, kindly reach out via mail to 
  <a href="mailto:i.coimbra@amsterdamumc.nl">the PI</a>.
</p>
  
<h3>Agenda</h3>

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
    {% endfor %}
  </tbody>
</table>