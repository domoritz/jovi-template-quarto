---
name: Initial Editor Checklist
about: Checklist for editors to fill out prior to review
title: Initial Editor Checklist
labels: pre-review
assignees: ''

---

- [ ] Check that the HTML version is in the repo as index.html and renders to the JoVI format (refer to https://github.com/journalovi/jovi-template-quarto)
- [ ] Article uses a format something similar to the template
- [ ] Includes author information
- [ ] Includes abstract
- [ ] Includes the required paper sections
   - [ ] Table of contents
   - [ ] Research materials
   - [ ] Authorship
   - [ ] License
   - [ ] Conflicts of Interest
- [ ] Add a notice infobox at the top that the paper is under review w/ link to github issues above the abstract. In Quarto this looks like:
   ```
   ::: {.callout-important appearance="simple"}
   ## Under Review {.unnumbered}
   This paper is under review on the experimental track of the [Journal of Visualization and Interaction](https://www.journalovi.org/).
   :::
   ```
- [ ] Set up github pages
   - [ ] Settings -> Actions -> General -> Allow journalovi, and select non-journalovi, actions. Enter: 
      `actions/*,quarto-dev/*`
      ![image](https://github.com/journalovi/2023-park-gatherplots/assets/6345019/05018b2f-f00e-4019-92de-cced0aab0d72)
   - [ ] If using Quarto:
      - [ ] clone the repo locally
      - [ ] run this command in the repo directory:
         ```
         quarto publish gh-pages index.qmd
         ```
- [ ] From the main repo page, click the settings gear icon next to "About" on the right. 
   - [ ] Under "Description" enter "UNDER REVIEW"
   - [ ] Under "Website" tick "Use Your Github Pages Website".
- [ ] Verify the publishing workflow works. On the repo page, go to Actions and click on the "XXX Publish" (XXX = Quarto/Idyll/etc) workflow on the left, then click Run Workflow and run it.
   - [ ] When this completes, check that the "pages build and deployment" action is successful.
   - [ ] Check that the article is visible at the github.io address.
- [ ] Edit README.md and add the following at the very top:
   ````
   ```diff
   ! This paper is under review on the experimental track of the Journal of Visualization and Interaction.
   ```
   ````
- [ ] Ensure all appropriate supplemental materials are included: e.g. experimental data, experimental analysis code, source code for artifacts, etc. For a full list of requirements see the [transparency section of the author guide](https://www.journalovi.org/author-guide.html#transparency-requirements)
  - [ ] Check they are in appropriate long-term repositories (e.g. OSF, Zenodo, etc). Github repositories are okay as long as they are also archived on something like OSF or Zenodo. One easy way to archive + DOI an existing github repo is with Zenodo; see [here](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content)
  - [ ] Check they are listed in the abstract and the required Materials section of the paper
- [ ] If anything in the above list is missing (required paper sections, supplemental materials, etc), create an issue tagging the authors and ask them to add those materials (do this after sending them the intial review email).
