# Yadt | Modular Config

<img src="res/standalone.svg" style="width: 2048px; margin-left: 40%; margin-top: 15%; opacity: 0.5;" />

<p style="margin-top: 550px; text-align: left; margin-left: 80px;">
http://www.yadt-project.org/
<br/>
<br/>
2013-08-08&nbsp;&nbsp;|&nbsp;&nbsp;IT-Pro-SD&nbsp;&nbsp;|&nbsp;&nbsp;ImmobilienScout24
</p>

.fx: titleslide imageslide

---

# Present: Artefacts and Config

<img src="res/7207121_f520.jpg"/>

.fx: imageslide whiteheading

---

# Future: Modular Config

<img src="res/lego.jpg"/>

.fx: imageslide

---

## Artefacts with Config Snippets,

httpd.rpm: /etc/yadt.conf.d/20_httpd.yaml

    !python
    service:
        httpd:


<p style="margin-left: 10%;">+</p>

tomcat.rpm: /etc/yadt.conf.d/30_tomcat.yaml

    !python
    service:
        tomcat:

---

## Merged in Filesystem,

    !python
    /etc/yadt.conf.d/
        00_defaults.yaml
        01_host_settings.yaml
        20_httpd.yaml
        30_tomcat.yaml

---

## ... Resulting in a MVYC

    !python
    services:
      - httpd:
      - tomcat:

<p style="margin-top: 300px;">
<em>MVYC: Minimal Viable Yadt Configuration</em>
</p>

---

## How the Merge Happens:

* Arrays: extended
* Hashes: merged (yes, recursion)
* Scalars: overwritten (order matters!)

---

## Config Augmentation ...

httpd-with-tomcat.rpm: /etc/yadt.conf.d/40_httpd_with_tomcat.yaml

    !python
    service:
        httpd:
            needs_services: [tomcat]

---

## ... Gets Merged, too!

    !python
    /etc/yadt.conf.d/
        ...
        40_httpd_with_tomcat.yaml

<p class="arrow-down">&nbsp;</p>

    !python
    services:
        httpd:
            needs_services: [tomcat]
        tomcat:

---

## Bonus: Even More Features

    !python
    settings: {
        'ARTEFACTS_INDUCING_REBOOT': ['kernel']
    }

---

# Making the jump!

<img src="res/jump.jpg" />

.fx: imageslide whitetext

---

# But How?

<span style="font-size: 24pt; visibility: hidden;">&#x2190; we are here</span>

## 1. standard rpms with standard config
## 2. custom config snippets <span style="font-size: 24pt; font-style: italic;"> only when needed</span>
## 3. your hosts without /etc/yadt.services

---

# But How?

<span style="font-size: 24pt; visibility: normal; color: red;">0. &#x2190; we are here</span>

## 1. standard rpms with standard config
## 2. custom config snippets <span style="font-size: 24pt; font-style: italic;"> only when needed</span>
## 3. your hosts without /etc/yadt.services

---

# Thanks!

<p style="margin-top: 550px; text-align: left; margin-left: 80px;">
http://www.yadt-project.org/
<br/>
<br/>
2013-08-08&nbsp;&nbsp;|&nbsp;&nbsp;IT-Pro-SD&nbsp;&nbsp;|&nbsp;&nbsp;ImmobilienScout24
</p>

<img src="res/standalone.svg" style="width: 2048px; margin-left: 40%; margin-top: 15%; opacity: 0.5;" />

.fx: titleslide imageslide

