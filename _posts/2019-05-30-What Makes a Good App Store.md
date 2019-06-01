---
layout: post
title: What Makes a Good App Store?
date: 2019-05-30 00:00 -0600
#date-edit: 2019-04-23 21:27 -0400
categories:
  - Think-Piece
  - Tech
  - Apple
  - Microsoft
  - Google
  - Apps
#excerpt: Objective-C has passed on. This language is no more. It has ceased to be. This is an ex-language.



---

App Stores, or package managers, are necessary these days for handling all the software we love to use. Harken back not so long ago, and we were manually buying updates from Circuit City, driving them home, and installing them manually. Now, if done well, we don't even realize our software is updating.

It's no trivial task, and there are many competing approaches to it. Here, I did a little reasearch into what I think makes a good app store, and how some popular ones stack up against eachother.

<table>
    <thead>
        <tr>
            <th>Feature</th>
            {% for appStore in site.data.appStores.stores %}
            <th class="horiz">{% if appStore.isGui %}{{ appStore.shortName }}{% else %}<code>{{ appStore.shortName }}</code>{% endif %}</th>
            {% endfor %}
        </tr>
    </thead>

    <tbody>
    {% for feature in site.data.appStores.features %}
    <tr>
        <th>{{ feature.name }}</th>
        {% for appStore in site.data.appStores.stores %}
        <td>{{ appStore.features[feature.key] }}</td>
        {% endfor %}
    </tr>
    {% endfor %}
    </tbody>
</table>
