# Creating the Index Map

<details open>
  <summary><b>What You'll Need:</b></summary>
<ol>
<li>Index map</li>
<li>DRS Report for the index map</li>
<li>ArcMap</li>  
<li>*HarvardMapCollection* Sharepoint Access</li>    
<li>Python IDE (or any text editor)</li>     
</ol>
</details>

### Step One:
**Georeference the index map in ArcMap**
### Step Two:
**Once your image has been georeferenced, digitize the polygons for the index map.** Each index map will be one polygon, and every polygon will be stored in one single shapefile.
### Step Three:
**Run the python codes which will create and populate the attribute table fields.** These can be found in the [HarvardMapCollection sharepoint](https://hu.sharepoint.com/sites/HarvardMapCollection)
- Go to Documents > IndexMapProject and download 1) *addGeosonFields.py* and 2) *populateAeonfield.py*
- Open *addGeosonFields.py* in your IDE or text editor of choice. Change the variables as needed and run the script.
- Next open, edit, and run *populateAeonfield.py*
### Step Four:
**Manually fill in values for the rest of the fields**

- `label:` (string) Alphanumeric code identifying the sheet or frame. This is usually a handwritten number which is found on the bottom of the scanned map image.
  - e.g. "L-16"

- `title:` (string) title of the sheet or frame. If not found on the scanned map image, check the Hollis metadata, in the *Contents* section.
  - e.g. "Santiago" 

- `Available:` (true/false) Indicates if we have the index map in our collection

- `Download:` (none)

- `iiifURL:` (the URN, appended by '?buttons=y') This creates the link to the IIIF image viewer
  - e.g. "http://nrs.harvard.edu/URN-3:FHCL:102285046?buttons=y"

- `thumbURL:` (the URN, appended by '?width=200') This creates the thumbnail for the index map
  - e.g. "http://nrs.harvard.edu/URN-3:FHCL:102285046?width=200"

### Step Five:
Convert from Shapefile to GeoJSON in Arcmap

