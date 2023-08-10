# rss.sh

RSS generator in POSIX shell script


## How to use

```
rssgen -a "your.domain" -t "rss title" -d "description" path > feed.rss
```

Path can be a glob, the result will be passed to a find command.

For each item *rssgen* will search 3 things on your matched files:

- `<title>` tag for extracting the item title
- `<meta name="description"` for getting the description
- `<meta name="revised"` for the publication date

And with those values an rss feed item is made. Check the [feed.rss](feed.rss)
file and the posts folder.


### Arguments

- `-a`: set the domain
- `-c`: set copyright owner
- `-d`: set the description
- `-t`: set title field
- `-s`: set stylesheet
- `-l`: set language field
- `-h`: show this help
- `-v`: print the version

Run `rssgen -h` to see all options


## Dependencies

- a POSIX compatible shell
- find
- grep
- sed 


## Meta

Part of weblibs project, licensed under the [MIT license](LICENSE).
