# OS

## SAMFi-OS_OrangePi_zero

Before you use the [SAMF-OS_OrangePi_zero](https://github.com/FYSETC/FYSETC-SAMFi-OS). You need an TF card with at least 8G capacity. 

### Step 1

Download and flash the OS image with `balenaEtcher` software to your TF card. Insert your flashed TF card to OrangePi-zero and connect Ethernet cable then power on. Find the ip address of OrangePi-zero on your router, host name is `orangepizero`.

![](OrangePi-zero\OrangePi_zero.jpg)

### Step 2

You can find the firmware `klipper.bin` in `OrangePi-zero` folder after you download the github repository. It is also stay in the OS path `firmwares\spider-king407.bin` after you login the OS with SSH.

Original SSH account and password:

```
account: fysetc
password: fysetc123
```

Enter DFU mode(set a jumper on `3.3V` and `BT0` pin on king core board and click the reset button, you need power on the board with 24v ), and flash the firmware with the command below after you connect your OrangePi and Spider-king with USB cable.

```
dfu-util -R -a 0 -s 0x08008000:leave -D firmwares/spider-king407.bin
```

or follow the instructions [here](https://github.com/FYSETC/FYSETC-SPIDER#44--firmware-upload) for firmware uploading. Remember to remove the `3.3v` `BT0` jumper and click the reset button after you flashed the firmware. 

![](OrangePi-zero\spider-king.jpg)

### Step 3:

Prepare the `pinter.cfg`, using the command below

```
cp klipper_config/spider-king.cfg klipper_config/printer.cfg
```

You probably need to change `id` by `ls /dev/serial/by-id` command.

I use the voron2.4 config for this example, you need to change it according to your machine. Now visit the webpage with your orangepi-zero IP address. Good to go.
