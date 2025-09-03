# 🪜 Steps to Add a New Specialization: *Communication Engineering*

### **1. Create the Specialization Page**

Create a new file at the root of your repo (same level as `datascience.md`) and name it `communication-engineering.md`.

```yaml
---
layout: page
title: Communication Engineering
permalink: /teaching/communication-engineering/
parent: Teaching
nav: true
---
# Communication Engineering

Here are the courses under **Communication Engineering**:

<ul>
  {% for course in site.teaching %}
    {% if course.category == "Communication Engineering" %}
    <li>
      <a href="{{ course.url }}">{{ course.title }}</a>
      ({{ course.course_number }}) – {{ course.term }}
    </li>
    {% endif %}
  {% endfor %}
</ul>
```

---

### **2. Add New Courses Under This Specialization**

Inside `_teaching/`, create a course file, e.g., `digital-comm.md`:

```yaml
---
layout: page
title: Digital Communications
permalink: /teaching/communication-engineering/digital-comm/
parent: Communication Engineering
course_number: CE201
term: Spring 2026
category: Communication Engineering
---
# Digital Communications

Course page content goes here.
```

---

### **3. No Changes Needed in `breadcrumbs.yml`**

Since you already have this in `_config.yml`:

```yaml
breadcrumb_parents:
  teaching: "Teaching"
  projects: "Projects"
```

👉 Any page under the `_teaching/` collection (like your new course) will automatically inherit **Teaching** as the top-level parent.
Because you’re also declaring `parent: Communication Engineering` in the course, the full chain will work.

---

### **4. Check Breadcrumbs Output**

Visiting `/teaching/communication-engineering/digital-comm/` will show:

```
Home › Teaching › Communication Engineering › Digital Communications
```

---

✅ That’s it — only two steps: create the specialization page + create course pages under it.

---


