Headers:
# This is a header 1
## This is a header 2
### This is a header 3
#### This is a header 4
##### This is a header 5
###### This is a header 6

Image:

![The character Harry Tuttle portrayed by actor Robert De Niro in the 1985 film Brazil](https://github.com/wsearcySC/skills-communicate-using-markdown/assets/119954632/8a94c909-615c-49b2-818e-5daebcb6a03a)

Code:
``` bash
#Output the SMART data, taking into account the type of drive
echo 'SMART Data:'
if [[ "$drive_type" == "sas" ]]; then
    ssh $backplane_ip "smartctl -a /dev/scale/slot$slot_num | grep -e Product -e Capacity -e Serial -e Current -e hours"
elif [[ "$drive_type" == "ssd" ]]; then
    ssh $backplane_ip "smartctl -a /dev/scale/slot$slot_num | grep -e Model -e Capacity -e Serial -e Cels -e Hours"
else
    echo "Unsupported drive type"
    exit 0
fi
```
