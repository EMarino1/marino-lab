========================================
HOW TO UPDATE THE MARINO LAB WEBSITE
========================================

OVERVIEW
--------
The workflow is always:

Edit files → Build site → Push to GitHub → Website updates


----------------------------------------
STEP-BY-STEP INSTRUCTIONS
----------------------------------------

1. OPEN YOUR PROJECT FOLDER

Open PowerShell and go to your project:

cd "C:\Users\emanu\OneDrive\Desktop\my-research-site"


----------------------------------------

2. EDIT YOUR CONTENT

Modify the relevant file:

- Homepage → index.qmd
- Research → research.qmd
- People → people.qmd
- Join page → join.qmd
- Publications → publications.qmd
- Styling → styles.css
- Images → replace files in /images/


----------------------------------------

3. BUILD THE WEBSITE

Run:

quarto render

This updates the "docs/" folder (the live website files).


----------------------------------------

4. PREVIEW LOCALLY (OPTIONAL)

Run:

quarto preview

This opens the website locally in your browser so you can check changes.


----------------------------------------

5. ADD FILES TO GIT

Run:

git add .


----------------------------------------

6. COMMIT CHANGES

Write a short description:

git commit -m "Update homepage text"

Examples:
- "Add new publication"
- "Update research figures"
- "Fix layout"


----------------------------------------

7. PUSH TO GITHUB

Run:

git push


----------------------------------------

8. WAIT FOR UPDATE

Wait ~1–2 minutes.

Your website updates automatically at:

https://emarino1.github.io/marino-lab/


----------------------------------------
HOW TO CHECK IT WORKED
----------------------------------------

1. Refresh your website
2. If needed, hard refresh:
   Ctrl + Shift + R


----------------------------------------
COMMON ISSUES
----------------------------------------

1. Changes not visible:
   → You forgot: quarto render

2. Images not updating:
   → Replace image
   → Run quarto render
   → Then git push

3. Git says "nothing to commit":
   → You didn’t save your file

4. Page broken:
   → Check file names and _quarto.yml


----------------------------------------
GOLDEN RULE
----------------------------------------

Always run:

quarto render

BEFORE pushing changes.


----------------------------------------
ULTRA-SHORT VERSION
----------------------------------------

quarto render
git add .
git commit -m "update"
git push


----------------------------------------
EXAMPLE (ADDING A NEW PAPER)
----------------------------------------

1. Edit publications.qmd
2. Run:

quarto render
git add .
git commit -m "Add new publication"
git push


----------------------------------------
END
----------------------------------------