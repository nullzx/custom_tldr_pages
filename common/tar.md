# tar

> Archiving utility.
> Often combined with a compression method, such as gzip or bzip2.
> More information: <https://www.gnu.org/software/tar>.

- 解压, E[x]tract a (compressed) archive [f]ile into the target directory:

`tar xf {{path/to/source.tar[.gz|.bz2|.xz]}} -C {{path/to/dir}}`
`tar xf {{path/to/source.tar[.gz|.bz2|.xz]}} --directory={{path/to/dir}}`

- 解压, E[x]tract a (compressed) archive [f]ile into the current directory [v]erbosely:

`tar xvf {{path/to/source.tar[.gz|.bz2|.xz]}}`

- 压缩, [c]reate a compressed archive [f]ile, [a]uto select compression program by the archive file suffix:

`tar caf {{path/to/target.tar.xz}} {{path/to/file1 path/to/file2 ...}}`
`tar caf {{path/to/target.tar.gz}} --directory={{path/to/dir}} .`
`tar caf {{path/to/target.tar.gz}} {{path/to/file1}} ... -C {{path/to/dir}} ...`

- 合并但不压缩 [c]reate an archive and write it to a [f]ile:

`tar cf {{path/to/target.tar}} {{path/to/file1 path/to/file2 ...}}`

- [c]reate a g[z]ipped archive and write it to a [f]ile:

`tar czf {{path/to/target.tar.gz}} {{path/to/file1 path/to/file2 ...}}`

- E[x]tract files matching a pattern from an archive [f]ile:

`tar xf {{path/to/source.tar}} --wildcards "{{*.html}}"`

- Lis[t] the contents of a tar [f]ile [v]erbosely:

`tar tvf {{path/to/source.tar}}`
