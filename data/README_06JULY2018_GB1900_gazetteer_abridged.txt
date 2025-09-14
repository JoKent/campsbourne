README FILE

GB1900 GAZETTEER ABRIDGED 

Contained within this zip archive are three files:

1) gb1900_gazetteer_abridged_july_2018.csv

This is the main data file as further described below. It is identical to the complete version of the gazetteer except that the number of rows has been reduced by removing common non-place-names, as further described at the end of this document. It therefore contains 1,174,449 text strings transcribed from the Ordnance Survey second edition County Series six inch-to-one mile maps, plus a header row listing the column names.

2) CC_BY_SA_LICENCE_GB1900_gazetteer_abridged.txt

Creative Commons Attribution Share-Alike Licence applying to these data.

8) README_06JULY2018_GB1900_gazetteer_abridged.txt

The file you are reading now.

# LICENCE

Released under a CC-BY-SA Licence, see separate text file for details.


# CITATION

Please reference this work as the "GB1900 Gazetteer (Abridged)" made available by the GB1900 Project. You must acknowledge "the Great Britain Historical GIS Project at the University of Portsmouth, the GB1900 partners and volunteers".

You may call any work you derive from this dataset whatever you like EXCEPT that you must not name your work "the GB1900 Gazetteer (Abridged)", or any other name including "GB1900" or "Great Britain 1900". When using or citing the work, you should not imply endorsement by the GB1900 project or by any of the project partners.

We welcome offers to collaborate on improving future editions of the GB1900 Gazetteer, including additional abridgement. Contact us at gbhgis@port.ac.uk


# PROVIDERS

This dataset is made available via www.VisionofBritain.org.ok which is operated by Great Britain Historical GIS Project, University of Portsmouth, one of the GB1900 project partners. The other GB1900 project partners are the National Library of Scotland, the Royal Commission on the Ancient and Historical Monuments of Wales, the Centre for Advanced Welsh and Celtic Studies at the University of Wales, The National Library of Wales and The People's Collection Wales.


# DATASET DOCUMENTATION

These data derive from the GB1900 crowd-sourcing project, but after the GB1900 web site substantial additional work was carried out, including manual checking and correcting of c. 30,000 points against the historical maps. 

The main data file contains the following columns:

(1) pin_ID

Alphanumeric identifier used to identify locations within the GB1900 system. This can be used as a primary key to a database table, and serves to link these enhanced data to the raw dump files.

(2) final_text

Agreed transcription of the text on the original maps. Provided that the first two transcriptions made in GB1900 matched, or a third transcription matched one of the other two, this will be that "majority" version. However, c. 1.5% of the data were manually checked and corrected as described below.

(3) nation

"England", "Scotland" or "Wales", depending on location.

(4) local_authority

Name of the modern local authority area containing the pin location. Computed using digital boundaries provided for use with the 2011 census and downloaded from the UK Data Service. Areas off the coast were matched to the nearest local authority.

(5) parish

Name of the modern Civil Parish containing the pin location. These were identified using boundaries downloaded from the UK Data Service on 29th June 2018, and represent English and Welsh parishes as defined for the 1991 census and Scottish parishes as defined in 2001. Areas off the coast have not been matched to parishes, and pin locations falling in "un-parished" areas in England, generally urban, have been given the name "<name of local authority> (Un-parished)".

(6) osgb_east

Ordnance Survey national grid coordinate, expressed as number of meters east of grid origin.

(7) osgb_north

Ordnance Survey national grid coordinate, expressed as number of meters north of grid origin.

(8) latitude

WGS-84 co-ordinate.

(9) longitude

WGS-84 co-ordinate.

(10) notes

Additional details for manually checked entries.


MANUAL CHECKS:

Entries were checked manually under three circumstances:

(1) TRANSCRIPTION NOT CONFIRMED BY WEB SITE: Either no two transcriptions matched, or there were not enough transcriptions. These were the majority of cases checked manually.

(2) ONE BUT ONLY ONE TRANSCRIPTION INCLUDED AN ACCENTED CHARACTER: Many place names in Scotland and Wales included accents, and the GB1900 system was designed to simplify entering them, but they were still sometimes left out. We therefore checked all cases where one volunteer had included an accent even though the "agreed" transcription did not include one.

(3) RAILWAYS AND CANALS: These were often names in two parts, the first identifying the company, the second identifying the "line", "branch" or "loop"; and these were often transcribed separately. All strings ending in line, branch or loop that did not start with a company name were checked, and where necessary merged into a single string of text.

OTHER SPECIAL CASES:

(4) DETACHED PORTIONS: Where a small outlying area of a parish is detached from the main area it is identified by a lower case letter. In some cases these lower case letters exist in isolation as just a letter, a-e. In other cases the letter is accompanied by the name of the parish or parishes the area relates to.

(5) PARTIAL TEXT STRINGS: Where the text string on the map was truncated due to the edge of sheet or printing error on the original map, the volunteers were asked to input exactly what was given on the map. If known the full correct text string was then entered in the notes.


*************************
* THE CLEANING PROCESS: *
*************************


*** Removing Numeric Strings ***

Volunteers were asked not to transcribe certain strings including or relating to numbers for areas, elevation and distances. Where these strings have been transcribed they have been removed from the cleaned dataset.

They include:
# Acres - area
# Surface of water  - area
# B. M. / Bench mark - height
# Yards - distance for shooting range

In addition Where an M. P was followed by a place name and a number for a distance these have been shortened to just be M. P


*** Standardised Text Strings ***

We have standardised a small number of specific text strings. 
With two specific exceptions (noted below) we have not changed the letters or the order of the letters in a string.
These changes concern the standardised use of punctuation, spacing and letter cases.
All the original transcriptions without these changes can be sourced in the full raw dump file.

The changes we made to specific text strings are as follows:

# Full stops have a space inserted immediately after them

# Commas and closing brackets preceded by a space have had that space removed.

# Opening brackets followed by a space have had that space removed.

# Hyphens have had any adjacent spaces removed.

# Where consecutive brackets appear a space has been inserted between them.

# Curly apostrophes have been replaced by straight apostrophes.

# Double spaces have been replaced by a single space.


STANDARDISED ABBREVIATIONS:

Like the text strings, specific abbreviations have been standardised, and here the need for standardisation outweighs, in particular, the exact use of spaces and full stops on the original maps: we treat any such variations as typographic errors. The affected strings should always be standardised as follows:

A. D.
Bapt. Chap.
(B. H.)
B. H. 
Boro.
By.
Bdy.
B. P.
B. Ps 
B. P. W. D.
B. Ps. W. D.
B. R.
B. S.
B. Ss.
B. S. A D
B. S. D. C. P
B. S. W D
B. Ss. W D
Ch.
Chalk Pit
Chap.
Chapel
Chaps.
Church
C. T. 
Div.
F. B.
F. Bs.
F. P.
Ford
Gravel Pit
G. P
G. Ps 
H. & L. W. M. O. T.
H. P. to which O. T. flow
H. W. M. O. T.
H. W. M. O. S. T.
L. B
L. W. M. O. T.
Meth. Chap.
Methodist Chapel
M. P
M. S.
Mort. Chap.
Old Chalk Pit
Old Chalk Pits
Old Gravel Pit
Old Gravel Pits
Old Marl Pit
Old Marl Pits
Old Quarries
Old Quarry
Old Shaft
P. H.
(P. H.)
Parly.
Parly. Co. Div. Union & R. D. By.
Parly. Co. Div. & U. D. By.
Parly. Co. Div. Union & U. D. By.
PL.
P. O.
P
Ps
Quarries
Quarry
R. D. By.
S. B.
Sch.
Schs.
S. P.
S. Ps.
Smy.
School
Spring
Sun. Sch.
U. D. By.
Union & R. D. By.
Union & U. D. By.
W
Ws
Weir

N.B. The two abbreviations where we have changed the perceived order are both for boundary markers:
'WD B.Ps' has been altered to 'B. Ps. W. D.'
'W D B.Ss' has been altered to 'B. Ss. W D'

In both cases the detail of the map and the placement of the text meant it was difficult to identify 
if the War Department letters should go before or after the Boundary posts/stones. In this instance 
we felt it made more sense to make these text strings in line with the others.

****************
* ABRIDGEMENT: *
****************

The frequency of each unique string in the complete gazetteer was counted, and all strings with a frequency of 300 or more were excluded with the following exceptions, which were manually assessed as being sometimes or always "place names". This is of course a subjective decision, and note that the commonest of these terms, "Manor House", appears in the data set 1,617 times:

Back Lane
Church Farm
Church Lane
Currick
Fox Covert
Glebe Farm
Green Lane
Hall Farm
HIGH STREET
Hill Farm
Hill House
Home Farm
Lodge Farm
Long Plantation
Manor House
Manor Farm
Mill Lane
Mount Pleasant
New House
New Inn
New Road
Park Farm
Rose Cottage
The Cottage
The Elms
The Grove
The Mount
The Rookery
Ty-newydd
White Hill
White House
Woodside
Woodlands


Paula Aucott
Humphrey Southall
July 2018
