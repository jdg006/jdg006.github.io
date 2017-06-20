---
layout: post

title: BlocJams

feature-img: "img/sample_feature_img.png"

thumbnail-path: "https://d13yacurqjgara.cloudfront.net/users/3217/screenshots/2030966/blocjams_1x.png"

short-description: Music-playing Website building walkthrough

---


**Summary**
 
{:.center}
![]({{ https://github.com/jdg006/portfolio-iro }}/img/blocjams homepage.png)
The bloc-jams project was a project that was meant to teach me how to build a website. The website that was built was a  music playing website and exposed me to ways to include audio files on a webpage. The project also introduced me to issues regarding the styling of a website and the overall structure that a website needs to have.
 
**Explanation**
 
Bloc-jams was a project created by the employees of bloc to introduce students to website building. The student was to follow along as the website was built. The website was split up into different sections and in each of those sections the student was assigned work that would allow them to demonstrate their understanding of how that particular section of the website worked. The project first showed the student how to set up the html of each webpage and then how to style the web pages. It then went over the more complex steps of making the web page dynamic by using DOM scripting. The project concluded with refactoring the javascript used in the website to use jQuery. My role in this project was that of the student.
 
**Problem**
 
The problem that this project was meant to solve was that people needed an online music player to play their music from. The website needed to be able to take audio files and put them into a format that was understandable by the user. The website also needed to allow the user to have control over the audio files. The user needed to be able to pause, rewind, skip to the next song or change the song back to the previous song in the queue as well as also tracking the current position of the song playing and being able to skip to a particular part of the current song playing. 
 
**Solution**
 
In order to play audio files through the website the bloc-jams project utilized the Buzz music library. This library allowed us to play, pause, skip, seek, and track the audio file that we were currently playing. We had to use some javascript to be able to make the icons on the music player functional and allow the user to control the audio file using the icons. The example code below shows what needed to be done to get the next button to work on the audio files on the site:
```javascript
var nextSong = function() {
    var currentSongIndex = trackIndex(currentAlbum, currentSongFromAlbum);
    currentSongIndex++;

    if (currentSongIndex >= currentAlbum.songs.length) {
        currentSongIndex = 0;
    }

    var lastSongNumber = currentlyPlayingSongNumber;

    setSong(currentSongIndex + 1);
     currentSoundFile.play();
     updateSeekBarWhileSongPlays();

    updatePlayerBarSong();

    var $nextSongNumberCell = $('.song-item-number[data-song-number="' + currentlyPlayingSongNumber + '"]');
    var $lastSongNumberCell = $('.song-item-number[data-song-number="' + lastSongNumber + '"]');

    $nextSongNumberCell.html(pauseButtonTemplate);
    $lastSongNumberCell.html(lastSongNumber);
};
```
Most of the other controls were similiar to this one, but with other functions such as previous song, play/pause, and seek. We also used DOM scripting to arrange the music files into positions that were understandable by the user. 
 
**Results**

{:.center}
![]({{ https://github.com/jdg006/portfolio-iro }}/img/SongPlayer.png)
 
The result of the project was a functional, music-playing website that was easy to understand and intuitive to control. The website was styled well and was aesthetically appealing. 
 
**Conclusion**
 
In the end the project did all that it sought to do from its onset. It reviewed basic website building techniques and made me learn and understand more advanced coding practices. The project allowed me to write my own code for the website at times, but would then always show what the best practice was for the that particular part of the website. I learned that there are many ways to write the code for a website and two very different sets of code can have essentially the same outcome. The project did make me realize that a great deal of foresight is required to write succinct, well-functioning code. Much of the code that I wrote by myself I later learned would have made subsequent sections of the website difficult to create or fit together with the rest of the website. Going forward I will make sure to take the time to plan ahead before diving into the code I need to write for a website. 