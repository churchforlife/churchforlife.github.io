---
layout: default
title: About
navId: 50
---

## About Us

![ACC logo](/img/acclogo.png)

Church for Life is one of the only remaining Pentecostal churches established in the Dandenong ranges, having been planted by The Assemblies of God in Victoria. The church has existed for almost 30 years and has also been known as "Emerald Christian Life Church" and "Emerald Assembly of God."

Pastor Malcolm Doswell and his wife Stacey have been members of the church since 1989 and took over the leadership of the church in 1997 after Mal resigned from Victoria Police. In the last few years the congregation of the church has been wrestling with the question of "What is church?"

The journey we have undertaken has been difficult at times with many different ideas and concepts, but most had at their core the idea of simplifying the idea of church: being more connected with each other, a greater sense of community, and growing in our relationship with God. Our vision statement simply became "Glorifying God - Growing people."

As a result of this journey we have seen much stronger connections between people in the congregation, developing connections within our local community and a new found love for the things of God. Our services are not so highly organised that there is no room for the Holy Spirit to move. There is normally a time of worship and a sermon along with time for people to share their own God experiences from the week. We are encouraged by the stories we hear and are reminded that God still uses ordinary people in the execution of his will.

Pentecostal churches believe in the power of the Holy Spirit operating today. In the Gospel of Luke Jesus is recorded as saying, “The Spirit of the Lord is on me, because he has anointed me to proclaim good news to the poor. He has sent me to proclaim freedom for the prisoners and recovery of sight for the blind, to set the oppressed free, to proclaim the year of the Lord’s favour." We are commanded to do as He did in John 14:12 where Jesus says, "Very truly I tell you, whoever believes in me will do the works I have been doing, and they will do even greater things than these, because I am going to the Father."

We do not consider our services to be seeker sensitive, rather, we examine the Bible and see what it has to say to us in regard to the plan and purpose of God for our lives. The task of reaching the lost is done outside the four walls of the church and backed up by the weekly meetings of Christian believers worshiping God.

In this way we hope to influence the world in which we live and remain strong in our own faith. Growing people in God is not something we do, it is something that God accomplishes. We provide a place where the Holy Spirit can do the work of changing hearts and reclaiming lives.

In short, we are a group of believers who look to the Holy Spirit for the power to do what we are each called to do in a world that appears to have lost its way. We corporately Glorify God and provide a safe place where He is Growing People. We hold true to the basic tenants of the protestant christian creeds and strive to be living examples of Christ.

<!-- <div class="separator"></div> -->

## The Team

Church for life is run by a close-knit team with years of experience doing... er... whatever it is that they do (look, I'm just a web developer, okay? ;)

<ul id="teamList">
  {% assign people = site.people | sort: 'rank' %}
  {% for person in people %}
    <li class="person">
        <div class="teamHeader"><div><img class="mugshot" alt="{{ person.name }}" src="{{ person.photo }}"></div><div class="namePosition"><p class="name">{{ person.name }}</p><p class="position">{{ person.position }}</p></div></div>
        <div class="bio">{{ person.content }}</div>
    </li>
  {% endfor %}
</ul>
