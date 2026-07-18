# FOIL5 Exploration
### xflrpy:
```pip install xflrpy```
<img width="1344" height="729" alt="image" src="https://github.com/user-attachments/assets/9c554e88-9e88-43c2-ab12-7a556d69ac84" />
<img width="1344" height="729" alt="image" src="https://github.com/user-attachments/assets/8783d057-24c0-4187-8a5e-125534993ab7" />

### Some videos:
[General Airfoil analysis - techwinder](https://www.youtube.com/watch?v=o04HL4vT7kU)
Main takeaways:
- Use bunched when refining airfoil to help with laminar->turbulent transition calculations
- Sets trailing edge flaps. "make deflection permanent" makes the deflected flap it's own airfoil
- Mainly uses define an analysis not batch analysis (?)
- Airfoil ranges with type 1 analysis are 0 to max pos. AOA and another set for 0 to max neg. AOA eg. (0 -> 15) and (0 -> -10)
  - makes xfoil converge better and more often
  - lets re-initialization of BL happen more naturally
- For type 4 analysis, sweeps through Re while AoA is fixed
- Uses Variable Sets Alpha and Re
  - Allows you to see the graphs with specific polars without needing to specify which ones are being shown
- type 6 analysis (flap analysis?)
- Polars and Analysis are the same object. Analysis is the input parameters, and the Polar is the output of said Analysis.
- double click anywhere to center graph view
- press x/y then scroll to zoom in axis
- Touches on batch mode-legacy which is needed to generate viscous data for 3D analysis, does not use new batch analysis for this
  - uses the new batch analysis to do multi-type batch analysis
Did a little test of my own to comfirm suspicions and yes, it is indeed better to have two broken ranges than one long continuous range:

Here we have magenta as thhe single continuous range and the light blue as the broken ranges
<img width="1058" height="963" alt="both_compared" src="https://github.com/user-attachments/assets/60ce5ef2-65fb-4f2b-b8ee-b1c9bf66c5d0" />

  
[Follow Up with 3D of above - techwinder](https://www.youtube.com/watch?v=kuaHycjO-7g)
Main Takeaways:
 - asd

### 3D Inverse design
