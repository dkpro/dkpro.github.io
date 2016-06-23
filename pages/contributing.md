---
layout: page-fullwidth
title: "About DKPro"
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
   * [Corporate Contributor License Agreement]({{ site.url}}/files/ccla.txt) (CCLA) - required when contributor is employed

*Note: your browser may not correctly detect the UTF-8 encoding in the CLA files. In that case, please switch the encoding in your browser to UTF-8 or right-click on the links, select "Save as", and open the files in a UTF-8–capable editor before printing and signing. You'll know that  the encoding has been properly detected when the umlaut *"ä"* (an 'a' with two dots above) appears in the phrase "*Technische Universität Darmstadt*".

### How to make contributions

Contributions should be submitted by opening an issue on the (GitHub) issue tracker of the project to which you wish to contribute. Describe the bug you fix or the feature that you provide and attach your changes as a diff file.

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

We try to maintain a common code style through our projects (right-click on link and select "Save as"):

* [Eclipse Code Style file]({{ site.url}}/files/DKProCoreStyle_20120326.xml) (2012-03-26)

But please note that **readability trumps style**. Some parts of the code are formatted manually.
Please to not carelessly reformat whole files. Format those sections that you are working on and
**review your changes before you commit** to avoid unnecessary changes throughout the code. If you plan
to reformat larger parts of the code, then please do this in separate commits that do not contain
any functional changes. Please do **not use any automatic save actions** that modify code except
maybe "remove unused imports".
