# TheCADExperience
CAD Documentation and learning how to do some simple CAD
Stage 0: Shortcuts I have

## Getting the DAT Files for XFLR5/FLOW5:
- Find desired airfoils on airfoil tools and under Details click on the "Source dat file" and make sure it is in Selig format

<img width="1278" height="867" alt="image" src="https://github.com/user-attachments/assets/f1da0175-180d-41d4-840f-50b0be870bbe" />
- If not, you should be able to select the Selig forma DAT file on the right hand side
- Next, Copy everything but the name and paste it into excel/sheets

<img width="1176" height="753" alt="image" src="https://github.com/user-attachments/assets/c3e6b8c8-15a2-4cbb-9043-e077506b3d3f" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/15e16865-a952-4157-8252-399582f656a2" />
- Now, Select the Data menu bar, and with the column of values selected, click on "Text to Columns", Follow the wizard until your data is seperated into two columns
- 
<img width="755" height="539" alt="image" src="https://github.com/user-attachments/assets/28857389-b9bf-42c9-8d97-ab3c2f6cb5bf" />
<img width="755" height="539" alt="image" src="https://github.com/user-attachments/assets/ae07556f-aed4-4624-8fc5-fb37cfa38451" />
<img width="755" height="539" alt="image" src="https://github.com/user-attachments/assets/766e6089-c2f2-4de7-b75e-64f63c18f968" />
- It should look like this:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ed4f6ea3-0566-4a25-a1bd-34720c341d8b" />
- Now you can organize your columns into an x, y, and z, axis respectively by adding a column of 0s to the right of your two existing columns.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5fba1a71-5da4-4416-8709-bd047ece3d4d" />
- Save as -> "Text (Tab delimited) (*.txt)"

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2211e475-7f8e-424a-8452-481400f35d09" />
- Once saved as a .txt, rename the files to end with .dat so XFLR5/FLOW5 can use them. Note that windows may prompt you asking if you're sure since this changes the file format. Additionally, it may not let you while the excel/sheet application is still open.

<img width="796" height="118" alt="image" src="https://github.com/user-attachments/assets/6c770463-5214-4950-9675-dd667a5cae54" />

## XFLR5/FLOW5 
(I will be learning how to use FLOW5) ALSO NOTE. AT TIME OF WRITING THIS FLOW 5 IS STILL CLOSED SOURCE SO THERE ISN'T THE NECESSARY GPL LISENCING TO  RUN 2D ANALYSES NATIVLY SO THIS IS STILL NEEDED TO BE DONE IN XFLR5 FOR NOW.
- In FLOW5, press **CTRL+SHFT+F** to load desired .dat files into a project space.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0d4d07d2-9907-41ad-996d-a2896f442ac7" />
- Next, press **CTRL+5** to enter Foil Design.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/97112937-175c-4f2b-b5ea-d575a2e12397" />
- Click on "Switch to the foil design view" to fully view each airfoil and edit the styles of each airfoil however you like for easier identification.
- I also recommend making the camber line, and airfoil spline nodes visible for better visualization.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dad705b1-3eca-4403-ade9-404e801e373d" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/44b05203-67ce-4114-8918-7418bdc8cb02" />

*** NOTE TO SELF THESE IS A NEAT INTERPOLATE FOIL TOOL THAT LETS YOU INTERPOLATE BETWEEN AIRFOILS WHHICH MIGHT BE REALLY USEFUL FOR BLENDED WINGS/TRANSITION REGIONS ***
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ce8c7a39-23c1-4413-9b01-856a01be1b51" />

- Next we want to refine our airfoils so they are smoother, like my brain. So after selecting the desired airfoil, **press F9**, or R_Click the airfoil>Modify>Refine Globally, increase the number of panels to somewhere in the range of 150-300. Too many will make your computer toasty and may prevent convergence. I did 200.

<img width="1283" height="758" alt="image" src="https://github.com/user-attachments/assets/b3d1edac-0436-4b92-ad70-19b38678968e" /> <img width="1283" height="758" alt="image" src="https://github.com/user-attachments/assets/b533bf4a-b575-4b02-9186-44c03eb01258" />
- The bunched vs uniform can help you run more efficient analyses by focusing spline nodes where it matters but I just left it as uniform since I'll be using these .dat files for CAD too
- I choose not to overwrite the old .dat files and save as new ones. This allows me to rename the airfoil to something shorted than my directory location as well as keeping the old .dat file in case I need to redo any analyses/want to do anything using the original .dat file.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6bedb39c-212c-40c1-aa8e-a2e86e3f6f1e" />

## 2D Analysis
This only needs to be done once per analysis and must be done before 3D analysis.
SIKE This needs to be done in XFLR5 still then results need to be ported into FLOW5...
Here's how to do that:
- ... jk I gave up and skipped to CAD stuffs 
- Press **F7** or navigate from the top menu bar and select Analysis>Batch analysis to start a batch analysis

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8a6c615c-c31d-45e7-9334-be1c5a40edb4" />
<img width="1283" height="758" alt="image" src="https://github.com/user-attachments/assets/2974a930-96cf-4f3f-9916-77a06db2ab6e" />
- From here 


SIKE THIS IS DONE ONCE AFTER 2D BATCH ANALYSIS TO SET UP FOR 3D ANALYSIS!! 
- Press F6 to define an analysis or go to the top menu bar and select Analysis>Define an analysis.
- De-select Default Name and name it something recognizeable, like "Jun12_S1223_01" or whatever the naming convention you choose to follow.
- Select Analysis **type 1** [^1]
[^1]: type one produces a fixed speed polar which is all wee need for the 3d analysis later on. This type scans lift, drag, and moment over a range of AOAs at a fixed freestream velocity which is what we assume our plane will fly at. We might want to look at using other analyses like type 3 for speed polars and the like in the future.
- Ncrit should be decreased the more irregular a surface is. I understand it as being "the more difficult it is for air to stick, the lower the ncrit". so rough with flaps/control surfs. 7-10, very smooth, 11-14, very rough (fully deflected control surface) 5-8.







  


Stage :
Dimensions and Basic Specs:
Get Rib Spacing, Tapers, Sweep and Twist from Analysis

