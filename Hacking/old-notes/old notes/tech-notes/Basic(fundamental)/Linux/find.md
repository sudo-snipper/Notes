## find
`find -type f -name file`
> -type d :: for directory

`find ./ -type f -size 1033c ! -executable`
> find from current directory
> -size 1033 bytes
> ! -executable :: file with no executable permission

`find / -type f -user username -group groupname`
