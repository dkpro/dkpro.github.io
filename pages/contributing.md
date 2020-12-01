---
layout: page-fullwidth
title: "Contributing to DKPro"
permalink: "/contributing/"
---

As DKPro is growing and being used more and more outside the UKP Lab, we are getting inquiries on how people can contribute to DKPro… and we are very happy to get these!

### Our model

We chose to adopt a model similar to that of the Apache Foundation, which involves contributors signing and submitting a *contributor license agreement*. These represent a license that the contributor grants to Technische Universität Darmstadt and *covers contributions to all of our projects*. That is, it is it not limited to DKPro Core, but also covers JWPL, Uby, and a growing set of additional projects that we govern at the UKP Lab.

To this end, we adapted the contributor agreements used at Apache for our purposes. In particular, we replaced mentions of the Foundation with mentions of the University (Technische Universität Darmstadt) and added a clause that the agreement is governed by German law. Please read the license agreements carefully before signing them.

The primary contributor agreement is the *Individual Contributor License Agreement* which is submitted by each individual contributing person. However, if that person is working under contract, we ask that their employer sign and file an additional *Corporate Contributor License Agreement* which certifies the consent of the employer with the actions of the contributing person. 

*We ask that you discuss the topic of contribution with your employer even if you plan to create your contributions in your spare time. Being open from the start will avoid problems later and your employer will likely be happy to sign the corporate contributor license agreement after you have discussed the particulars.*

The contributor license agreement represents a license that the contributor gives to Technische Universität Darmstadt (here represented by the UKP Lab) and which allows us to sublicense the contribution. This is particularly important if the contribution was initially made to a part of DKPro that we need to license under the GPL due to third-party dependencies. The contribution might be a first step towards a more generic extension of the framework which we would eventually like to have licensed under the Apache License to maximize its usability. Having separate contributor license agreements allows us to refactor such contributions and to eventually move them from a GPL module to an Apache-licensed module.

### Contributor license agreements

Details on how and where to submit the agreements are included in their respective texts.

   * [Individual Contributor License Agreement]({{ site.url}}/files/icla.txt) (ICLA) - always required
   * [Corporate Contributor License Agreement]({{ site.url}}/files/ccla.txt) (CCLA) - strongly recommended when contributor is employed

*Note: your browser may not correctly detect the UTF-8 encoding in the CLA files. In that case, please switch the encoding in your browser to UTF-8 or right-click on the links, select "Save as", and open the files in a UTF-8–capable editor before printing and signing. You'll know that  the encoding has been properly detected when the umlaut *"ä"* (an 'a' with two dots above) appears in the phrase "*Technische Universität Darmstadt*".

### How to make contributions

Contributions should be submitted by sending a [pull request](https://help.github.com/articles/using-pull-requests/) to the project to which you wish to contribute.  If your contribution addresses an existing bug or feature request listed in the project's issue tracker, please reference it.  (If not, consider opening a new issue before sending your pull request.)

Prolific contributors may eventually be granted write access to the code repositories. Access to the repositories is granted on a per-project basis.

### Contributor attribution

The `CONTRIBUTORS.txt` file is used to keep track of contributors. It is to be used in favor over
author attributions in individual files, e.g. via `@author` tags. For `@author` tags in code copied
from a third-party, see *Integrating third-party code* below.

The reason that we prefer a central place for maintaining the list of contributors is, that

* it is easier to maintain – attribution distributed across files tends to get outdated quickly as code is refactored and people do not update the tags; and
* it is easier to get an overview of all contributors.

The most authoritative and detailed source, however, is the version history of the version control system. That
said, the `CONTRIBUTORS.txt` may mention people that contributed before the code was open-sourced
or who did not have direct commit access to the repository.

### Copyright

All contributions remain under the copyright of the original authors (or their employers).

### Integrating third-party code

Code integrated from third parties by others than their original authors may not have any
copyright notice, `@author` tags, nor other kind of attribution removed. 

Names of authors of third-party code are not to be added to the `CONTRIBUTORS.txt` file. 

In general, integration of third-party code should be avoided. Instead, the required libraries should be specified as dependencies.

Third-party code that is integrated must be compatible with our license. For Apache-licensed modules,
it must be compatible with the Apache license. For GPL-licensed modules, GPLed dependencies are
also OK. In case of doubt, ask the DKPro developer team.

### Code style

We use a style for formatting the source code in {product-name}. Our approach consists of two steps:

* DKPro code formatting profile - the profile configures your IDE to auto-format the code according to
  our guidelines as you go.
* Checkstyle - this tool is used to check if the source code is actually formatted according to our
  guidelines. It is run as part of a Maven build and the build fails if the code is not formatted
  properly.

Here is a brief summary of the formatting rules:
* no tabs, only spaces
* indenting using 4 spaces in Java files and 2 spaces in XML files
* maximum 100 characters per line (with a few exceptions)
* curly braces on the next line for class/method declarations, same line for logic blocks (if/for/...)

We offer a code formatting profile for Eclipse here (right-click on link and select "Save as"):

* **[Eclipse Code Style file]({{ site.url}}/files/DKProStyle_20201201.xml)** (2020-12-01, use for Eclipse 4.17.x (2020-09) and above)
* [Eclipse Code Style file]({{ site.url}}/files/DKProCoreStyle_20170725.xml) (2017-07-25, use for Eclipse 4.7.x and above - deprecated)

In Eclipse, go to **Preferences -> Java -> Code Style -> Formatter** to import the file. Apparently,
the files can also be used with IntelliJ via the [Eclipse Code Formatter](https://plugins.jetbrains.com/plugin/6546-eclipse-code-formatter) plugin.

But please note that **readability trumps style**. Some projects may have the convention to auto-format
all files and use markers such as `@formatter:off/on` to guard manually-formatted sections. Others may format manually fully manually. Before reformatting whole files, better check the policy. 

If manual formatting isused, format those sections that you are working on and **review your changes before you commit** to  avoid unnecessary changes throughout the code. If you plan to reformat larger parts
of the code, then please do this in separate commits that do not contain any functional changes. Please
do **not use any automatic save actions** that modify code except maybe "remove unused imports".

### Preparing a pull request

In order to contribute to a DKPro project, you need to create a **pull request**. This section
briefly guides you through the best way of doing this:

* Before creating a pull request, create an issue in the issue tracker of the project to which
  you wish to contribute
* Fork the project on GitHub
* Create a branch based on the branch to which you wish to contribute. Normally, you should create
  this branch from the **master** branch of the respective project. In the case you want to fix
  a bug in the latest released version, you should consider to branch off the latest maintenance
  branch (e.g. **1.2.x**). If you are not sure, ask via the issue you have just created. Do **not**
  make changes directly to the master or maintenance branches in your fork. The name of the branch
  should be e.g. `feature/[ISSUE-NUMBER]-[SHORT-ISSUE-DESCRIPTION]` or `bugfix/[ISSUE-NUMBER]-[SHORT-ISSUE-DESCRIPTION]`.
* Now you make changes to your branch. When committing to your branch, use the format shown below
  for your commit messages. Note that `#` normally introduces comments in git. You may have to 
  [reconfigure git](https://stackoverflow.com/questions/22936252/escape-comment-character-in-git-commit-message) 
  before attempting an interactive rebase and switch it to another comment 
  character.
{% highlight text %}
  #[ISSUE NUMBER] - [ISSUE TITLE]
  [EMPTY LINE]
  - [CHANGE 1]
  - [CHANGE 2]
  - [...]
{% endhighlight %}
* You can create the pull request any time after your first commit. I.e. you do not have to wait
  until you are completely finished with your implementation. Creating a pull request early 
  tells other developers that you are actively working on an issue and facilitates asking questions
  about and discussing implementation details.

