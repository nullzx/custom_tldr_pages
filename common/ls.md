

> List directory contents.
> More information: <https://www.gnu.org/software/coreutils/ls>.

- 每行只显示一个([1])条目 
`alias l='ls -1'`

- 按名称排序，长格式([l]ong)，文件大小以字节形式展现
`alias ll='ls -l'`


- 按大小排序([S]ize)，以人([h]uman)习惯的方式查看条目的大小，以人([h]uman)习惯的方式查看条目的大小
`alias lls='ls -Slh'`

- 按文件类型排序([e]xtension,即扩展名), 长格式([l]ong), 以人([h]uman)习惯的方式查看条目的大小
`alias lle='ls -Xlh'`

- 按最近修改时间([m]odify [t]ime)排序, 长格式([l]ong),以人([h]uman)习惯的方式查看条目的大小
`alias llmt='ls -tlh --time-style=iso'`


- 按最近(([r]everse))状态修改时间([c]hange)时间([t]ime)排序, 长格式([l]ong), 以人([h]uman)习惯的方式查看条目的大小
`alias llct='ls -rctlh --time-style=iso'`


- 仅显示隐藏([h]ide)条目, 按名称排序, 长格式([l]ong), 以人([h]uman)习惯的方式查看条目的大小，但无法通过颜色来区文件类型
`llh () {`
`    ls -AlhF | awk '$9 ~ /^\./'`
`    return 0`
`}`


- 所有条目，按名称排序, 先显示隐藏文件和目录, 再显示非隐藏文件和目录, 长格式([l]ong)，以人([h]uman)习惯的方式查看条目的大小，但无法通过颜色来区文件类型
`lla () {`
`    llh`
`    ls -lhF | tail -n +2`
`    return 0`
`}`

- 所有条目([A]ll)，按大小排序([S]ize), 长格式([l]ong), 以人([h]uman)习惯的方式查看条目的大小
`alias llas='ls -ASlh'`

- 所有条目([A]ll), 按文件类型排序([e]xtension,即扩展名), 长格式([l]ong), 以人([h]uman)习惯的方式查看条目的大小
`alias llae='ls -AXlh'`

- 所有条目([A]ll), 按最近修改([m]dify)时间([t]ime)排序, 长格式([l]ong), 以人([h]uman)习惯的方式表示条目的大小
`alias llamt='ls -Atlh --time-style=iso'`


- 所有条目([A]ll), 按最近(([r]everse))状态修改时间([c]hange)时间([t]ime)排序, 长格式([l]ong), 以人([h]uman)习惯的方式表示条目的大小
`alias llact='ls -Arctlh --time-style=iso'`

- 显示给定目录([d]irctory)的, 长格式([l]ong), 而非目录中内容的信息
`alias lld='ls -ld'`

