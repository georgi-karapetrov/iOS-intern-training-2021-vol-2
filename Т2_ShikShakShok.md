# Introduction

[All work and no play makes Jack a dull boy](https://i.guim.co.uk/img/static/sys-images/Film/Pix/pictures/2012/5/22/1337709078456/The-Shining-008.jpg?width=300&quality=45&auto=format&fit=max&dpr=2&s=7a18528291f53d36c11d81a39fc4362e). And what better way to relax after a hard day at work than a trusty ol' game of Tic-Tac-Toe on your mobile device (plenty of ways, actually).

## Requiremets
Your task is to create an iOS application which allows the user to enter their name and commence a relaxing game of [Tic-Tac-Toe](https://en.wikipedia.org/wiki/Tic-tac-toe). The game should be playable and look good on both iPhones and iPads. The opponent should be an AI, choosing random square from the available ones on the field.

## Before you start
When approaching tasks of this sorts (creating simple games), it is a good idea to avoid tight-coupling the user interface and the game logic. This translates to simply having two (or more) layers which have distinct responsibilites. For instance, in this case this means having an 'engine' for the game, which contains and handles the field matrix, and a seperate 'graphics layer', which handles the drawing of the current state of the field matrix. This way, the application could (in theory) be easily ported to a console version (the game engine will be 'plugged' in a different graphics layer, which will deal with the drawing of X's and O's in the terminal).

## What to use
The beauty of CocoaTouch. More specifically [UICollectionViewController](https://developer.apple.com/documentation/uikit/uicollectionviewcontroller?changes=_3&language=objc). Every cell of the tic-tac-toe field matrix should be presented to the user via the UICollectionView of the said controller.

## From Tic-Tac-Toe to Tunak-Tunak-Tun
It does not take much effort to convince you that Tic-Tac-Toe is a boring game. This is rather convenient in our case, as it will be really hard to make it more boring than it currently is. So let's try to improve it a little. Transform your current Tic-tac-toe engine to a ~~Shik-Shak-Shok~~ **Tunak-Tunak-Tun** engine. The rules of ~~Shik-Shak-Shok~~ **Tunak-Tunak-Tun**  are almost identical to Tic-Tac-Toe's. The only difference is that instead of three states per square, there are [**Eleven**](http://digitalspyuk.cdnds.net/17/50/980x490/landscape-1512999743-screen-shot-2017-12-11-at-134204.jpg) - [Se7en](https://www.imdb.com/title/tt0114369/) = 4 ([quick maffs](https://youtu.be/M3ujv8xdK2w?t=10)). This is represented by different colors of the X's, O's or something else. The win condition is to have three symbols of the same colour (red, green, blue or whatever you choose) in a column, row or diagonal. Who made the winning move should also be taken into consideration (as to who to award the victory to).

## Tunak tunak tun - da da da 
If you are not familiar with Tunak-Tunak, please be ashamed of yourself and get educated [here](https://www.youtube.com/watch?v=vTIIMJ9tUc8) now. Resources for the Tunak-Tunak-Tun can be found [here](/resources/T2).