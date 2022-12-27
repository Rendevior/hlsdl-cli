# hlsdl-cli
Simple HLS playlist downloader written in Shell

# Installation
```sh
curl -sLo "${PREFIX}/bin/hlsdl-cli" https://raw.githubusercontent.com/Rendevior/hlsdl-cli/master/hlsdl-cli
chmod +x "${PREFIX}/bin/hlsdl-cli"
```
## Options
```
-v                           : Print Version and Exit
-h                           : Print Help
-z                           : Supress output (only shows errors)
-q [high|low]                : Choose specific Quality
-u, --user-agent=[useragent] : Set an User-Agent Header
-r, --referer=[referer]      : Set an HTTP Referer Header
-o [filename]                : Output filename
-d [dir]                     : Cache to specific directory (default: ~/.ffmhls)
-c [N]                       : Set number of connection will be used for downloading [1-16]
--header=[headers]           : Set a custom HTTP Headers for request
```
## How to use
Example usage:
```sh
hlsdl-cli -o filename.mp4 -d ./.cache -q 720 "https://example.com/example.m3u8"
```
## Dependencies
- sed
- grep
- awk
- curl
- openssl
- ffmpeg
