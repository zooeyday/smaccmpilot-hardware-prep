# SMACCMPilot Platform Prep

This repository contains a set of utility programs required to transform an
ordinary Pixhawk-based flight platform, such as the Iris or Iris+ quadcopters
sold by 3D Robotics, into a SMACCMPilot compatible platform.


## Step 0: Flashing the PX4 project Bootloader

If you haven't ever used JTAG or don't even know what that means, skip this
step.

If you have used a JTAG interface to flash programs to the Pixhawk's FMU
processor, you probably need to reflash the USB bootloader on the FMU processor.
Follow the instructions in `fmu_bootloader/` on how to perform this step.

## Step 1: Flash the APM firmware to the FMU

We need to load a version of the APM project's firmware onto the FMU processor
in order to perform an upgrade of the firmware on the IO coprocessor.

Follow the steps in `fmu_apm_firmware/` to load the included APM project
firmware image onto the FMU.

## Step 2: Upgrade the IO coprocessor firmware

A new firmware image for the px4io IO coprocessor is provided in the `sdcard`
directory. It must be copied onto a Micro SD card. Follow the instructions in
the `sdcard` directory to complete this operation.

## Step 3: Upgrade each 3DR Radio's firmware

SMACCMPilot uses a upgraded version of the 3DR Radio firmware which fixes
several serious security vulerabilities in the factory firmware, and provides a
more reliable framing mechanism. Follow the instructions provided in the
`smaccm_sik/` directory With each 3DR Radio (or compatible HM-TRP based radio).

## Step 4: RC Transmitter Configuration

TODO.

## Questions

Contact pat@galois.com
