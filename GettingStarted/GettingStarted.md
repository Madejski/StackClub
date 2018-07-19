# Getting Started on the LSST Science Platform

_Greg Madejski and [Phil Marshall](https://github.com/LSSTScienceCollaborations/DMStackClub/issues/new?body=@drphilmarshall)_

We are developing tutorial notebooks on remote JupyterLab instances, to short-circuit the DM stack installation process and get used to working in the 
notebook aspect of the LSST science platform. In these notes we provide:
* Notes on how to get set up on the LSST Science Platform (LSP) JupyterLab Notebook Aspect at NCSA
* Help with getting set up to the DM Stack Club tutorial notebooks

> NB. In Phase 0, we made use of the [jupyterlabdemo.lsst.codes](https://jupyterlabdemo.lsst.codes/user/madejski/lab?redirects=1)
instance, set up by the DM team in the Google cloud. For Phase 1, we will be using the LSP JupyterLab instance at the LSST Data Facility, NCSA.

**The go-to resource is the [LSST Science Platform (LSP) Notebook Aspect Documentation](https://nb.lsst.io/)** - below we give a very brief summary, and some DM Stack Club-specific tips.

## Accessing the LSST Science Platform
The [LSP docs](https://nb.lsst.io/) provides an introduction to the NCSA system, including how to gain access and then how to use JupyterLab once you are in. 
Getting in to NCSA takes involves getting an NCSA account, and then figuring out VPN access.

### Getting an NCSA Account
Contact Phil (DM @drphilmarshall on LSSTC Slack) or Simon (@ksk) to get an NCSA Stack Club account. You'll need to provide your full name (first and last) and your email address. You'll (eventually) get an email invitation to [create an account at NCSA](https://identity.ncsa.illinois.edu/) (including choosing a username of 8 characters or fewer). After you have submitted your form, it typically takes 24 hours for your account to be set up: set an alarm to come back the next day!

### Accessing NCSA via its VPN
As explained on the [PDAC wiki](https://confluence.lsstcorp.org/display/DM/PDAC+networking+and+user+accounts+for+developers), the only way to get onto the LSST science platform at NCSA is via its virtual private network (VPN). The easiest way is by using Cisco's AnyConnect, which if you don't have you can get by pointing your browser at **https://vpn.ncsa.illinois.edu/** and selecting the `ncsa-vpn-default` option (this will only work if you have a java-compatible browser, like firefox esr version<=52). If you already have the AnyConnect client installed, open it up and enter `vpn.ncsa.illinois.edu` in its connection window. 

If you forget your password it can be reset following the instructions [here](https://developer.lsst.io/services/lsst-dev.html?highlight=reset#lsst-dev-password). If you have problems connecting to the NCSA services you can check their status and submit a help ticket [here](https://confluence.lsstcorp.org/display/DM/LSST+Service+Status+page).

### Starting up the LSST Science Platform JupyterLab Notebook Aspect 
Once the VPN connection is established, you should be able to navigate to the the JupyterLab instance at **https://lsst-lspdev.ncsa.illinois.edu/nb**. Select `Release 15.0` and `medium` on the Spawner Options landing page, and then hit the "Spawn" button. You'll (eventually) end up on the JupyterLab launcher, where you can use the file manager in the left hand side bar to open your Jupyter notebooks, or start terminal or notebook editor tabs from the buttons provided.  You should see the pre-installed `notebook-demo`  notebooks in the file manager, for example.

> It might take a long time to start the JupyterLab instance (a few minutes or so).  We recommend using "Release 15.0" to try to keep the notebooks from going stale (adopting a common Stack version makes testing easier), and using "medium" size (to enable the image processing notebooks).  

> At the end of your JupyterLab session, please make sure you save all and log out (from the launcher menu), to free up the cluster for others. 


## Contributing to the DM Stack Club Repo
From the Launcher, start a terminal, `cd` to the `notebooks` folder and `git clone` the `DMStackClub` repo, using https access:
```
git clone https://github.com/LSSTScienceCollaborations/DMStackClub.git
```
You can then `git checkout` a development branch and modify the club notebooks, opening them from the file manager and using the resulting notebook editor. New to `git` and GitHub? Have a play in [this sandbox](https://github.com/drphilmarshall/GettingStarted) - from there you can watch Phil on YouTube doing a GitHub live demo, too.

### Workflow
The Stack Club workflow is to edit the club notebooks (or start new ones) in a suitable development branch, push it to the base repo, and submit a pull request (to enable club code review). Club members have Write access and so can do this; everyone else can push to their fork of the DMStackClub repo, and submit a PR from there. To exercise this workflow, try modifying  [`Hello_World.ipynb`](https://github.com/LSSTScienceCollaborations/DMStackClub/blob/master/notebooks/Hello_World.ipynb), pushing your commit(s) and submitting a PR. Don't forget to clear outputs and save before committing your changes!  (note from Greg Madejski:  this link might not work any more)

### Test Data
Broadly useful datasets should be available in `/project/shared/data`  - this is a group-writeable folder, so feel free to contribute public data there. You can also use your personal `/project/<username>` folder for datasets that you want to share, but may not be as generally applicable. As a rule, Stack Club notebooks should use data in `/project/shared/data`.



