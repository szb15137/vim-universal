vim-universal
=======
A universal VIM integration

 - Written in Python and VimL
 - Extended plugins with pack by submodules
 - Support MacOS and Linux-x86_64

Requirements
------------

 - vim8.2 or higher
 - Python2.7+ or Python3.1+

Install
-----
Please clone it with all submodules
```
git clone https://github.com/shawnvim/vim-universal --recurse-submodules
```
Or you can just download the `release.zip` with all submodules and rename it to `.vim`  
If you want to keep the folder name as vim-universal, you can use `gvim -u PathToVimrc`

Remove submodule
-----
If you have duplicated plugins locally, you can remove submodule by:
```
git submodule deinit project-sub-1
git rm project-sub-1
```
and then remove the related configuration in `vimrc`

Update
-----
If you want to update with all submodules, please use:
```
git submodule foreach git pull origin master
```

Init
-----
After initial install, please install Leaderf fuzzy find engine:
```vim
:LeaderfInstallCExtension
```
And you can check the nstallation status after VIM restart by:
```vim
:echo g:Lf_fuzzyEngine_C
```

Readme / Help
-----
Most of the plug-ins' configuration is in `autoload/setup`, and you can use `gx` to check their Github page, or use `gf` to go to the file directory


Run time path
-----
If you have other rtp or pack directory, you can include it by:
```vim
let g:path_internal = YourOtherRTP
if isdirectory(g:path_internal)
    let &rtp .= ','.g:path_internal
    call YourOtherFunction()
endif
```
