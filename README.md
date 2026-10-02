# Creating a Continuously Zonated ChipShop LAMPS device

# Introduction

Current the LAMPS model in the ChipShop device is run at either Zone 1 or Zone 3 using two flow rates (15 uL/hr and 5 uL/hr respectively) to investigated questions related to zonation. There is a desire to create a continuously zonated device similar to the vLAMPS (Micronit device) but with a microfluidic ChipShop device.

Currently, we use the 7-Chamber Reaction Chamber device for our single zone chips, the concept device would be the 4-Chamber long channel device below:

### [Device 560](https://www.microfluidic-chipshop.com/channel-chips/54-1897-straight-channel-chip-350-m-channel-depth-fluidic-560.html#/5-material-ps/12-surface_treatment-none)
<img src="https://www.microfluidic-chipshop.com/188-large_default/straight-channel-chip-350-m-channel-depth-fluidic-560.jpg" width="300">

First principles dictate that we should create a Fluid Finite Elements Model (FEM) of Oxygen in the device with the cells (namely, the Hepatocytes). To do so, open source python packages will be utilized to create the channel mesh and physical subdomains (Cells, Matrix Materials) and peform the FEM analysis. Below, you can find the package lists specific to those ends.

| Package | Use |
|----|----|
|PyVista| Visualization of meshes and simulations|
|Gmsh| Creating Meshes and subdomains |
|fenics-ffcx| solving FEMs |

