# Gradle vim-syntastic plugin
a gradle plugin to generate the classpath file and config variables for getting
Syntastic.vim to work with a gradle build.

Obviously this plugin depends on the 'syntastic' vim plugin.

## Usage
apply the plugin file and then run the `vimFiles` task to generate the required
files. To ensure that syntastic is correctly configured you will also need to source
.vimrc.local

The easiest way to do this is to add the following lines to the end of your .vimrc:

    if filereadable(glob('./.vimrc.local'))
        so ./.vimrc.local
    endif


