# Yadt | New Dependency Resolving

<img src="res/standalone.svg" style="width: 2048px; margin-left: 40%; margin-top: 15%; opacity: 0.5;" />

.fx: titleslide imageslide

---

# Old Strategy

<img src="res/old0.dot.svg" style="height: 400px; opacity: 1; margin-top: 10%;" />

.fx: imageslide

---

# Old Strategy

<img src="res/old1.dot.svg" style="height: 400px; opacity: 1; margin-top: 10%;" />

.fx: imageslide

---

# Old Strategy

<img src="res/old2.dot.svg" style="height: 400px; opacity: 1; margin-top: 10%;" />

.fx: imageslide

---

# Old Strategy

<img src="res/old3.dot.svg" style="height: 400px; opacity: 1; margin-top: 10%;" />

.fx: imageslide

---

<img src="res/waterfall.jpg" style="height: 800px;"/>

.fx: imageslide

---

# New Strategy

<img src="res/new0.dot.svg" style="height: 400px; opacity: 1; margin-top: 10%;" />

.fx: imageslide

---

# New Strategy

<img src="res/new1.dot.svg" style="height: 400px; opacity: 1; margin-top: 10%;" />

.fx: imageslide

---

# New Strategy

<img src="res/new2.dot.svg" style="height: 400px; opacity: 1; margin-top: 10%;" />

.fx: imageslide

---

<center>** Old vs. New **</center>

<img src="res/new2.dot.svg" style="height: 300px; margin-top: 10%; margin-left: 20%;" />
<img src="res/old3.dot.svg" style="height: 300px; margin-top: 10%; margin-left: -25%;" />

.fx: imageslide

---

# Troublemaker: jcr

<img src="res/troublemaker.dot.svg" style="height: 400px; opacity: 1; margin-top: 12%;" />

.fx: imageslide

---

# Solution

/etc/yadt.services

    !python
    ...
    tomcat:
        needs_artefacts: [is24-jcr]
    ...

---

# Solution

<img src="res/troublemaker1.dot.svg" style="height: 400px; opacity: 1; margin-top: 12%;" />

.fx: imageslide

---

# Question

<p style="text-align: right;">
What do we test in Tuv?
</p>

---

# Perspective

<div class="whitebody">
modularization of the yadt config
<p/>

(an invitation to next yadt talk :o)
</div>

<img src="res/beyond_horizon.jpg" style="height: 576px;" />

.fx: imageslide whiteheading

---

# Thanks!

<p style="margin-top: 50%;">
2013-08-01 | IT-Pro-SD | Immobilienscout 24
</p>

<img src="res/standalone.svg" style="width: 2048px; margin-left: 40%; margin-top: 15%; opacity: 0.5;" />

.fx: titleslide imageslide
