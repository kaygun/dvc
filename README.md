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

1. It tracks individual files.
2. You can safely checkout different versions.
3. It can show the diff between a version and its parent.
4. It can show version tree both as a log and as a graph.

If you need more functionality than the ones I described above,
you probably need a more sophisticated version control system.

## Is it going to do X?

No.

## Are you going to port it to $LANG?

No.

## Dependencies

`dvc` heavily depends on [MD5][5] hash sum signatures. I am using [`md5sum`][6] which
comes with coreutils.  But if you'd like to use another hash function, you should
edit the source and make the change.

`dvc` uses [graph-easy][4] to display the dependency tree.  If you'd like
to use that feature, you should install it.

## Bugs?

Many. This is a personal project, and by no means is *production quality*,
whatever that may mean.  By design `dvc` doesn't delete any file it tracks,
but you may lose files, data, code etc. due to unforseen circumstances.

[1]: https://git-scm.com/
[2]: https://www.mercurial-scm.org/
[3]: https://subversion.apache.org/
[4]: http://bloodgate.com/perl/graph/manual/
[5]: https://en.wikipedia.org/wiki/MD5 
[6]: https://en.wikipedia.org/wiki/Md5sum
