---
layout: post
title:  "Audio and Video Tags"
categories: jekyll update
---

### Question:
Describe the `audio` and `video` tags and how they enhance the user experience. Provide examples of their usages.

<hr>

 <h1 style="color:#3CCAE6">Audio Tag</h1>

 Audio can add depth to a site by giving the user an experience more aligned with our media center world nowadays with some notable examples such as Pandora, for our purposes our examples will be simple.

This is an example of the basic syntax for the audio tag :

**Audio Tag Syntax :**

```html
<audio src="../audio/butthead.mp3" controls>
<p>If you are reading this, it is because your browser does not support the audio element.</p>
</audio>
```
<br>

Starts off with the audio tag which takes an attribute of `src` which points to where that sound file is. Then we have `controls` , this gives us the panel to press play and pause. The audio won't work because the audio file doesn't exits, I just wanted to give you an idea of what it will look like. 

**Result:**

<audio src="../audio/butthead.mp3" controls>
<p>If you are reading this, it is because your browser does not support the audio element.</p>
</audio>

<br>







 <h2 style="color:#3CCAA1">Audio Formats</h2>

In the above example we use an .mp3 audio file but this isn't a great idea when using in a live site becasue not all users will be able to hear it if their on a browser that doesn't support it.

Three types of audio formats are used on the web they are: MP3, Ogg, and Wav. They all do the same thing but the .wav is uncompressed so you only want to use this type when you small file sizes anything else use the other two. 

This brings up an important point, if .mp3 files arent' supported on all browsers and .wav isn't always going to be the best option then what. Well you can combine the file types much like you do with the font-family property to give a back up if that audio type isn't supported in that browser. 

**Syntax for multiple file types:** 

```html
<audio> 
  <source src="WhiteChristmas.mp3">   <!-- first file will play if supported -->

  <source src="WhiteChristmas.ogg">   <!-- second file will play if first not supported -->

  <p>Your browser does not support this audio file. Try a different browser</p>   
    <!--The paragarph will pop up if neither file type are supported  -->
</audio>
```
<br>

<table class="table table-striped">
      <caption style="font-weight: bold;text-align: center;color: black;font-size: 20px; text-transform: uppercase;">Browser Support for audio formats</caption>
    <thead>
        <tr>
            <th style="text-align: center;">
                Browser
            </th>
            <th style="text-align: center;">
                .mp3
            </th>
            <th style="text-align: center;">
                .ogg
            </th>
            <th style="text-align: center;">
                .wav
            </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Internet Explorer</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                no
            </td>
            <td style="text-align: center;">
                no
            </td>
        </tr>
        <tr>
            <th>Chrome</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
        <tr>
           <th>Firefox</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
        <tr>
           <th>Safari</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                no
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
          <tr>
            
               <th> Opera</th>
        
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
    </tbody>
</table>

Let's show one last audio clip. What movie is this audio clip from? 


```html
<audio controls>
  <source src="../audio/style.wav" controls></source>
  <source src="audio/beep.ogg" controls></source>
  Your browser isn't invited for super fun audio time.
</audio>
```

**Result:**
<audio controls>
  <source src="../audio/style.wav" controls></source>
  <source src="audio/beep.ogg" controls></source>
  Your browser isn't invited for super fun audio time.
</audio>


 <h1 style="color:#3CCAE6">Video Tag</h1>

Now we have the video tag to talk about but what better way to talk about then show video. The examples below illustrate some ways they can be used. The most popular examples of this tag would be Youtube although they use a lot JavaScript to get the videos to do more cool stuff.


Code: 

```html
<div style="text-align: center;">
<video autoplay loop  width="400px" >
<source src="../video/624073109.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</div>
```


Video with loop and autoplay without controls:

<div style="text-align: center;">
<video autoplay loop  width="400px" >
<source src="../video/624073109.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</div>

Code: 

```html
<div style= "text-align: center;">
<video autoplay   width="400px" controls>
<source src="../video/624073109.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</div>
```


Video without loop. With autoplay and controls:

<div style= "text-align: center;">
<video autoplay   width="400px" controls>
<source src="../video/624073109.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</div>



Code: 

```html
<div style= "text-align: center;">
<video autoplay   width="400px" controls>
<source src="../video/624073109.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</div>
```

Video without autoplay with controls:

<div style= "text-align: center;" >
<video width="400px" controls>
<source src="../video/624073109.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</div>

<br>

<table class="table table-striped">
      <caption style="font-weight: bold;text-align: center;color: black;font-size: 20px; text-transform: uppercase;">Browser Support for video formats</caption>
    <thead>
        <tr>
            <th style="text-align: center;">
                Browser
            </th>
            <th style="text-align: center;">
                MP4
            </th>
            <th style="text-align: center;">
                WebM
            </th>
            <th style="text-align: center;">
                Ogg
            </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Internet Explorer</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                no
            </td>
            <td style="text-align: center;">
                no
            </td>
        </tr>
        <tr>
            <th>Chrome</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
        <tr>
           <th>Firefox</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
        <tr>
           <th>Safari</th>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
          <tr>
            
               <th> Opera</th>
        
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
            <td style="text-align: center;">
                yes
            </td>
        </tr>
    </tbody>
</table>


 <h1 style="color:#3CCAE6">Summary</h1>

 This was a quick article showing the video and audio tags and what can be done with them. This is by means no mean an extensive look into these tags but covers the basics. 