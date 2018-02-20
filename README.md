# my ppas
    for APT in `find /etc/apt/ -name \*.list`; do
         grep -o "^deb http://ppa.launchpad.net/[a-z0-9\-]\+/[a-z0-9\-]\+" $APT | while read ENTRY ; do
             USER=`echo $ENTRY | cut -d/ -f4`
             PPA=`echo $ENTRY | cut -d/ -f5`
             echo sudo apt-add-repository ppa:$USER/$PPA
         done
     done

sudo apt-add-repository ppa:openrazer/stable    
sudo apt-add-repository ppa:webupd8team/terminix    
sudo apt-add-repository ppa:polychromatic/stable    
sudo apt-add-repository ppa:webupd8team/atom    
sudo apt-add-repository ppa:rael-gc/scudcloud    

sudo apt update


# Stuff needed for work
i3    
meld    
atom    
terminator    
tilix    
vim    
thunar    


# light -- laptop backlight controls
    git clone https://github.com/haikarainen/light.git
    cd light
    sudo make
    sudo make install

# extras for life
nfs-common     
ffmpeg     
openrazer-meta     
polychromatic     
scudcloud     
