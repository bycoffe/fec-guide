The first line in every electronic filing is the "header" row, which contains metadata [1] about the filing.

All the values in the header row are important to someone, but a few in particular are especially important to us:

_The FEC version number_ 
This is the value in the third column of the header row, and it tells us which set of field names and positions to use for each row type. In fact, we can't even parse the header row itself correctly without knowing the FEC version number, because the row's fields changed between versions five and six.

The FEC occasionally updates the version required for new filings [2] and makes available the field definitions for the new version. But older filings that were submitted before the update will remain in the FEC's filing system, and we'll need to parse them based on the version they used.

The version number currently required for electronic filers is 8.

For a list of field definitions, see Appendix A.

_The Report ID_
In filing versions 3 through 5, this was the value in the seventh column of the header row. Since version 6, the report ID has appeared in the sixth column.

The report ID is an indication of whether the filing is an amendment [3] -- that is, does it correct an error in an earlier filing.

If the filing is not an amendment, the report ID field will be blank.

If the filing is an amendment, the report ID will look like this: *FEC-763780*

The numbers after the hyphen in the report ID represent the ID [4] of the original filing that this one amends, even if the original filing has been amended previously.

_The Report Number_
In filing version 3 through 5, this was the value in the eighth column of the header row. Since version 6, the report number has appeared in the seventh column.

The report number is important only for amendments. If the filing is not an amendment, the field will be blank.

In an amendment, the report number represents the number of times the original filing has been amended. The report number is *1-indexed*, meaning that the first amendment to a filing will have report number 1, the second amendment will have report number 2, and so on.


[1] Definition of metadata.

[2] The last update was XXXXXXX. 

[3] For more information on amendments, see chapter XX.

[4] The *filing ID* is the several-digit number unique to each filing. It can be seen in the URL of an electronic filing on the FEC's website, and in the filenames of an electronic filing.
