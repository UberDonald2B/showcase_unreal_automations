# showcase-unreal-automations

This is a public showcase for python scripts still in development I've been working on to streamline the transfer of assets into Unreal.

## Usage
As scripts are being developed, how to use these tools along with any additional information will be posted here.  

The install instructions to setup Unreal and Visual Studio Code to work together to develop Unreal automations using the Unreal Engine Python API. Using a more robust code editor with autocomplete and debugging functionality will make the process of code review and collaboration much each for the entire software engineering team.

## Install Instructions
[Setup documentation](SETUP.md)

### In Development
![Picture of fallout guy](images/fallout_guy.jpg)


# Script Demos

## Texture Import / Shader Setup Automation Script
DEVELOPMENT - Python script automating the import of PBR textures into Unreal, then creating a material instance based on the textures type. In this case, these textures are all Opaque shaders. Once the material instance is created, the associated settings are then changed based on a config.yaml file. Once the script is completely run, all textures and shaders are neatly organized into folders.  

**DEMO:** https://player.vimeo.com/video/932251936?h=2a14229b2e

## FBX Import / Blueprint Setup Automation Script
DEVELOPMENT - Python script to automate importing an FBX asset with custom settings based upon pre-established production pipeline guidelines. Create a blueprint, with a custom parent class with custom settings based on the asset imported. Then materials are properly assigned, saved, and then compiled.  
  
This is still early in development, but already functional for many of my projects. I plan to continue to expand and develop this tool to accept more complicated asset configurations in the near future.

**DEMO:** https://player.vimeo.com/video/932251911?h=6325c8fe30