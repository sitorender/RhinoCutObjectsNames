# RhinoCutObjectsNames
Rhinoceros cut objects names

script:

import rhinoscriptsyntax as rs   
objList = rs.GetObjects("Select objects to name")  
for singleID in objList:   
   name = rs.ObjectName(singleID)   
   print "name for object is ", name   
   first_chars = name[0:24]   
   rs.ObjectName(singleID, first_chars)   


Run the script (tools>pythonscript>edit)  
copy/paste/selectthecode/play    
select the object to rename   
enter


You can create a button with the code: 
hold ctrl and duplicate a single button on a toolbar  
hold shift and right click on the new button 
delete the current script and replace it with this 

! _-RunPythonScript (   
import rhinoscriptsyntax as rs   
objList = rs.GetObjects("Select objects to name")  
for singleID in objList:   
   name = rs.ObjectName(singleID)   
   print "name for object is ", name   
   first_chars = name[0:2] 
   rs.ObjectName(singleID, first_chars)   
)  

edit the button icon image (in the up right corner)   


You can change the lenght to cut editing this line "first_chars = name[0:24]" e. "first_chars = name[0:12]"    
or create different buttons with different lenght on left and right click



