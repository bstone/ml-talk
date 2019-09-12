# Getting started with Git

## What is `git`?

Today we will discuss the delivery method of all course materials, assignments, and projects. This method will rely on learning `git`. 

- According to [Wikipedia](https://en.wikipedia.org/wiki/Git_(software)), "Git is a version control system that is used for software development and other version control tasks. As a distributed revision control system it is aimed at speed, data integrity, and support for distributed, non-linear workflows." 

------

> - Basically, it is a more sophisticated Dropbox and allows you to keep your code up to date across multiple platforms. 

- A complete walk through of Git can be found online at [`https://git-scm.com/book/en/v2`](https://git-scm.com/book/en/v2). 
- Today we will only learn the basics. 


## Sign up with GitHub

If you don't already have an account, you will need a GitHub account. You can do so here: [https://github.com/](https://github.com/).

- I'll wait here while you do this. ![](./img/cat-waiting.gif)

::: notes

- Once you are finished, go to blackboard and click on the first homework a for Week 01
- This will send me your github info
- I will use this to send an invitation

:::

## 

Once you have accepted your invite, you now have access to the coures materials. The page should look something like this. Feel free to poke around. 

> - [`https://github.com/math-355`](https://github.com/math-355 =50x50)

<img src="./img/organization-landing-page.png" width="600"/>

::: notes

- After everyone is signed up, go to the syllabus page and talk about it.
- Once done come back here for Git stuff. 

:::


## Cloning a Repo

First, what is a repo and why would you want to clone it? __Repo__ is short for repository which is basically a directory of files and folders. Individually you have a GitHub account and you are now members of the GitHub Organization Math-355. All examples, homework, syllabi, resources, etc. will be stored in individual repos in the organization (not your personal account)


------

So now what? All of your desired repos are sitting on some magical server. How do you get your hands on it? 

1. Use the GitHub interface (lame)
    - Downloading this way does not allow for version control
    - This will result in 1990s style backups
2. Use `git` to clone the repo (cool kids do this)
    - `git` will allow for the server and your local machine to communicate
    - This way all local changes can be pushed to the server. 

::: notes

- Stop and talk about these points

:::    


## GitHub Interface {data-background-color="#ff0000"}

We will walk through this method, but working this way will NOT allow you to turn in homework. 

[https://github.com/math-355](https://github.com/math-355)


## Command Line with `git` 

> - If you have a mac or linux, you're done.
- Or you could follow along and get a newer version of `git`.

- If you have Windows OS, then you will need to download and install `git`.
- [https://git-scm.com/download/](https://git-scm.com/download/)
- This should install a program called `git bash`. (I think)

------

## Navigating the command line

Once you have `git` installed, open up `terminal` (mac/linux) or `git bash` (windows).

- `ls` --- gives you a list of items in the directory
- `cd DIRCTORY` --- changes directory to one you can see with `ls`
- `cd ..` --- moves up a directory

::: notes

Try it out!

:::

## Our first clone

It's time to clone a repo. Go to your a first homework assignment and click on the button that says 

`Clone or download`

then copy the link. Then type the following into the command line. 

```
$ git clone COPIEDLINK
$ cd week-01-getting-started-fall-2019-USERNAME
$ ls
```

::: notes

Make sure and mention what the $ is for

:::


<!-- <pre><code class="hljs" data-trim data-line-numbers="4,8-11">
import React, { useState } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  return (
    &lt;div&gt;
      &lt;p&gt;You clicked {count} times&lt;/p&gt;
      &lt;button onClick={() =&gt; setCount(count + 1)}&gt;&lt;button onClick={() =&gt; setCount(count + 1)}&gt;&lt;button onClick={() =&gt; setCount(count + 1)}&gt;
        Click me
      &lt;/button&gt;
    &lt;/div&gt;
  );
}
</code></pre>
 -->

<!-- Well you could use the GitHub interface, but that is lame. So we need to get the files to your local machine. There are several ways to do this, but the cool kids like to clone. __Cloning__ is just copying and pasting the repo to your local machine. To do this we need to get our hands a little dirty with the following steps.

* Open `Git Bash` (or `Git Shell` on some machines) on your machine. This is a command line interface that allows you to communicate with GitHub.
* Once you have `Git Bash` open, type `cd Desktop` and hit enter. This will make sure all downloads are placed on your desktop.
* Look for a green button on this page that says `Clone or download`, click it, and copy the text. It should look something like this: `https://github.com/YOURUSERNAME/Lab01-Intro-to-GitHub-Spring-2018.git`. 
* Go back to Git Bash and enter the following (note, don't enter the `$`, it's just there to tell you that is the start of the line):
```
$ git clone https://github.com/YOURUSERNAME/Lab01-Intro-to-GitHub-Spring-2018.git
```
* Next change directory to the repo by typing:
```
$ cd Lab01-Intro-to-GitHub-Spring-2018
```
* Look into the repo by typing:
```
$ ls
```

You see? All of the files are there! This is great right? Now you have a local copy of the repo sitting on your machine. No matter what you do, you will not mess up the originals. All of your edits/changes will be local on your machine until you push your changes back to the server. So let's do that. -->

## Why should use `Git`?

The main reason right now is because we will be using it to turn in assignments during this class. But besides that it is a very powerful tool that will help future you be successful. Here are a few reasons why git is great:

* Version control, keeps all machines up to date
* Helps keep track of conflicts
* Complete history of your projects
* Easy testing without breaking your code

## How to do your homework (Anaconda)

* Open Anaconda Navigator
  * Launch Jupyter Notebook
  * Navigate to file in homework repo
  * Edit, commit, push

## How to do your homework (Command Line)

Install and run Jupyter Notebook
```
$ python3 -m pip install jupyter --user
$ jupyter notebook
```
* Navigate to file in homework repo
* Edit, commit, push


## Review

Here is a quick overview of `git`. For all future labs, the work-flow will be as follows:

* Clone repo to your local machine 
  - `git clone url/to/repo`
* Navigate to repo (using `cd` and `ls`)
* Add files if needed (`git add filename`)
* Commit any new changes 
  - `git commit -am 'message'`
* Pull new changes from server (`git pull`)
* Push your changes to server (`git push`)





