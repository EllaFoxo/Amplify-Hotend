# Katapult Setup

Katapult is the bootloader which lets you remotely flash new firmware versions, without requiring access to the physical board.

## Obtaining Katapult

If this is your first time using Katapult, you will need to SSH into your printer to acquire the source:-

```shell
git clone https://github.com/Arksine/katapult.git
```

## Configuration

Once cloned, open the Katapult configuration menu with the following:-

```shell
cd katapult
make menuconfig
```

Configure Katapult so your setup is as follows:-

![Katapult Configuration](/images/katapult-configuration.png)

## Katapult Flashing

Katapult can be loaded onto the board using `dfu-util` command. If you are running MainsailOS
```shell
sudo dfu-util -d 0483:df11 -R -a 0 -s 0x08000000:mass-erase:force:leave -D out/katapult.bin
```

## Done!

You can now press the reset button on your Amplify PCB board.

If all went well, the status LED should now be blinking. You are now ready to install Kalico.
