Joshua Murphy

CS 595 - Web Security

Assignment 4 

<br/>

## Assignment Description Part 1 - Which public sites are framable?


### Table 

|URL                   |iframe allowed|x-frame-options                                                             |
|----------------------|-------------|----------------------------------------------------------------------------|
|about.com             |-            |SAMEORIGIN                                                                  |
|akamaized.net         |404          |                                                                            |
|alexa.com             |-            |SAMEORIGIN                                                                  |
|alibaba.com           |O            |                                                                            |
|amazon.fr             |-            |SAMEORIGIN                                                                  |
|amazon.it             |-            |SAMEORIGIN                                                                  |
|asahi.com             |O            |                                                                            |
|asus.com              |-            |SAMEORIGIN                                                                  |
|bandcamp.com          |O            |                                                                            |
|bbc.co.uk             |-            |DENY                                                                        |
|bbc.com               |O            |                                                                            |
|bp3.blogger.com       |404          |                                                                            |
|brandbucket.com       |-            |SAMEORIGIN                                                                  |
|businessinsider.com   |-            |SAMEORIGIN                                                                  |
|buzzfeed.com          |-            |SAMEORIGIN                                                                  |
|cnbc.com              |-            |content-security-policy: frame-ancestors 'self'                             |
|cnil.fr               |-            |SAMEORIGIN                                                                  |
|cointernet.com.co     |O            |                                                                            |
|debian.org            |-            |SAMEORIGIN                                                                  |
|depositfiles.com      |-            |SAMEORIGIN                                                                  |
|dot.tk                |-            |Referrer Policystrict-origin-when-cross-origin                              |
|draft.blogger.com     |-            |SAMEORIGIN                                                                  |
|drive.google.com      |-            |DENY                                                                        |
|dropbox.com           |-            |DENY                                                                        |
|dw.com                |O            |                                                                            |
|ea.com                |-            |SAMEORIGIN                                                                  |
|ebay.co.uk            |-            |SAMEORIGIN                                                                  |
|elmundo.es            |O            |                                                                            |
|elpais.com            |O            |                                                                            |
|en.wikipedia.org      |404          |                                                                            |
|enable-javascript.com |O            |                                                                            |
|etsy.com              |-            |SAMEORIGIN                                                                  |
|evernote.com          |-            |SAMEORIGIN                                                                  |
|fb.me                 |-            |DENY                                                                        |
|feedburner.com        |-            |DENY                                                                        |
|files.wordpress.com   |-            |SAMEORIGIN                                                                  |
|finance.yahoo.com     |-            |SAMEORIGIN                                                                  |
|focus.de              |O            |                                                                            |
|francetvinfo.fr       |O            |                                                                            |
|guardian.co.uk        |-            |SAMEORIGIN                                                                  |
|harvard.edu           |-            |SAMEORIGIN                                                                  |
|hugedomains.com       |-            |ALLOW-FROM https://hugedomains.com/                                         |
|id.wikipedia.org      |404*         |loads normally outside iframe, but says cannot find when in iframe          |
|imgur.com             |-            |DENY                                                                        |
|independent.co.uk     |-            |content-security-policy: frame-ancestors 'self' https://*.brightsites.co.uk;|
|instagram.com         |-            |SAMEORIGIN                                                                  |
|interia.pl            |O            |                                                                            |
|kakao.com             |O            |                                                                            |
|kompas.com            |-            |SAMEORIGIN                                                                  |
|last.fm               |-            |SAMEORIGIN                                                                  |
|latimes.com           |-            |DENY                                                                        |
|leparisien.fr         |O            |                                                                            |
|lg.com                |-            |frame-ancestors 'self' www.lgechat.com lgechat.com;                         |
|m.wikipedia.org       |404*         |200 when curling, but cannot find page when in or out of iframe             |
|mega.nz               |-            |DENY                                                                        |
|mozilla.com           |-            |DENY                                                                        |
|msn.com               |-            |SAMEORIGIN                                                                  |
|nature.com            |-            |DENY                                                                        |
|naver.com             |-            |DENY                                                                        |
|nba.com               |-            |SASAMEORIGIN                                                                |
|netflix.com           |-            |DENY                                                                        |
|netvibes.com          |-            |DENY                                                                        |
|networkadvertising.org|O            |                                                                            |
|nhk.or.jp             |O            |                                                                            |
|nydailynews.com       |O            |                                                                            |
|ovh.com               |-            |SAMEORIGIN                                                                  |
|pcmag.com             |O            |                                                                            |
|photobucket.com       |-            |SAMEORIGIN                                                                  |
|pinterest.com         |-            |SAMEORIGIN                                                                  |
|play.google.com       |-            |SAMEORIGIN                                                                  |
|reuters.com           |O            |                                                                            |
|rfi.fr                |-            |DENY                                                                        |
|rtve.es               |O            |                                                                            |
|ru.wikipedia.org      |O            |                                                                            |
|search.google.com     |-            |SAMEORIGIN                                                                  |
|sedo.com              |-            |SAMEORIGIN                                                                  |
|soratemplates.com     |O            |SAMEORIGIN                                                                  |
|spiegel.de            |O            |                                                                            |
|spotify.com           |-            |DENY                                                                        |
|ssl-images-amazon.com |404          |                                                                            |
|telegram.me           |-            |SAMEORIGIN                                                                  |
|thoughtco.com         |-            |content-security-policy: frame-ancestors 'self'                             |
|time.com              |-            |SAMEORIGIN                                                                  |
|trustpilot.com        |-            |DENY                                                                        |
|twimg.com             |404          |                                                                            |
|ucoz.ru               |-            |SAMEORIGIN                                                                  |
|upenn.edu             |-            |SAMEORIGIN                                                                  |
|usgs.gov              |-            |SAMEORIGIN                                                                  |
|usnews.com            |O            |                                                                            |
|video.google.com      |-            |SAMEORIGIN                                                                  |
|wa.me                 |-            |DENY                                                                        |
|washington.edu        |O            |                                                                            |
|wikia.com             |-            |SAMEORIGIN                                                                  |
|wiley.com             |-            |SAMEORIGIN                                                                  |
|wired.com             |O            |                                                                            |
|gov.uk                |O            |ALLOWALL                                                                    |
|over-blog.com         |-            |DENY                                                                        |
|weebly.com            |-            |SAMEORIGIN                                                                  |
|youtube.com           |-            |SAMEORIGIN                                                                  |
|zoom.us               |-            |SAMEORIGIN     

</br>

## Assignment Description part 2 - Frame Path attack



## Video Links




## Extra Credit






# References
