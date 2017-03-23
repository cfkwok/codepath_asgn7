# codepath_asgn7
Kali vs WordPress

# Project 7 - WordPress Pentesting

Time spent: 5 hours spent in total

> Objective: Find, analyze, recreate, and document **3 vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) OVE-20160717-0003
  - [x] Summary: "Two Cross-Site Scripting vulnerabilities exists in the playlist
functionality of WordPress. These issues can be exploited by convincing
an Editor or Administrator into uploading a malicious MP3 file. Once
uploaded the issues can be triggered by a Contributor or higher using
the playlist shortcode." (Link 1)
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.7.3
  - [X] GIF Walkthrough: http://imgur.com/hjBG0KU
  - [X] Steps to recreate: "The following MP3 file can be used to reproduce this issue:

https://www.securify.nl/advisory/SFY20160742/xss.mp3

1) upload MP3 file to the Media Library (as Editor or Administrator).
2) Insert an Audio Playlist in a Post containing this MP3 (Create Audio
Playlist)." (Link 1)
  - [X] Affected source code: https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7
    - [Link 1](http://seclists.org/oss-sec/2017/q1/563)
1. (Required) Stored XSS
  - [X] Summary: "A stored XSS vulnerability in WordPress allows an user with the posting capability to compromise the website." (Link 1)
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.3
  - [X] GIF Walkthrough: http://imgur.com/xGyxzV4
  - [X] Steps to recreate: Post in plain text <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a>
  - [] Affected source code: 
    - [Link 1](https://klikki.fi/adv/wordpress3.html)
1. (Required) Publish Post & Mark as Sticky Permission Issue
  - [X] Summary: vulnerable to a cross-site scripting vulnerability when processing shortcode tags (Link 1)
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.3.1
  - [X] GIF Walkthrough: http://imgur.com/f9mxo2W
  - [X] Steps to recreate: Put TEST!!![caption width="1" caption='<a href="' ">]</a><a href="http://onMouseOver='alert(1)'">Click me</a> in a post
  - [] Affected source code:
    - [Link 1](https://wordpress.org/news/2015/09/wordpress-4-3-1/)
    - [Link 2](http://blog.knownsec.com/2015/09/wordpress-vulnerability-analysis-cve-2015-5714-cve-2015-5715/)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
