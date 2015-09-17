**Don't use this. Use https://github.com/Scuilion/gradle-syntastic-plugin - it's better.**

# Gradle vim-syntastic plugin
a gradle plugin to generate the classpath file and config variables for getting
Syntastic.vim to work with a gradle build.

Obviously this plugin depends on the 'syntastic' vim plugin.
 
## Installing (build.gradle)
Add contents of vim.gradle to your build.gradle:

    apply plugin: 'java'
    apply plugin: 'maven'
     
    repositories {
         mavenCentral()
    }
    (...)
    task vimFiles << {
        (...)

## Installing (vim.gradle)
Just add the `vim.gradle` to the project root.

# Installing - Adding support on VIM
The easiest way to do this is to add the following lines to the end of your .vimrc:
 
     if filereadable(glob('./.vimrc.local'))
         so ./.vimrc.local
     endif
     
## Usage (build.gradle)
For installing stuff just run:

    gradle vimFiles

Then you will be ready to go! The `.syntastic-classpath` and `.vimrc.local` will be generated on the project root.

## Usage (build.gradle)
For installing stuff just run:

    gradle -b vim.gradle vimFiles

Then you will be ready to go! The `.syntastic-classpath` and `.vimrc.local` will be generated on the project root.

 
 

