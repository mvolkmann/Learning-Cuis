# Learning-Cuis

Greetings and Welcome!!

Smalltalk is a wonderful way of doing things in software and Cuis is a particular implementation of this language and its environment.

Cuis shares ideas with other Smalltalk implementations and shares much of its implementation mechanics with the [Squeak](http://www.squeak.org) and [Pharo](http://www.pharo.org/) environments.

Smalltalk is a big world, which you can use to do just about anything that can be done with a computer.

Cuis is different in that it is actively managed to become smaller, where each component carries its own weight with the minimum of baggage.

We think this makes Cuis easier to learn.

One measure of a Smalltalk's size is the number of Classes which implement its code.

If you open a Workspace in many Smalltalks, you can type and print (cmd-p)
````Smalltalk
	Smalltalk allClasses size.
````   

Here are the ***class counts*** for some related implementations.

Cuis and Pharo both forked from Squeak around release 3.7

| Cuis | Squeak | Pharo |
| ---- | ------ | ----- |
| |Smalltalk-80 (236 Classes) | |
| |Squeak 1.1 (327 Classes) | |
| |Squeak 2.0 (509 Classes) | |
| |Squeak 3.0 (1545 Classes) | |
|Cuis Fork |Squeak 3.7 |Pharo Fork |
|Cuis 1.0 (599 Classes) |Squeak 3.8 (2321 Classes) |Pharo 2.0 (3226 Classes) |
|Cuis 2.0 (644 Classes) |Squeak 4.4 (2511 Classes) |Pharo 3.0 (4020 Classes) |
|Cuis 3.0 (647 Classes) |Squeak 4.5 (2175 Classes) |Pharo 4.0 (4924 Classes) |
|Cuis 4.1 (655 Classes) |Squeak 5.0 (2244 Classes) |Pharo 5.0 (6170 Classes) |
|Cuis 4.2 (501 Classes) |Squeak 5.2 (2713 Classes) |Pharo 6.0 (6388 Classes) |
|Cuis 5.0 (480 Classes) |Squeak 5.3 (2737 Classes) |Pharo 7.0 (7867 Classes) |
|Cuis 6.0 (579 Classes) |Squeak 6.0 (2832 Classes) |Pharo 8.0 (9084 Classes) |
|Cuis 6.2 (680 Classes) | |Pharo 9.0 (10670 Classes) |
|Cuis 7.0 (675 Classes) | |Pharo 10.0 (9690 Classes) |
| | |Pharo 11.0 (9986 Classes) |



We are working hard to keep Cuis small and easy to learn, even as more capabilities are added.

![Cuis Lifts Above its Weight](CuisLiftsAboveItsWeight.png)

This project is all about learning Cuis and sharing Cuis code which others may find of interest.

# Beginners: 

***Get Cuis*** from https://github.com/Cuis-Smalltalk/Cuis-Smalltalk-Dev

Take a look at ***Quick-UI-Tour*** (click on file 'Quick-UI-Tour.md' above or)
- https://github.com/Cuis-Smalltalk/Learning-Cuis/blob/master/Quick-UI-Tour.md

Read ***TheCuisBook*** !!
- https://cuis-smalltalk.github.io/TheCuisBook/

Take a look at how ***LayoutMorphs*** are used to maintain visual relations between graphic elements:
- https://github.com/Cuis-Smalltalk/Learning-Cuis/blob/master/LayoutTour.md

Look at the ***Terse Guide*** (World Menu -> Help -> Terse Guide to Cuis)

Look at ***documentation*** available for other wonderful Smalltalk implementations
- http://squeak.org/documentation/
- http://stephane.ducasse.free.fr/FreeBooks.html

Take a ***detailed tour*** which creates a Package and a GitHub repository for it
- https://github.com/Cuis-Smalltalk/Learning-Cuis/blob/master/SamplePackage1.md

***Subscribe*** and ask questions at the ***Cuis developers email*** list
- https://lists.cuis.st/mailman/listinfo/cuis-dev
- cuis-dev@lists.cuis.st

Software 'code' is meant to be read as well as written.  Well written software is something we all work on getting better at.  There are some cool Cuis packages on GitHib.

Look at the ***repositories in GitHub*** with names starting 'Cuis-Smalltalk'.  Many of these have a 'RoughGuide.md' file which points out code topics and techniques of interest.

View videos on the Cuis Smalltalk YouTube Channel
- https://www.youtube.com/playlist?list=PLbevs6Mp0MMMaR5gSYzJQXQ56OplFSCJk

Look at the ***package reference***
- https://github.com/Cuis-Smalltalk/Learning-Cuis/blob/master/PackageRef.md

Examples of Cuis Smalltalk with interesting Features are described in 'PackageRef.md' including:

* Morphic-ColorEditor
* ClassCommentBrowser
* Crypto-NaCl
* Interlingua-English-Lookup
* Morphic-Misc1
* ... -NamedColors
* Code-Patterns
* Ropes
* Morphic-Games-Solitaire
* Life
* Construction


I find it best to "git clone" repositories in a common directory, in my case named 'Cuis-Smalltalk'.

You can get the standard repositories using a script in 'Cuis-Smalltalk-Dev'.

This is how it looks using Linux.

````
mkdir Cuis-Smalltalk
cd Cuis-Smalltalk
git clone https://github.com/Cuis-Smalltalk/Cuis-Smalltalk-Dev
Cuis-Smalltalk-Dev/clonePackageRepos.sh
cd Cuis-Smalltalk-Dev
squeak Cuis<version>.image "squeak is name of OpenSmalltalk VM"
````
Ask for a feature in a workspace
````Smalltalk
  Feature require: #'Morphic-ColorEditor'.
````
Select the code and "do-it" (cmd-d).

If all went well, you should be able to open a ColorEditor via the World Menu -> New morph.. -> ColorEditor -> ColorEditorPanel

To keep repositories up to date, periodically:
````
cd Cuis-Smalltalk/Cuis-Smalltalk-Dev
./pullAllRepos.sh
````

***Enjoy!***




# Contributors:

The basic goals here are to develop a strategy which is
- Easy to contribute to
- Orienting and useful to people learning Cuis/Smalltalk
- Simple enough that we will bother to maintain it and not step (often) on each others feet.

The gist is that we, the Cuis community, maintain an overview/README.md page, then just add our own mature/example projects to the list of interesting repositories.

Each Project should supply a 'RoughGuide.md', which describes what the interesting bits of code are, as well as the Project 'README.md' which should
- Name the project/feature(s) -- what is this good for, what does it do?
- List the latest Cuis version+revision the code was tested with.
- Show the Smalltalk code to load the package(s).
- Have useful code/usage examples.
- Optionally, show a screen graphic (what does this look like?)

All project repositories should be named with prefix 'Cuis-Smalltalk-'.

For an example. look at the Cuis-Smalltalk-ColorEditor repository.

ToDo:

-  Using the Styled Text Editor, we start and maintain a Rough Guide to Cuis (Cuis-by-Example).  After the general Smalltalk and Cuis overviews, we can write about parts of the system, patterns of how to get things done, and use forked project examples.

I suspect it would not be too much work to embed Smalltalk WorkSheets (TerseGuide WorkSpaces) as objects in STE, which would allow us to have nice live examples.  Projects could contribute chapters.

Open a FileList after loading STE, select MorphBecomeButton.object and click on button "openSTE" to see some interesting code.

Enjoy!
