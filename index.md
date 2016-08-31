---
layout: default
title: Home
navId: 10
---

## Welcome

This is an introductory paragraph telling readers this is the website of a church. Yada yada yada. Placeholder text placeholder text placeholder text placeholder text placeholder text placeholder text placeholder text placeholder text. End of paragraph.

<!-- <div class="separator"></div> -->

<div id="latestContainer">
  <div id="news">
    <h2>Latest news</h2>
{% include listGenerator.html printEx=true%}
  </div>
  <div id="comingUp">
    <h2>Coming Up</h2>
{% include coming.html %}
    </div>
</div>
