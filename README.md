# oolite-expansion-catalog

This repository hosts a list of expansion URLs.
From this list the expansion catalog is built regularly.

## File format

The file expansionUrls.txt hosts the list of known expansions.

 The rules are:
 - Have one URL per line
 - Lines starting with hash are considered comments and ignored
 - Empty lines (zero length or just whitespace) are ignored
 - it is recommended to sort the URLs to easily spot duplicated.
   Check the generator's pedantic mode.


## Processing

Whenever changes are pushed into the repository, or regularly 
once a month or even on manual invocation the build process is 
triggered. 

For that HiranChaudhuri/OoliteAddonScanner is invoked to read 
the expansionUrls.txt file, download the expansions, read their 
metadata and assemble that into a new expansions catalog.

This catalog is then pushed both in plist and json format into 
the website on the only-media branch in OoliteProject/oolite-web.
