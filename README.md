# HackathonNames

[Link to class slides](https://docs.google.com/presentation/d/1bwkCllKEPb2s6guoQyJHmYSU1V4PcOuDVtaIfhk0xpA/edit#slide=id.gf840b18e06_0_520)

# Finishing the GDI Git & GitHub for Hackathons Lab

I have now fixed the default branch and there are a few steps you need to take to finish the lab!

## Find which branch your commit is on

Your commit is most likely either on the `master` branch or the `feat/add-otter` branch. 

To find out which branch you're on:

    git branch -v

All the local branches on your machine will be listed, and the one with the `*` is the branch you're on. 

On your branch, look for your commit with:

    git log

> *Quick Tip:* Use space to scroll down and `:q` or `Cmd` `+` `C` to exit the editor. You can also type `/` followed by your name (for example, I would type `/brenda`) to search for your commit. 

If you don't see your commit on this branch, switch to the other branch and search for it. To switch branches use:

    git checkout <branchname>

For example, to switch to master:

    git checkout master

To switch to `feat/add-otter`:

    git checkout feat/add-otter

If you don't find your commit at all, make a new one. 

## If your commit is on branch `feat/add-otter`

    git pull origin master
  
    git push -u origin/master
  
## If your commit is on branch `master`

    git pull

    git push

# Getting Unstuck

## Git or Command not found

Make sure you are in the correct directory! Try `pwd` and look around. 

## I don't have permission to push

### Check permissions

Make sure you have access to this repository

### Check your remote URL is SSH, not HTTPS

To see your remote URL:
    git remote -v

This will tell you if you're pointing to a `git@...` URL (SSH) or `https://...` URL (HTTPS). If you are on https, switch the remote to our SSH URL:

    git remote set-url origin git@github.com:brendajin/HackathonAnimals.git
    
### If you are not yet configured to use SSH with GitHub

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

