
# 42 London Discovery Week: HTML & CSS Showcase 👩🏻 💻

[![Made with HTML](https://img.shields.io/badge/Made%20with-HTML-orange?logo=html5)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Made with CSS](https://img.shields.io/badge/Made%20with-CSS-blue?logo=css3)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Built at 42 London](https://img.shields.io/badge/Built%20at-42%20London-black?logo=42)](https://42london.com)

---

## 📚 Table of Contents

- [About 42 London](#-about-42-london)
- [Project Overview](#-project-overview)
- [Project Structure](#️-project-structure)
- [Part 1: The Index Page](#-part-1-the-index-page)
- [Part 2: The Resume Pages](#-part-2-the-resume-pages)
- [Skills Demonstrated](#️-skills-demonstrated)
- [Authorship](#-authorship)
- [Learning Reflection](#-learning-reflection)

---

## 🏫 About 42 London

Brief Summary
[42 London](https://42london.com) is a *tuition-free coding school* redefining tech education through **peer-to-peer, project-based learning**.  
The school operates **24/7** and focuses on collaboration, problem-solving, and creativity, with *no teachers or classes*.  

I participated in **42 London’s Discovery Week**, a short, hands-on introduction to their learning environment. Discovery Week offers a preview of the 42 learning model before applying to the full **Piscine** (month-long selection process). During my coding week, I learned the essentials of bash and building web pages with HTML and CSS. Our final assignment (“Rush”) challenged me to set up a simple multi-page site: a responsive index page linking to two separate resume pages. 

---

## 💡 Project Overview

During Discovery Week, as a last task, I built the **HTML & CSS Rush Project**, a mini showcase website to practice essential web development fundamentals. I practiced HTML structure, semantic elements, creating navigation, using Bootstrap for responsive designs, and styling with custom CSS.

**Goal:** Create a simple, multi-page site using *HTML*, *CSS*, and *Bootstrap 4*.  
The homepage allows users to choose between **two resume (CV)** pages.

### Key Learning Areas
- Semantic HTML structure  
- CSS styling, hover effects, and responsive design  
- Bootstrap navigation and grid system  
- Accessibility and good web structure practices  

---

## 🗂️ Project Structure

```text
/discovery_piscine/rush
│
├── auteur # Author logins (dinicuta, bakoca)
├── rush.html # Index (homepage)
├── styles.css # Shared style definitions
├── resume1.html # Resume page for Diana
└── resume2.html # Resume page for Baris
```

[Jump to Part 2: Resume Pages](#-part-2-the-resume-pages)

---

## 🏠 Part 1: The Index Page

**File:** `rush.html`  
**Purpose:** Guide users to select one of the two resumes.

**Features:**
- Responsive layout with **Bootstrap Grid**  
- Interactive resume selection with hover transitions  
- Full-screen background image for design appeal  

**Preview:**

<img width="850" height="397" alt="Website page 1" src="https://github.com/user-attachments/assets/e6057cef-6143-4ac7-b3f2-0e463c3eb999" />

[Screenshot #1: Homepage]



Sample Code (Partial):

```html
xml
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Resume Selection</title>
  <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="bg-light text-center py-4">
    <h1>Pick One:</h1>
  </header>
  <div class="container-fluid h-100 d-flex justify-content-center align-items-center">
    <div class="row text-center">
      <div class="col-md-6">
        <div class="resume-box" onclick="location.href='resume2.html';">
          <h2>🦁 Resume 1: Baris</h2>
        </div>
      </div>
      <div class="col-md-6">
        <div class="resume-box" onclick="location.href='resume1.html';">
          <h2>🐈 Resume 2: Diana</h2>
        </div>
      </div>
    </div>
  </div>
  <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
```

Custom Style (styles.css snippet):

```
css
body {
  font-family: Arial, sans-serif;
  background-image: url('https://images.pexels.com/photos/460672/pexels-photo-460672.jpeg?auto=compress&cs=tinysrgb&w=600');
  background-size: cover;
  height: 100vh; margin: 0;
}

.resume-box {
  background-color: rgba(255, 255, 255, 0.8);
  border-radius: 10px;
  padding: 40px;
  cursor: pointer;
  transition: transform 0.3s, box-shadow 0.3s;
}

.resume-box:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
}
```

---

## 🧾 Part 2: The Resume Pages

Each `resume.html` file presents a personalized professional profile.

**Sections Included:**
1. **Personal Info:** name, title, photo, introduction  
2. **Professional Experience & Skills:** work experience and strengths  
3. **Contact:** email and LinkedIn links  

**Responsive Design Features:**
- Fixed navigation bar (always visible) 
- Collapsible *Bootstrap* hamburger menu for mobile  
- Section-based layout (adapts to all screen sizes) with padding and easy readability

  

**Preview:**

<img width="1068" height="686" alt="Resume Page" src="https://github.com/user-attachments/assets/079cd515-4803-463f-baf0-2936fff60132" />

[Screenshot #2: Profile 2]

Sample: resume1.html

```html
xml
<nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
  <a class="navbar-brand" href="#">My Resume</a>
  <button class="navbar-toggler" ...>
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item"><a class="nav-link" href="#personal-info">Personal Info</a></li>
      <li class="nav-item"><a class="nav-link" href="#professional-experience">Professional Experience</a></li>
      <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<section id="personal-info">
  <h2>Name: Diana</h2>
  <h3>Job Title: Computational Wizard at NOYB</h3>
  <img src="https://loop.frontiersin.org/images/profile/851522/203" ...>
  <p>Brief introduction: ...</p>
</section>
<!-- Professional Experience and Contact sections follow -->
```

 Navbar & Section Styles (Inline CSS):

```css
body { padding-top: 56px; }
.navbar { position: fixed; top: 0; width: 100%; z-index: 1000; }
section { padding: 60px 20px; }
#personal-info p { text-align: justify; }
```

[Screenshot #3: Mobile Menu](https://github.com/Dia-git/html/blob/main/Resume%20Website%20-%20Diana%20Nicutari.pdf)

---

## 🛠️ Skills Demonstrated

- Organizing and linking multiple HTML files  
- Applying responsive design best practices  
- Using **Bootstrap 4** components  
- Writing structured, semantic HTML  
- Using **CSS transitions** and hover effects for interactivity  

---

## 👩‍💻 Authorship

The `auteur` file includes the project authors:

```text
dinicuta
bakoca
```


---

## 🧠 Learning Reflection

This project, completed during **42 London Discovery Week**, provided practical exposure to designing and structuring a front-end site collaboratively. It reinforced the importance of coordination, version control, and clear presentation across multiple pages.

Skills developed:
- Basics of structuring HTML files and linking CSS/JS dependencies.
- Making web layouts responsive with Bootstrap and grids.
- Creating and styling navigation bars, sections, and buttons.
- Using semantic HTML and accessibility best practices.
- How presentation and functionality differ (structure vs. style).
- Workflow for organizing files and preparing code for peer evaluation.

---

> Built as part of **Discovery Week at 42 London** — not the full curriculum.


---
---

<!---


--->
