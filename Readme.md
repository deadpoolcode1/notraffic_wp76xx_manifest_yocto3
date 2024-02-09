##build instructions

mkdir ~/wp76xx_yocto3

cd ~/wp76xx_yocto3

python3 ~/bin/repo init -u ssh://git@github.com/legatoproject/manifest -m mdm9x28/tags/SWI9X07Y_03.01.07.00/linux.xml -g default,-cache,proprietary ; repo sync

git clone git@github.com:deadpoolcode1/notraffic_wp76xx.git -b yocto3 personal_swi

cp personal_swi/modular-tools.sh .

sudo git config --system --add safe.directory '*'

. modular-tools.sh yocto_build
