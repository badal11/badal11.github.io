---
layout: post
title: Linked-List based Music-Player 
date: 2019-10-29 09:56:00-0400
description: 
tags: project
categories: class-project
giscus_comments: false
related_posts: false
featured: false
---

# Linked List-based Music Player
This code is to build a basic music player with play/pause, previous, and next functionalities. The music player uses an audio element to play music tracks, and there is also a linked list (`DoubllyLinkedList`) to store information about different music tracks. Here's a breakdown of the code:

### HTML (index.html)

- The HTML structure includes various elements for displaying music information, buttons, timers, and volume controls.

### JavaScript (script.js)

#### Variables
- Various variables are declared to store references to DOM elements such as buttons, timers, sliders, etc.
- `musicObj`: An HTML audio element created dynamically. It's set with a default music track.

#### Event Listeners
1. **Play/Pause Button:**
   - Toggles the play/pause state of the music track using the `playpauseTrack` function.

2. **Next Button:**
   - Triggers the `dll.traverse` function to get information about the next music track.
   - Updates the `musicObj.src` with the new music track path.
   - Plays the new music track and updates the music title and button colors.

3. **Previous Button:**
   - Triggers the `dll.traverse` function to get information about the previous music track.
   - Updates the `musicObj.src` with the new music track path.
   - Plays the new music track and updates the music title and button colors.

4. **Volume Slider:**
   - Listens for changes in the volume slider and adjusts the volume of the music accordingly.

5. **Music Slider:**
   - Listens for changes in the music slider and adjusts the position of the music accordingly using the `changeMusicPos` function.

#### Functions
- `playpauseTrack()`: Plays or pauses the music track based on the current play/pause state.
- `updateMusicSlider()`: Updates the position of the music slider based on the current time of the music track.
- `changeMusicPos()`: Changes the position of the music based on the value of the music slider.
- `changeMusicTitle(title)`: Updates the displayed music title.
- `changePrevNextColor()`: Updates the color of the previous and next buttons based on whether there are previous or next tracks in the playlist.

### JavaScript (doublelinkedlist.js)

- Defines a `Node` class representing a node in the doubly linked list.
- Defines a `DoubllyLinkedList` class with methods for pushing nodes, setting the default pointer, and traversing the linked list.
- Creates an instance of the `DoubllyLinkedList` class (`dll`) and inserts three music tracks into the linked list.

### Conclusion

This code creates a basic music player with functionality to play, pause, go to the next or previous track, adjust volume, and seek through the track. The music playlist is implemented using a doubly linked list.