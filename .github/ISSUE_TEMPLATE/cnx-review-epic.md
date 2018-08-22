---
name: CNX Release Review Epic
about: Create an issue as an Epic in Zenhub in order to track all issues for a given CNX release.

---

## Milestone dates:
- Code freeze (no new features):  **DATE**
- Code deployed to staging server: DATE
- Testing on staging server: DATE => DATE
- RC Review meeting: DATE
- Code Released to Production: **DATE**


## Link to release report
in Zenhub

## Repos updated:
- oer.exports
- webview
- cnx-recipes
- Products.RhaptosPrint
- etc.

## Demo:
- 1
- 2

## No Demo:
- 1
- 2

## Repo Checklist (Books+CNX)
<details>
<summary>Click here to see full checklist</summary>
	
- [ ] **oer.exports** (*Helene*)
	- [ ] https://github.com/Connexions/oer.exports/blob/master/version.txt should match current release
	- [ ] Release created in https://github.com/Connexions/oer.exports/releases
	- [ ] New RhaptosPrint egg should be built by DevOps (they need the version number)
- [ ] **cnx-recipes** (*Helene*)
	- [ ] Release created in https://github.com/Connexions/cnx-recipes/releases
	- [ ] cnx-deploy: `environments/__prod_envs/files/publishing-requirements.txt` should be updated -- a bot will automatically create this PR, which will need to be reviewed and merged.
- [ ] **webview** (*Helene*)
 	- [ ] Release created in https://github.com/Connexions/webview/releases
	- [ ] Tarball for version needs to be available at https://packages.cnx.org/js-builds/ (I think Jenkins builds this automatically?)
	- [ ] cnx-deploy: needs a manual PR opened, reviewed, and merged to update `environments/__prod_envs/vars/versions.yml`
- [ ] **cnx-archive** (*Ross or Mulich*)
 	- [ ] Release tag created in GitHub
 	- [ ] PyPi version revved
	- [ ] cnx-deploy: `environments/__prod_envs/files/publishing-requirements.txt` should be updated -- a bot will automatically create this PR, which will need to be reviewed and merged.
- [ ] more CNX repos here etc. -- full list here: https://github.com/Connexions/cnx/issues/8
</details>

## Links to DevOps cards:
- staging
- prod
