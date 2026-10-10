# Task 6: Host a Static Website with GitHub Pages

**Live website:** https://YOUR-USERNAME.github.io/devops-task-6-github-pages/
**Repository:** https://github.com/YOUR-USERNAME/devops-task-6-github-pages

## Objective
Deploy a simple HTML website using GitHub Pages.

## What I built
A one-page portfolio site made with plain HTML (`index.html`) and CSS (`style.css`). It has sections for skills, projects, certifications and contact. It is responsive, keyboard accessible and has no build step.

## Steps I followed
1. Created `index.html` and `style.css`.
2. Created a new public GitHub repository and pushed the files:
   ```bash
   git init
   git add .
   git commit -m "Add static website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/devops-task-6-github-pages.git
   git push -u origin main
   ```
3. Opened the repo, then **Settings → Pages**.
4. Under **Build and deployment**, set Source to **Deploy from a branch**, then chose branch **main** and folder **/ (root)**, and clicked **Save**.
5. Waited a minute or two, then opened the live link GitHub showed at the top of the Pages settings.
6. Customised the site with CSS (`style.css`) and pushed the change to confirm it redeploys.

## Screenshots
Add screenshots of the Pages settings and the live site here, for example `screenshots/pages-settings.png`.

## Interview questions

**1. What is GitHub Pages?**
A free service that hosts static websites (HTML, CSS, JavaScript) straight from a GitHub repository.

**2. Can you host dynamic apps here?**
Not server-side ones. There is no backend, so no PHP, Node.js servers or databases. You can run client-side JavaScript and call external APIs, or use a separate service for the backend.

**3. What are the limits of GitHub Pages?**
Published sites should stay under 1 GB, with a soft bandwidth limit of about 100 GB per month and a soft limit of 10 builds per hour. It is meant for static content, not for running a business or online store. Check GitHub's current docs, as limits can change.

**4. How do you update the website?**
Commit and push changes to the publishing branch. GitHub rebuilds and redeploys the site automatically.

**5. What happens when you delete the repo?**
The site goes offline and the URL returns a 404 page.

**6. What is the default file that loads?**
`index.html` in the root of the publishing folder.

**7. Can you use a custom domain?**
Yes. Add the domain under Settings → Pages, create the DNS records (a CNAME for subdomains, or A records for an apex domain), and turn on "Enforce HTTPS". HTTPS certificates are free.

## Outcome
I can deploy static content for free using GitHub Pages and update it with a simple `git push`.
