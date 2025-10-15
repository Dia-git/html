# 42 London Discovery Week: HTML &amp; CSS Showcase

#### Brief Summary
### During my coding week at 42’s Discovery Piscine, I learned the essentials of bash and building web pages with HTML and CSS. Our final assignment (“Rush”) challenged me to set up a simple multi-page site: a responsive index page linking to two separate resume (“CV”) pages. I practiced HTML structure, semantic elements, creating navigation, using Bootstrap for responsive designs, and styling with custom CSS.

<img width="1068" height="686" alt="Resume Page" src="https://github.com/user-attachments/assets/079cd515-4803-463f-baf0-2936fff60132" />

---

## Project Structure

/discovery_piscine/rush

│
├── auteur
├── rush.html            # Index (home) page
├── styles.css           # Shared styles
├── resume1.html         # First resume
└── resume2.html         # Second resume


## Part 1: The Index Page 

See the "rush.html" file.
Purpose: Visitors pick between the two resumes.
Features:
Responsive design with Bootstrap 4.
Big clickable sections with custom hover effect.
Stylish background image.



<img width="850" height="397" alt="Website page 1" src="https://github.com/user-attachments/assets/e6057cef-6143-4ac7-b3f2-0e463c3eb999" />


[Screenshot #1: Homepage]

Sample Code (Partial):

```
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

Part 2: Building the Resume Pages
Each resume page features:
A fixed, custom navigation bar — always visible.
Three main sections:
Personal Info: Name, job title, profile photo, brief intro.
Professional Experience & Skills: As lists.
Contact: Email/LinkedIn links.
Sample: resume1.html
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

Responsive Design & Navigation

- I used Bootstrap's grid to ensure:
- Layout adapts to all screen sizes.
- Navbar collapses into a hamburger menu on mobile.
- Navbar & Section Styles (Inline CSS):

```
css
body { padding-top: 56px; }
.navbar { position: fixed; top: 0; width: 100%; z-index: 1000; }
section { padding: 60px 20px; }
#personal-info p { text-align: justify; }
```

[Screenshot #3: Mobile Menu]

Final Touch: The auteur File
- Ensures authorship:
- text

dinicuta
bakoca

---

## What I Learned

Basics of structuring HTML files and linking CSS/JS dependencies.
Making web layouts responsive with Bootstrap and grids.
Creating and styling navigation bars, sections, and buttons.
Using semantic HTML and accessibility best practices.
How presentation and functionality differ (structure vs. style).
Workflow for organizing files and preparing code for peer evaluation.
