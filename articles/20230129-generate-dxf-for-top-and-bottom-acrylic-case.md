# How to generate dxf file for top and bottom acrylic case
Author: Sanket Sonavane    
Publish Date: 2023-01-29    
Last Updated: 2023-01-29  

## online tools
- dxf viewer 
    - [GroupDocs Apps](https://products.groupdocs.app/viewer/total)
    - [ShareCad](https://sharecad.org/viewer#0a7995d0-074d-4ff6-8dc1-8e200449112e16030-ext)
- gerber viewer 
    - [Online Gerber Viewer - PCBWay](https://www.pcbway.com/project/OnlineGerberViewer.html)

## apps used
- KiCAD 6 [KiCad EDA - Schematic Capture & PCB Design Software](https://www.kicad.org/)
- FreeCAD [FreeCAD: Your own 3D parametric modeler](https://www.freecadweb.org/)

## What I wanted to do
So I wanted to generate an acrylic top and bottom plate for a split mechanical keyboard. Normally a lot the popular open source split keyboards have there gerbers and kicad files uploaded to the github repo and those files help you print your pcb. but I wanted to create a acryclic case and for that you need to give your acryclic laser cutter service provider a dxf file. So how do I generate this dxf file from provided kicad pro.

## Approach
when you open the kicad .pro file in kicad for the top plate they both seem to have Edge.Cut (border) and F.Mask (plate holes) Layer so you use kicad to plot these files to individual dxf files and now once you have these individual dxfs you need to merge both these to make a single dxf file. This merging can be done in FreeCad.

So now that you have two dxf files , open one dxf in freecad and import another dxf in that same opened dxf file. now information of both dxf is present in a sigle document. now you select all layers and export this dxf in FreeCAD and thats how you now have a single dxf file.

repeat the same for bottom plate and give these files to your laser acrylic service and you have your top and bottom plate with plate holes.

EDIT:
Seems like F.Mask might generate larger holes than needed so I have decided to just print the Edge.Cut DXF file and manually drill the holes with a drill machine.

## Further notes
While this merging of multiple dxf into a single dxf should be part of KiCAD but its still not there in it, I am a beginner with KiCAD and atleast I could not find this so thankfully FreeCAD was there to rescue.