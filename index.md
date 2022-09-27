# Creating Index Maps

<details open>
  <summary><b>What You'll Need:</b></summary>
<ol>
<li>Index maps</li>
<li>ArcMap</li>  
  <li><i>HarvardMapCollection</i> Sharepoint Access</li>    
<li>Python IDE (or any text editor)</li>     
</ol>
</details>

### Step One:
**Georeference the parent map in ArcMap.** This is the map which contains all the smaller, index maps. Make sure the apporpriate coordinate system is selected while doing this (WGS 1984 is fine).
### Step Two:
**Once your image has been georeferenced, use map to digitize the index map polygons.** Each index map will be one polygon, and every polygon will be stored in one single shapefile. 
> **Note:** *Some polygons will not have an index map linked to it, but all index maps will link to exactly one polygon.*
### Step Three:
**Run the python code which will create and populate the attribute table fields.** These can be found in the [HarvardMapCollection sharepoint](https://hu.sharepoint.com/sites/HarvardMapCollection)
- Go to Documents > IndexMapProject and download 1) *addGeosonFields.py* and 2) *populateAeonfield.py*
- Open *addGeosonFields.py* in your IDE or text editor of choice. Change the variables as needed and run the script.

### Step Four:
**Manually fill in values for the rest of the fields**

- `label:` (string) Alphanumeric code identifying the sheet or frame. This is usually a handwritten number which is found on the bottom of the scanned map image.
  - e.g. Sheet 2 out of 8 would be labeled "2"

- `title:` (string) title of the sheet or frame. If not found on the scanned map image, check the Hollis metadata, in the *Contents* section.
  - e.g. "Santiago" 

- `available:` (Boolean: true/false) Indicates if we have the index map in our collection

- `download:` (none)

- `iiifURL:` (string) (the URN, appended by `?buttons=y`. This creates the link to the IIIF image viewer.
  - e.g. "http://nrs.harvard.edu/URN-3:FHCL:102285046?buttons=y"

- `thumbURL:` (string) the URN, appended by `?width=200`. This creates the thumbnail for the index map.
  - e.g. "http://nrs.harvard.edu/URN-3:FHCL:102285046?width=200"

### Step Five:
**Next open *populateAeonfield.py* in your IDE or text editor**. Edit the variables listed at the top of the script and then run it.

### Done!

