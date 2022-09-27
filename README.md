# Creating the Index Map

<details open>
  <summary><b>What You'll Need:</b></summary>
<ol>
<li>Index map</li>
<li>DRS Report for the index map</li>
<li>ArcMap</li>  
<li>'HarvardMapCollection' Sharepoint Access</li>    
<li>Python IDE (or any text editor)</li>     
</ol>
</details>

### Step One:
**Georeference the index map in ArcMap**
### Step Two:
**Once your image has been georeferenced, digitize the polygons for the index map.** Create one shapefile containing multiple polygons.
### Step Three:
**Run the python codes which will create and populate the attribute table fields.** These can be found in the [HarvardMapCollection sharepoint](https://hu.sharepoint.com/sites/HarvardMapCollection)
- Go to Documents > IndexMapProject and download 1) *addGeosonFields.py* and 2) *populateAeonfield.py*
- Open *addGeosonFields.py* in your IDE or text editor of choice. Change the variables as needed and run the script.
- Next open, edit, and run *populateAeonfield.py*
### Step Four:
Manually fill in values for the rest of the fields
### Step Five:
Convert from Shapefile to GeoJSON in Arcmap

