# all-app-in-docker

As devleoper, we need install many developing tools in local machine.
Install all tools is ok, but if you want to share your tools, then it is hard, because you need take care about what version you should use, Is there any other denpendency for your tools? Dose this compatible with your OS version?

The most important thing is I don't want tools put many dotfiles in my home path...
Even I just uninstall some tools, they still put \*shift in my home path

So I decide using docker to isolate all of them, but of course, I don't want it block my daily develop work.

# How to use

running auto/install_zsh, them it will copy all bin file to your home folder, and adding bin file to your system path.
