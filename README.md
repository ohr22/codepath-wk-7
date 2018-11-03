# codepath-wk-7
# Project 7 - WordPress Pentesting

Time spent: 4 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenticated Stored XSS in Youtube URL Embed
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.0-4.7.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: ![dsvhyc1avj](https://user-images.githubusercontent.com/40126473/47955570-53cbda80-df70-11e8-9c06-8046cb1aecd4.gif)
  - [ ] Steps to recreate: Login as admin, create a new post. Post a youtube link with XSS [embed src='https://youtube.com/embed/12345\x3csvg onload=alert("woah!")\x3e'][/embed]
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    
1. (Required) Authenticated Shortcode Tags XSS
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.3
    - Fixed in version: 4.3.1
  - [ ] GIF Walkthrough: ![y69k0jza8d](https://user-images.githubusercontent.com/40126473/47955574-69d99b00-df70-11e8-852b-f03aaef528f9.gif)
  - [ ] Steps to recreate: Login as admin, create a new post. Post the following in the body:  [caption width="1" caption='<a href="' ">]</a><a href=" onmouseover='alert("stop")' ">Click me!</a>
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    
1. (Required) Authenticated Stored XSS
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: ![m4noucjgjo](https://user-images.githubusercontent.com/40126473/47955577-73fb9980-df70-11e8-84d6-104651b3048a.gif)
  - [ ] Steps to recreate: Login as admin, create a new post. Paste the following: <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a>. When mouse hovers, XSS pops up
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

GIFs created with [RecordIt](http://recordit.co/).

## Notes

Hard to research some of the exploits. Also, ran into issues with setting up Kali. 

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
