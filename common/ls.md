# ls

> List directory contents.
> More information: <https://www.gnu.org/software/coreutils/ls>.
> 下面使用的llh是函数, 它的定义如下
> llh () {
>    ls -AlhF | awk '$9 ~ /^\./'
>    return 0
> }
> 下面使用的lla是函数, 它的定义如下
> lla () {
>    llh
>    ls -lhF | tail -n +2
>    return 0
> }

- 每行只显示一个条目 alias='ls -1'
`l`

- 按名称排序，长格式，文件大小以字节形式展现 alias=ll='ls -l'
`ll`

- 按大小排序，长格式，以合适的方式显示文件大小 alias lls='ls -lhS'
`lls`

- 按文件类型排序, 以合适的方式显示文件大小 alias lle='ls -lhX'
`lle`

- 按最近修改时间排序, 以方便人类读的方式显示大小 alias llmt='ls -lhtr'
`llmt`

- 按最近创建时间排序, 以方便人类读的方式显示大小 alias llct='ls -lhc'
`llct`

- 仅隐藏条目, 按名称排序,  但无法通过颜色来区文件类型
`llh`

- 所有条目, 按名称排序, 先显示隐藏文件和目录, 再显示非隐藏文件和目录, 长格式, 但无法通过颜色来区文件类型
`lla`

- 所有条目，按大小排序, 以方便人类读取的方式显示大小 alias llas='ls -AlhS'
`llas`

- 所有条目, 按文件类型排序, 以合适的方式显示文件大小 alias llae='ls -AlhX'
`llae`

- 所有条目, 按最近修改时间排序, 以合适的方式显示文件大小 alias llamt='ls -Alhtr --time-style=iso'
`llamt`

- 所有条目, 按最近创建时间排序, 以合适的方式显示文件大小 alias llact='ls -Alhct --time-style=iso'
`llact`

- 显示给定目录的长格式信息, 而非目录中内容的信息 alias lld='ls -ld'
`lld`
