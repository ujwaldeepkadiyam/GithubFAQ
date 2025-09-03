# 📂 Skeleton for Adding a New Specialization with breadcrumbs

👉 Create a file in the repo root (same level as `datascience.md`) named after your specialization, e.g. `specialization-name.md`

```yaml
---
layout: page
title: Specialization Name
permalink: /teaching/specialization-name/
parent: Teaching
nav: true
---
# Specialization Name

Here are the courses under **Specialization Name**:

<ul>
  {% for course in site.teaching %}
    {% if course.category == "Specialization Name" %}
    <li>
      <a href="{{ course.url }}">{{ course.title }}</a>
      ({{ course.course_number }}) – {{ course.term }}
    </li>
    {% endif %}
  {% endfor %}
</ul>
```

---

# 📂 Skeleton for Adding a New Course

👉 Inside `_teaching/`, create a file named after your course, e.g. `course-name.md`

```yaml
---
layout: page
title: Course Name
permalink: /teaching/specialization-name/course-name/
parent: Specialization Name
course_number: CE101   # Replace with your course code
term: Fall 2025        # Replace with semester/term
category: Specialization Name
---
# Course Name

Welcome to **Course Name**!  

(Add course details, syllabus, lecture notes, resources, etc.)
```

---

# 🪜 Steps Summary

1. **Create specialization page** (using skeleton 1)

   * Put it in repo root.
   * `parent: Teaching`.
   * Match `permalink` with the specialization name.

2. **Create course page(s)** inside `_teaching/` (using skeleton 2)

   * `parent: Specialization Name` (must match specialization page `title`).
   * `category: Specialization Name` (so it shows up in the list).
   * Make sure `permalink` follows `/teaching/specialization-name/course-name/`.

3. **Done!** Breadcrumbs will automatically show as:

   ```
   Home › Teaching › Specialization Name › Course Name
   ```

---

⚡ So if tomorrow you add *Communication Engineering*, just do:

* `communication-engineering.md` (specialization page)
* `_teaching/digital-comm.md`, `_teaching/signal-processing.md` (course pages)

and you’re set 🎉

---

Do you also want me to make a **boilerplate copy-paste block** (just replace the names inline) so you don’t even have to think about formatting?
