---
layout: post
title: "Best Hosted Continuous Integration Services for a Private Repository"
date: 2014-10-05
tags: devops
description: |
  I tried to use them all and made a comparison
  chart, which may help you to chose the most
  suitable continuous integration service for a private project
keywords:
  - continuous integration
  - hosted continuous integration
  - cloud continuous integration
  - continuous integration in cloud
  - continuous integration service
categories: jcg
style: |-
  .x-col1 { width: 6em; }
  .x-col2 { width: 4em; }
  .x-colX { width: 2em; }
  .x-head { height: 6em; }
  .x-hr { border-top: 1px solid gray; }
  .x-right { text-align: right; }
  .x-bottom { vertical-align: bottom; }
  .x-vertical {
    vertical-align: bottom;
    white-space: nowrap;
  }
  .x-vertical div {
    text-align: left;
    transform: translate(0, -.5em) rotate(270deg);
    width: 2em;
  }
  .x-build {
    height: 18px;
  }
---

Every project I'm working with starts with a setup of
[continuous integration]({% pst 2016/aug/2016-08-01-continuous-integration-maturity %})
pipeline. I'm a big fan of cloud services,
that's why I was always using [Travis](http://www.travis-ci.org). A few of
my clients questioned this choice recently, mostly because
of the price. So I decided to make a brief analysis of the market.

I configured [Rultor](https://github.com/yegor256/rultor),
an open source project, in every CI service I managed to find.
All of them are free for open source projects.
All of them are hosted and do not require any server installation
Here they are, in order of my personal preference (first four are
the best and highly recommended):

<table>
<colgroup>
<col class="x-col1"/>
<col class="x-col2"/>
<col class="x-colX"/>
<col class="x-colX"/>
<col class="x-colX"/>
<col class="x-colX"/>
<col class="x-colX"/>
</colgroup>
<thead>
<tr class="x-head">
  <td><!--name--></td>
  <td class="x-bottom x-right">Price</td>
  <td class="x-vertical"><div><span>Linux<sup>1</sup></span></div></td>
  <td class="x-vertical"><div><span>Windows<sup>2</sup></span></div></td>
  <td class="x-vertical"><div><span>MacOS<sup>3</sup></span></div></td>
  <td class="x-vertical"><div><span>Pull requests<sup>4</sup></span></div></td>
  <td class="x-vertical"><div><span>Log compress<sup>5</sup></span></div></td>
  <td class="x-vertical"><div><span>Docker<sup>6</sup></span></div></td>
  <td class="x-bottom">Build</td>
</tr>
</thead>
<tbody>
<tr><td><a href="http://www.travis-ci.org">Travis</a></td>
  <td class="x-right"><a href="https://travis-ci.com/plans">$129/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td><a href="https://travis-ci.org/yegor256/rultor">
    <img src="https://travis-ci.org/yegor256/rultor.svg?branch=master" class="x-build"/></a></td>
  </tr>
<tr><td><a href="http://www.shippable.com">Shippable</a>&#x263A;</td>
  <td class="x-right"><a href="http://www.shippable.com/pricing.html">free</a> (!)</td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td><a href="https://app.shippable.com/projects/542e8fb980088cee586d3806/builds/latest">
    <img src="https://api.shippable.com/projects/542e8fb980088cee586d3806/badge?branchName=master" class="x-build"/></a></td>
  </tr>
<tr><td><a href="http://www.appveyor.com">AppVeyor</a></td>
  <td class="x-right"><a href="http://www.appveyor.com/pricing">$39/mo</a></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center">?</td>
  <td class="center">&mdash;</td>
  <td><a href="https://ci.appveyor.com/project/yegor256/rultor/branch/master">
    <img src="https://ci.appveyor.com/api/projects/status/sulqrjerl27qqtl7/branch/master?svg=true" class="x-build"/></a></td>
  </tr>
<tr><td><a href="http://www.wercker.com">Wercker</a></td>
  <td class="x-right">$350/mo</td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td><a href="https://app.wercker.com/project/bykey/0e6506c69e078b7692e50b240c034524">
    <img src="https://app.wercker.com/status/0e6506c69e078b7692e50b240c034524/s%20wercker status" class="x-build"/></a></td>
  </tr>
<tr><td colspan="9" class="x-hr"></td></tr>
<tr><td><a href="http://www.semaphoreapp.com">SemaphoreApp</a></td>
  <td class="x-right"><a href="https://semaphoreapp.com/pricing">$29/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="http://www.drone.io">Drone</a></td>
  <td class="x-right"><a href="https://drone.io/pricing">$25/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="https://magnum-ci.com/pricing">Magnum-CI</a></td>
  <td class="x-right">?</td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center">?</td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="http://www.snap-ci.com">Snap-CI</a>&#x263A;</td>
  <td class="x-right"><a href="https://snap-ci.com/plans">$30/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center">?</td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="http://www.codeship.io">CodeShip</a>&#x263A;</td>
  <td class="x-right"><a href="https://codeship.io/pricing">$49/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center">?</td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  </tr>
<tr><td><a href="http://www.circleci.com">CircleCI</a>&#x263A;</td>
  <td class="x-right"><a href="https://circleci.com/pricing">$19/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="http://ci.solanolabs.com">SonoLabs</a></td>
  <td class="x-right"><a href="https://www.solanolabs.com/#pricing">$15/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center">?</td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="http://www.hosted-ci.com">Hosted-CI</a></td>
  <td class="x-right"><a href="https://hosted-ci.com/#plans">$49/mo</a></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center">?</td>
  <td class="center">?</td>
  <td class="center">&mdash;</td>
  </tr>
<tr><td><a href="http://www.deploybot.com">DeployBot</a></td>
  <td class="x-right"><a href="https://signup.deploybot.com/signup/new">$15/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center">?</td>
  <td class="center">?</td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="http://www.vexor.io">Vexor</a></td>
  <td class="x-right"><a href="http://vexor.io/">&cent;90/hr</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center">?</td>
  <td class="center">?</td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
<tr><td><a href="http://www.greenhouseci.com">GreenHouseCI</a></td>
  <td class="x-right"><a href="https://greenhouseci.com/pricing.html">$49/mo</a></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center"><i class="icon-no red"></i></td>
  <td class="center"><i class="icon-yes green"></i></td>
  <td class="center">?</td>
  <td class="center">?</td>
  <td class="center"><i class="icon-no red"></i></td>
  </tr>
</tbody>
</table>

<!--more-->

If you know any other good
[continuous integration]({% pst 2014/oct/2014-10-08-continuous-integration-is-dead %}) services,
[email me](/about-me.html), I'll review and add them to this list.
BTW, here is a ["full" list](https://en.wikipedia.org/wiki/Comparison_of_continuous_integration_software)
of continuous integration software and services.

By the way, a few platforms from this list contacted me and asked
to review them again. Some even offered me money to put them higher
in the list (kidding). Anyway, it's up to you to decide whether it's a
good sign or not (I think it's good, they care about their PR). I marked
them in the list with &#x263A; emoji.

## Best Four

{% badge /images/2014/10/travis.png 92 http://www.travis-ci.org %}

[**Travis**](http://www.travis-ci.org) is
the best platform I've seen so far. Mostly because
it is the most popular. Perfectly integrates with
GitHub and has proper documentation. One important
downside is the price of $129 per month. "With this money
you can get a dedicated EC2 instance and install Jenkins there" &mdash;
some of my [clients]({% pst 2015/jan/2015-01-26-happy-boss-false-objective %})
say. I strongly disagree, since Jenkins will
require a 24x7 administration, which costs way more than $129, but
it's always difficult to explain.

{% badge /images/2014/10/shippable.png 92 http://www.shippable.com %}

[**Shippable**](http://www.shippable.com) was easy to configure
since it understands `.travis.yml` out of the box.
The user interface is easy to navigate since it doesn't
have "settings" page at all (or I didn't find it). Everything is
configured via `shippable.yml` file in the repository. The service
looks stable and robust, no complains so far. As soon as they make
Docker containers available for all builds I will put them to the
first position and will migrate all my projects there.

{% badge /images/2014/10/wercker.png 92 http://www.wercker.com %}

[**Wercker**](http://www.wercker.com) is a European product
from Amsterdam, which is still in beta and that's why free
for all projects. The platform looks very promising. It is still
free for private repositories and is backed up by
[investments](https://gigaom.com/2014/10/01/wercker-takes-in-2-4-million-to-help-developers-test-their-code-in-the-cloud/).
They also have an interesting concept of build "boxes", which
can be pre-configured similar to Docker containers.
It works rather stable for the last few months, no complains so far.

{% badge /images/2014/10/appveyor.png 92 http://www.appveyor.com %}

[**AppVeyor**](http://www.appveyor.com) is the only one
that runs Windows builds. Even though I'm working mostly with
Java and Ruby, which are expected to be platform independent, they
very often appear to be exactly the opposite. When your build
succeeds on Linux, there is almost no guarantee it will pass on
Windows or Mac. I'm planning to use AppVeyor in every project,
in combination with some other CI service. Here is how I integrate
[Maven builds]({% pst 2015/jan/2015-01-10-windows-appveyor-maven %})
with AppVeyor.

## Others

{% badge /images/2014/10/semaphoreapp.png 64 http://www.semaphoreapp.com %}

[**SemaphoreApp**](http://www.semaphoreapp.com) is easy to
configure and work with. It makes an impression of a light-weight
system, which I generally appreciate. As a downside, they
<span class="strike">don't have any Maven pre-installed</span>
have an old version of Maven, but this was solved easily with a short
custom script that downloads and unpacks the latest Maven. Another downside is
that they are not configurable through a file (like `.travis.yml`) &mdash;
you should do everything through a UI. They also support
[caching between builds](https://semaphoreapp.com/docs/caching-between-builds.html).

{% badge /images/2014/10/magnum.png 64 http://www.magnum-ci.com %}

[**Magnum-CI**](https://magnum-ci.com/pricing) is a very lightweight
and young system. It doesn't connect automatically to GitHub,
so you should do some manual operations of adding a web hook.
Besides that, works just fine.

{% badge /images/2014/10/snap.png 64 http://www.snap-ci.com %}

[**Snap-CI**](http://www.snap-ci.com) is a product of
ThoughtWorks, an author of [Go](http://www.go.cd/),
an open source continuous integration server. It looks a bit more
complicated than others, giving you an ability to define "stages"
and combine them into pipelines. I'm not sure yet how these mechanisms
may help in small and medium size projects we're mostly working with,
but they look "cool". There is also a very unfortunate limitation of
2Gb RAM per build &mdash; some of my Java projects fail because of that.
Besides that, they don't give full access to the build server, for example
we can't modify anything in `/etc` &mdash; it is a show-stopper for us.

{% badge /images/2014/10/drone.png 64 http://www.drone.io %}

[**Drone.io**](http://www.drone.io) works fine, but their support
didn't reply to me when I asked for a Maven version update
(they have an old version pre-installed). Besides
that, their badge is not updated correctly in GitHub README.md &mdash;
when the build is broken, the badge stays green... very annoying.

{% badge /images/2014/10/codeship.png 64 http://www.codeship.io %}

[**CodeShip**](http://www.codeship.io) works fine, but their web UI
looks a bit out-dated. Besides that, they promise to work with pull
requests, but I didn't manage to configure them. They simply
don't notify our pull requests in GitHub, even though they build them.
Maybe I'll find a way, so far it's not clear.

{% badge /images/2014/10/circleci.png 64 http://www.circleci.com %}

[**CircleCI**](http://www.circleci.com) I still don't know why my build
fails there. Really difficult to configure and understand
what's going on. Trying to figure it out...

{% badge /images/2014/10/solanolabs.png 64 http://www.solanolabs.com %}

[**SolanoLabs**](http://www.solanolabs.com) looks rather immature and
difficult to configure. They don't even support automatic GitHub hook
configuration when new repository is added. However, their sales spams me
rather aggressively :)

{% badge /images/2014/10/hostedci.png 64 http://www.hosted-ci.com %}

[**Hosted-CI**](http://www.hosted-ci.com) is for iOS/OSX only. They don't
give anything for free, even for open source projects. I didn't have a chance
to test them yet.

{% badge /images/2014/10/cloudbees.png 64 http://www.cloudbees.com %}

[**CloudBees**](http://www.cloudbees.com) is basically a hosted Jenkins.
I don't really like Jenkins, that's why can't recommend this platform.

{% badge /images/2014/10/deploybot.png 64 http://www.deploybot.com %}

[**DeployBot**](https://deploybot.com/) doesn't even allow me to login
via GitHub, huh? They seem to be more "deployment" oriented, not just
continuous integration.

{% badge /images/2014/10/vexor.png 64 http://www.vexor.com %}

[**Vexor**](http://vexor.io/) looks nice and offers a rather unique
billing model &mdash; they charge per build, not per month. I would definitely
recommend to give it a try. I couldn't make it work though...

{% badge /images/2014/10/greenhouseci.png 64 http://www.greenhouseci.com %}

[**GreenHouseCI**](http://greenhouseci.com/) is a CI platform for
mobile apps (iOS, Android, etc.) Seems to be interesting, I just don't have
a full scale mobile app to test it against.

<hr/>

**Ship.io** is [dead](https://ship.io/ship-io-is-shutting-down/).

[**ZeroCI**](http://www.zeroci.com) is dead (as of 28-Aug-2016).

<hr/>

BTW, if you don't like the idea of keeping continuous integration
in cloud, consider these on-premise software packages (in order or preference):
[Jenkins](http://jenkins-ci.org/),
[TeamCity](http://www.jetbrains.com/teamcity/),
[Go](http://www.thoughtworks.com/products/go-continuous-delivery),
[Strider](http://stridercd.com/),
[BuildBot](http://buildbot.net/).

Keep in mind that no matter how good and expensive your
continuous integration service is, it
[won't help you]({% pst 2014/oct/2014-10-08-continuous-integration-is-dead %})
unless you make your
[master branch read-only]({% pst 2014/jul/2014-07-21-read-only-master-branch %}).

<hr/>

<sup>1</sup> This means that the platform can build your repo
in Linux environment. Almost all of them do that by default, unless
you configure them otherwise.<br/>
<sup>2</sup> Some of them can build on Windows platform.<br/>
<sup>3</sup> MacOS support means that an Objective-C/Swift product can be
built there.<br/>
<sup>4</sup> I mean GitHub pull request support here. Some of them can be
integrated with GitHub and will build pull requests before they are merged.
Build status will be visible in GitHub. A pretty convenient feature.<br/>
<sup>5</sup> Logs compression is a critical feature, at least for me. Most
of my logs are from Maven and without `col -b` they look too long and unreadable.<br/>
<sup>6</sup> Looks like Docker containers must be supported by all of them,
but unfortunately it's not the case. Ideally, all builds should run
in containers.