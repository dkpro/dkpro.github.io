---
layout: page
title: Dedicated build job for documentation
subheadline: A fast-lane for the documentation
meta_description: Building the asciidoc documentation of a multi-module Maven project on Jenkins using the DocLinks plugin.
description:
categories:
    - developer
tags:
    - jenkins
    - asciidoc
    - maven
    - howto
---

Maintaining documentation along with the code is a great thing because that way you make sure you always have proper documentation for each version you have release, not only for the latest as in the typical wiki-based documentation. And here, asciidoc and the asciidoc-maven-plugin provide a great service because you can actually build the docs as part of regular builds with Jenkins or Travis or the likes, and provide up-to-date documentation on your website even for the latest SNAPSHOT versions.

However, while a build is running, the links to the documentation usually do not work - and builds can run for quite a while and be triggered often.

The workaround is adding a separate fast build specifically for the documentation module - and this is what we are going to do now using [Jenkins][1] and the [DocLinks Plugin][2]:

* Setting up the build
  * Create a new Maven build for your project
  * Enter the repository URL
  * Configure your build trigger (e.g. Poll SCM) 
  * In the *Build* section, use the goal `-pl my-doc-module clean package`
    * Replace *my-doc-module* with the name of the module that contains your asciidoc
    * The `-pl my-doc-module` argument makes sure to only build that single module of your multi-module project
  * Save
* Publishing the documentation
  * Click on the *Modules* link in the left sidebar
  * Locate your documentation module and click on it
  * Within the module, click on *Configure* in the left sidebar
  * Activate *Publish documents*
  * Add your documentation, e.g.
    * Title: *User Guide and Reference*
    * Directory to archive: *target/generated-docs*
    * Index file: *user-guide.html*
  * Save

The next time you run a build, you will find links to the generated documentation *within the module*.
So again, if you are looking at your project (not at the latest build, but at the general project page),
click again on *Modules* and on your documentation module. The links are listed under *Document links*.

 [1]: https://jenkins-ci.org
 [2]: https://wiki.jenkins-ci.org/display/JENKINS/DocLinks+Plugin
 