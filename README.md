# Homework Assignment #12: Object Oriented Programming

# Overview

In object oriented programming (OOP) one use an object template (sometimes in the form of a class) or prototype that serves as model. That model is then instanciated as many times as required to create different "beings" which are also objects.
An object prototype can have properties and methods. Let's imagine that we create a model object named car. A car has properties including color, length, width, height, brand, model, year, etc. That car object can do things, move, accelerate, brake, honk, etc. Everytime the model is instanciated we give it a name and set some or all of its properties. We can set properties when we first intanciate it or later on.

# In which cases would an OOP pattern be a better choice?

Object-oriented design patterns typically show relationships and interactions between classes or objects, without specifying the final application classes or objects that are involved. Patterns that imply mutable state may be unsuited for functional programming languages, some patterns can be rendered unnecessary in languages that have built-in support for solving the problem they are trying to solve, and object-oriented patterns are not necessarily suitable for non-object-oriented languages.
In short whenever a model is used to specify objects having similar properties and behavior then objects oriented programming is a good approach.

# Example of Application using OOP: playlist organizer

## Overview

The user can create playlists with different tracks.

## User stories

- At the launch the user is prompted to either quit, create or select an existing playlist.
- If he chooses to create a playlist he needs to key in the name and that will save the playlist.
- If he selects a playlist he can then either quit, delete the playlist, add a track or select a track.
- If he selects adding a track he needs to key in the name of the track to be added.
- If he selects a track he can delete it.

## Pseudo code

### OBJECTS

Object Index  
_Properties_

- List of playlists

_Methods_

- Add playlist
- Delete playlist

Object Playlist:  
_Properties_

- list of tracks

_Methods_

- Add track
- Remove track

### MAIN CODE

While user doesn't quit

> Prompt to select an option: quit, add playlist, enter a playlist

> if quit then break

> if add playlist then prompt to enter the name.
>
> > index = new Index(initialize with list of playlist from memory)  
> > add the new playlist to index
> > save updated index to memory
> > back to previous screen

> if select a playlist then
>
> > playlist = new Playlist(initialize with list of tracks from memory )  
> > Print the list of tracks for the playlist  
> > Prompt to select an option: quit, delete playlist, add track, select track  
> > if quit then break

> > if add track then
> >
> > > prompt to enter the name
> > > add the new playlist to index  
> > > back to playlist screen

> > if remove track then
> >
> > > remove the track from playlist and save to memory
> > > back to playlist screen

> if delete playlist then
>
> > delete playlist and go back to main screen
