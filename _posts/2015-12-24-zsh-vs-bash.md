---
layout: post
title: zsh v/s bash
---

Often I have come across many different posts that has developers doing awesome stuff with the help of short scripts they have written in order to automate things / make things easier for themselves. The most interesting one I came across was this post of a Russian developer who had written scripts that could automatically send his wife a message if he was running a bit late or check for a certain keyword in the email from his co-worker among various other things. You can read the whole article here : [__Now that's what I call a Hacker__](https://www.jitbit.com/alexblog/249-now-thats-what-i-call-a-hacker/)

Cool, right? After reading that post I started to read about scripting. Majority of the scripting is done using the shell scripts, some are performed using python and other such scripting languages. The wikipedia definition of a shell script is : _A shell script is a computer program designed to be run by the Unix shell, a command line interpreter. The various dialects of shell scripts are considered to be scripting languages._ Now you need an environment, a __shell__ so to speak, in order to run these scripts. There are many different kinds of shells available : Korn Shell(ksh), Bourne Shell(bsh), C Shell(csh), Bourne Again Shell(bash), Z Shell(zsh) etc. Bourne again shell and Z Shell are the most commonly used shell nowadays. 

Bourne Again Shell(bash) is the shell that is the default one on most systems because of its backward compatibility with _sh_, the only shell present during the earlier times. It was developed as a software replacement to the original Bourne Shell(bsh).

Both bash and zsh are very smiliar to each other and both are extremely powerful in terms of the scripts a user wants to run. However bash was developed to keep portability in mind and thus follows POSIX, which is not followed by zsh that makes it lose out on portability. 

In terms of setting up both the shells from scratch, you can easily notice that bash just starts running whereas zsh takes you through a couple of steps, customizing it according to your needs in order to make it run as you intend it to. This customization and interactive use makes it a bit popular in the community. 

One more difference that I have read about the zsh and bash is that zsh ships with **_programmable autocompletion_**. One can also navigate the completion list and select the completion one wishes to use. Although bash now supports auto-complete via the _bash-completion_ package, this isn't navigable with keyboard and bash and the user has to type in the command themselves. 

There is also the feature of command history in the zsh. Often, one has more than a single terminal running scripts and zsh alllows to scroll from the past written commands across terminals which makes the job a lot easier. ~~Bash lacks this feature.~~ **UPDATE: ** A reader told me that there is a feature by which you can add commands to the _.bashrc_ config file using the command 

`shopt -s histappend                      # append to history, don't overwrite
export PROMPT_COMMAND="history -a; history -c; history -r; $PROMPT_COMMAND"`

More about this can be read here : <http://askubuntu.com/questions/67283/is-it-possible-to-make-writing-to-bash-history-immediate>

It is often said that zsh is faster than bash but that has not been proved yet, atleast for me. 

Bash also lacks in floating-point math, such as this command 
`number=$((3.5 / 4.2))` 
won't work in bash. It doesn't have directory aliases that can shorten the script by a whole lot. Although many of the zsh features can be configured in bash and the fact that bash is available on every device makes it used a whole lot more, there are many zsh features that cannot be configured into bash. 


A few links that talk about both the shells : 

1. <https://www.quora.com/What-is-the-difference-between-bash-and-zsh>
2. <http://ft.bewatermyfriend.org/comp/zshtalk.html>
3. <https://www.reddit.com/r/linux/comments/1csl7c/bash_vs_zsh/>
4. <http://www.slideshare.net/jaguardesignstudio/why-zsh-is-cooler-than-your-shell-16194692>
