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

### Manual invocation ###

You can trigger Github to process the repository without committing,
pushing or merging changes. For this just go to the Actions tab.
On the left side choose the `Build` workflow. In the table showing
the workflow runs the first line allows you to run the workflow.
Click the dropdown button and you can choose the branch to be
processed and finally trigger it.

## Results

When processed successfully, expect results to show up here:
  - The OoliteExpansionIndex, downloadable from the Releases page
  - The OoliteExpansionIndex, directly browsable at
    https://ooliteproject.github.io/oolite-expansion-catalog/
  - The expansion manager's catalog published at
    https://github.com/OoliteProject/oolite-web/blob/only-media/api/1.0/overview/index.html
    This is where Oolite or OoliteStarter grab the information from.
  - The catalog published at
    https://github.com/OoliteProject/oolite-web/blob/only-media/data/oxp.json
    This is where the website takes data to render the latest expansion release table.

