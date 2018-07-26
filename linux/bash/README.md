# bash

## Useful tips

### Count program stdout lines

```bash
$ program | tee >(wc -l)
```
### Remove pattern from a file

```bash
sed -ri -e '/<pattern>/d' file

sed -ri -e '/<pattern>$/d' file     # include line break
sed -ri.bak -e '/<pattern>/d' file  # writes backup to file.bak
```

Use with a grep like tool ([rg](https://github.com/BurntSushi/ripgrep)) and
`xargs` to run in multiple files.

```bash
rg <patter> -l | xargs sed -ri -e '/<pattern>$/d'
```
