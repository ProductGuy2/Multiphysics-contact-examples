# Multiphysics Contact Modeling - Bolt pretension and Gasket modeling
![Multiphysics contact gasket bolts](https://user-images.githubusercontent.com/130690758/232110981-1237fcf9-a71b-435b-b71d-9e8682ef20ec.png)

This example consists of the cylinder head cover and a small portion of the lower part of the cylinder head (see above). Both the cover and the lower part are made of steel. A thin gasket layer seals the joint between the cover and the lower part. The joint is fastened by two steel bolts. The assembly is loaded in six stages. In the first two stages, the fastening of the joint is simulated by applying a pretension of 12 kN to each of the bolts. After the bolts have been loaded, the three-stage thermal/structural loading cycle starts. First, the base of the assembly is heated to 200°C, while an interior pressure of 1.2 MPa is simultaneously applied to the cover and the lower part of the assembly. Next, the base is cooled down to -20°C, while retaining the interior pressure. In the fifth stage, the pressure is removed and the temperature of the base is increased again to room temperature of 20°C. The final loadcase of the analysis consists of disassembling the joint by loosening the bolts. 

# Multiphysics Pin to Seal Contact with Various Friction Models
![Multiphysics contact pin seal](https://user-images.githubusercontent.com/130690758/232475669-cc566a33-54cd-4fc5-b161-91eb4af02deb.png)

The example described  demonstrates various friction models of a rigid pin being inserted into and extracted from a rubber seal. 
The frictionless case, as expected, has the lowest insertion and extraction force whose peak value is around 20 N. Adding friction dramatically increases the peak insertion force to about 95 N, and the extraction force minimum peak is about -135 N. All three friction models produce nearly the same force history as long as the sliding velocity of the Arc Tangent type is properly set. The proper sliding velocity for this case is determined by the velocity of the pin during the insertion which gives a value of 0.020 cm/sec. Note what happens when the default sliding velocity is used, the effectiveness of the friction is dramatically diminished, and is incorrect. 
Comparing run times of various friction methods, the frictionless case requires the least amount of run time, followed by the Arctangent, then Bilinear, and the Stick-Slip model last. As designed, the Bilinear takes a bit more times but has the benefit of realistic default parameters that do not underestimate the friction forces like the Arctangent friction model. 
As an alternative, one can perform this analysis with the segment-to-segment friction approach. This method is advantageous in that it does a better job for self-contact that occurs in this model. This is activated using the Jobs Contact Control menu shown below. The resultant contact status is also shown. 

# Multiphysics Local Adaptive Meshing
![Multiphysic mesh adaptivity](https://user-images.githubusercontent.com/130690758/232479217-b1b8507d-2074-4d0c-a669-07eb014cda34.png)

In this example, a metal tube will be bent ninety degrees around a mandrel as shown in Figures 3 to 6. The local adaptivity criterion is based upon relative equivalent plastic strain with a threshold value of 0.75 and two levels of subdivision. 
The simulation uses symmetry and only half of the tube is modeled. Poisson's ratio is 0.3; Young's modulus is 30,000,000 MPa with initial yield of 50 MPa with work hardening. 
