# Grasshopper_Mesh2Mesh_Tiling

15394 Final Project
Shiva Peri

***** Brief *****

For my final project I wanted to make a Grasshopper script to combine meshes via a customizable tiling pattern. I wanted to make this because of the potential creative and artistic applications of being able to permute meshes in this way. 


***** Ideation *****

When I was in 12th grade I made a mesh which called Bubble Rocky. I've included it here for clarity. However, I made this mesh in Fusion360 by manually creating, scaling, and positioning the spheres. I realized that Grasshopper has several ways for manipulating groups of vectors via parameters. The intention of working with vectors is that the direction and length can be mapped to the orientation and scale of the "tile" mesh. However, I was only able to achieve the tiling of a Grasshopper defined cylinder.

Also, the projects Meander (http://roberthodgin.com/project/meander) and Shiv Integer (https://www.plummerfernandez.com/shiv-integer/) were inspiring references.


***** Challenges *****

 - extremely large file sizes
 - understanding the differences between meshes and surfaces
 - making the script reusable
 - I wanted the script to map one user defined mesh on to another in some interesting way
   Instead I was able to only achieve using a Grasshopper defined simple geometry (ie. Cylinder, sphere, etc) as the tiling mesh.


***** Included Files *****

 - Screenshots of the various creations I made with my script
 - STL files I used from thingiverse
 - The STL FunkyVase is a mesh that I made for an old project in high school


***** Excluded Files *****

Because I had extremely large file sizes, I have selected to not include them here. Rather below is a link to a Google drive folder which contains the STL files, Rhino Files, and the actual Grasshopper scripts.

NOTE: Unfortunately the complexity of the geometries I was trying to make forced Rhino to crash. A lot. And I was unable to export the STL or Rhino file for the result of running my script on FunkyVase. I did however include screenshots in this zip file.

Link (https://drive.google.com/drive/folders/1qeCySUGD1fT_c4megKPFY0PMxdnIYyGy?usp=sharing)



***** How the Script works *****

  1. Import an STL as a mesh into Rhino
  2. Select that mesh for the input in Grasshopper
  3. Extract normal vectors from mesh
  4. Define 2 attractor points using user input from sliders
  5. Determine the shortest distance from every normal point to an attractor point
  6. Use this distance as the length of the normal vector
  7. Convert the normal vector to a plane
  8. Create a cylinder and set length and radius according to calculated distance from earlier and preference
  9. Orient a cylinder to each normal plane
 10. Join all meshes
 11. Bake and export


***** Referenced Works *****

STLs from Thingiverse
 - skull (https://www.thingiverse.com/thing:441087)
 - coffee mug (https://www.thingiverse.com/thing:24464)

Grasshopper Tutorials
 - Mesh to Surface (https://youtu.be/scQGLhSBakI)
 - Scale NU (https://youtu.be/zQc86-ujhQ0)
