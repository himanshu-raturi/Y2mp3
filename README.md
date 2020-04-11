# Y2mp3
# YouTube MP3 download Application
![1_nMcCRZ0LDkL-Y7FoSBwCyA](https://user-images.githubusercontent.com/27719791/79046759-5f750380-7c30-11ea-8761-7ad0d0182b66.jpeg)> Y2mp3(YouTube MP3 download Application) convert your YouTube videos to mp3 files online in the highest available quality and download them for free.....Isn't it exciting.....



## Table of Contents
You're sections headers will be used to reference location of destination.

- [Description](#description)
- [Use of Badges](#use-of-badges)
- [Features](#features)
- [Installation](#installation)
- [Code Snippet](#code-snippet)
- [Getting Started](#getting-started)
- [Tools](#tools)



---

## Description
> YouTube MP3 download Application is build in python using `Pyqt5` library specifically `QtCore`  `QtGui`  `QtWidgets` for **GUI** development and `BeautifulSoup` `requests` `youtube_dl` `urllib.request` `pafy` for **Back end downloading operations**.
![basic](https://user-images.githubusercontent.com/27719791/79046018-de1b7200-7c2b-11ea-914e-7efc9a1dfa95.png)

---

### Use of Badges

[![Build Status](http://img.shields.io/travis/badges/badgerbadgerbadger.svg?style=flat-square)](https://travis-ci.org/badges/badgerbadgerbadger) [![Github Issues](http://githubbadges.herokuapp.com/badges/badgerbadgerbadger/issues.svg?style=flat-square)](https://github.com/badges/badgerbadgerbadger/issues)  [![Badges](http://img.shields.io/:badges-9/9-ff6799.svg?style=flat-square)](https://github.com/badges/badgerbadgerbadger)

- For more on these wonderful `badges`, refer to <a href="http://badges.github.io/badgerbadgerbadger/" target="_blank">`badgerbadgerbadger`</a>.





## Features
  * search for YouTube videos 
  * choose video from top 5 results from YouTube 
  * you can copy the download link from copy button 
  * download any video from the result
  * Choose destination for downloading video
  * Prompt error message when error occurred.
  
  





## Installation
* install `PyQt5` python library using pip
```python
pip install PyQt5
```
```
python
pip3 install PyQt5

```
Install youtube_dl for downloading videos from YouTube
```python
pip install youtube_dl
```
Download Youtube_dl - [youtube_dl](https://pypi.org/project/youtube_dl/)

Install requests
```python
pip install requests
```
Install pafy 
```python
pip install pafy
```




## Code Snippet

```python 

 text= self.lineEdit.text()   
        query = urllib.parse.quote(text)
        url = "https://www.youtube.com/results?search_query=" + query
        response = urllib.request.urlopen(url)
        html = response.read()
        response.close()
        soup = BeautifulSoup(html, 'html.parser')
         
        for vid in soup.findAll(attrs={'class':'yt-uix-tile-link'}):
            if i<5:
                i+=1   
                temp = 'https://www.youtube.com' + vid['href']
                self.link.append(temp)
                self.thumb.append('http://img.youtube.com/vi/'+vid['href'].replace('/watch?v=','')+'/default.jpg')
​
​
                options = {
            'format': 'bestaudio/best', # choice of quality
            'postprocessors': [{
                'key': 'FFmpegExtractAudio',
                'preferredcodec': 'mp3',
                'preferredquality': '320',
                }],
            'extractaudio' : True,      # only keep the audio
            'audioformat' : "mp3",      # convert to mp3 
             
            }

```
## Getting Started
```
git clone https://github.com/himanshurishikesh731/Y2mp3.git
```
* install the required tools 

* fork or download the repo 

* run the following command in terminal

```
python3 y2mp3.py
```


![final](https://user-images.githubusercontent.com/27719791/79046085-42d6cc80-7c2c-11ea-99fb-0efc9efcaff2.png)


## Tools
### References
* [PyQt](https://riverbankcomputing.com/software/pyqt/intro)
* [Sublime Text](https://www.sublimetext.com/3)
* [Beautifulsoup](https://pypi.org/project/beautifulsoup4/)
* [Youtube_dl](https://pypi.org/project/youtube_dl/)
* [Python](https://www.python.org/)



---



## License
---
[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)


[Back To The Top](#YouTube MP3 download Application)
