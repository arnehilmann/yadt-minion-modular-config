# Yadt | Modular Config

<img src="res/standalone.svg" style="width: 2048px; margin-left: 40%; margin-top: 15%; opacity: 0.5;" />

.fx: titleslide imageslide

---

<img src="res/7207121_f520.jpg"/>

Artefacts and their Configuration

.fx: fullimage whitetext

---

# Artefacts with Config Snippets,

*from httpd artefact:*

    !python
    service:
        httpd:

*from tomcat artefact:*

    !python
    service:
        tomcat:

---

# Merged in Filesystem,

    !python
    /etc/yadt.conf.d/
        00_defaults
        01_host_settings
        20_httpd
        30_tomcat

---

# ... Resulting in a Minimal Yadt Config

    !python
    services:
      - httpd:
      - tomcat:

---

# Additional Dependencies ...

*from httpd-with-tomcat artefact:*

    !python
    service:
        tomcat:
            needs_services: [httpd]

---

# ... Gets Merged, too!

    !python
    services:
        httpd:
        tomcat:
            needs_services: [httpd]

---

# Perspective

<img src="res/beyond_horizon.jpg" />

.fx: imageslide whiteheading

---

# Thanks!

<p style="margin-top: 50%;">
2013-08-08 | IT-Pro-SD | Immobilienscout 24
</p>

<img src="res/standalone.svg" style="width: 2048px; margin-left: 40%; margin-top: 15%; opacity: 0.5;" />

.fx: titleslide imageslide
