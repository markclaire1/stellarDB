# stellarDB
A collection of stellar spectra for use in photochemical and climate models

Files contain one header line with columns for wavelength(nm) and flux(mW/m^2/nm)

Documentation needed on best practices for updating this and other submodules like atmDB:
if updating any data within a submodule, it is best practice to create a branch, otherwise fetch/pull commands can overwrite:
Best practice:
cd into the submodule directory, and mentally realize that you are in an entirely distinct git project
git checkout <branchname>
follow normal best practices (make your changes, test, add, commit)

If in anyway complicated, it is nice to allow the maintainer a chance to review your additions. In this case:
push branch to remote repo
initiate pull request (via github.com)
deal with any requests, and wait for maintainer to merge into main branch
git pull
delete your local branch

If simple changes:
merge into the main branch and push.

Either way:
you also need to go up the heirarchy into the main project and do a git add/commit/push on the submodule directory
this will force users of the main project to update the submodule to have access to the new code
