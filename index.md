---
layout: default
title: Home
navId: 10
---

## Welcome

This is site is currently under construction. It's meant to be the site for Church For Life in Emerald, Victoria, Australia. It doesn't have much on it at the moment, but that will change as we move towards final release under its eventual domain name. Also, many of the site's functions are, well, to put it bluntly, non-functional; and it has some styling problems on the contact page. Oh well, you can't have everything. These problems will also be rectified soon. However, most of the work is done, and at least you've got a good idea of what it's going to look like in its completed state. :)

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
