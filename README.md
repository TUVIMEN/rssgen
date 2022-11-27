# rssgen

A bash script for creating rss feeds.

## Installation
    
    install -m 755 rssgen /usr/bin

## Usage

    rssgen [OPTION]... [URL]

RSS feed of THE\_HIGH\_COMMAND profile on bitchute

    rssgen -t THE_HIGH_COMMAND -p 'https://static-3.bitchute.com/live/channel_images/2pZ6g7DTmL61/lKUxB9HjipzMxGHRlha9pZHy_small.jpg' -d 'Auto generated page of THE_HIGH_COMMAND profile' -D 'hgrep "div +class=\"channel-videos-details text-right hidden-xs\"; span @p\"%i\\n\"" | date +%F -f -' -T 'hgrep "div +class=\"channel-videos-title\"; a @p\"%i\\n\""' -L 'hgrep "div +class=\"channel-videos-title\"; a +href @p\"https://www.bitchute.com%(href)a\\n\""' -I 'hgrep "div +class=\"channel-videos-text\" @p\"%i\\n\"" | sed "/^[ \\t]*$/d"' 'https://www.bitchute.com/channel/the_high_command/'

Get some help

    rssgen -h
