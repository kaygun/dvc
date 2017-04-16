# Dumb Version Control

## Why?

In my line of work, for tracking different versions of a single
file [git][1], [mercurial][2] or [svn][3] are much too heavy.
Then there is the issue of remember all the bells and whistles
of each of these version control systems.  After losing a day's
worth of work for using a wrong switch on git, I decided to write
a very dumb version control system aptly called `dvc`.

## Design philosophy

By design `dvc` doesn't do much: It tracks individual files 
and does not do much else.

1. tracks individual files
2. can show the diff between a version and its parent
3. can show dependency tree both as a log and as a graph

If you need more functionality than the ones I described above,
you probably need a more sophisticated version control system.

## Does it do X? 

No.

## Is it going to do X?

No.

## Are you going to port it to $LANG?

No.

## Bugs?

Many. This is a personal project, and by no means is *production quality*,
whatever that may mean.  By design `dvc` doesn't delete any file it tracks,
but you may lose files, data, code etc.
