# hello-world-20180701
Hello world tutorial run through, again

I created a new branch in the GitHub UI, and then experimented with how I'd get that branch into my local repo. I tried entering 'git pull' from my local clone of the repository, and got the following message:

```
From github.com:murrayjason/hello-world-20180701
 * [new branch]      readme-edits -> origin/readme-edits
Already up-to-date.
```

This seems to indicate that my local repo indeed acquired something to connect it to the new branch.

But then when I looked at the local branches, Git returned this

```
> git branch
* master
```

It did not show the new branch. Is this a bug, or just confusing?

Then I looked at the remote objects in the repo, and saw the new branch was indeed represented:

```
> ls remotes/origin/
HEAD        readme-edits
```

So I then tried switching to the new branch:

```
> git checkout readme-edits
Branch readme-edits set up to track remote branch readme-edits from origin.
Switched to a new branch 'readme-edits'
```

That looks as though switching for the first time to the new branch, in my local clone of the repo, enabled the local branch to track its namesake on GitHub. When I then queried the local branches, Git showed the new branch:

```
> git branch
* master
  readme-edits
```


