# Curriculum Notes: Git

## Alan Croswell's notes on the Software Carpentry curriculum

- git lesson setup page doesn't say to create a github.com
        account; only in the git download instructions. Might be
        better to say it here as well.

- We didn't get to collaboration via github PR's, merges, etc. due
        to poor time management. We need to stick to the syllabus and
        limit the digressions. *Note from Patrick: kind of feel like it's fine to not get to everything. Better they understand what you cover, in my opinion.*

- Windows users get a GUI GitHub login prompt when trying to do a
        git push to a remote, rather than being prompted on the
        terminal

- One student confused the `!` in the GitHub welcome email as part
        of their username, which caused git bash to freak out with a
        broken pipe error when they tried to push to Github. Worth
        noting in case anyone else has this issue.

## Aaron T's notes on SWC git-novice

- Also did not reach collaboration in a 2.5 hr lesson (2021 August, Python).
        But, `git push origin main` was a satisfying stopping point.

- git-novice lesson uses SSH keys for GitHub auth (as of mid-2021).
        It helped to walk through `ssh-keygen` process multiple times from
        `git remote add ...` to `ssh -T git@github.com`, emphasizing every
        step and suggesting that learners restart in the face of
        indecipherable SSH permission errors.
        _Snag:_ renaming `id_ed25519`,`id_ed25519.pub` to something else
            breaks SSH auth.  Next time, I'd say more strongly:
            "non-default SSH key names will break things".
        _Snag:_ during SSH keygen, learner browsers point to
            `github.com/username/planets`, which has a big "Settings" button
            that can lead folks to the wrong page.

- [Episode 5: Exploring History](http://swcarpentry.github.io/git-novice/05-history/index.html)
        in "Simplifying the Common Case",
        old git versions say `use "git checkout -- <file>..." to discard
        changes in working directory`,
        new git versions say `use "git restore <file>..." to discard changes
        in working directory`.
        SWC folks [deferred update](https://github.com/swcarpentry/git-novice/issues/776) because
        `restore` is still an experimental feature.
        So learners' computers may show different messages.
        For discussion, see git-novice issue
        [\#776](https://github.com/swcarpentry/git-novice/issues/776)
        and hyperlink trail therein.
        Next time, I'd skip `git checkout -- <file>` entirely.
