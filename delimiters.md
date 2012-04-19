Electronic filing delimiters
==========

There are two versions of raw data for every electronic filing submitted to the FEC.

In one version, the fields in the filing are delimited by commas. In the other, the fields are delimited by ASCII 28 characters.

In most situations, using the version with comma-separated values (CSV) would be preferable; such files are readable by most spreadsheet programs, and most programming languages have built-in support for CSV parsing.

But the FEC makes it easier to access the ASCII 28-delimited version than the CSV version, so in many cases the added ease of getting to the ASCII 28-delimited version outweighs the benefits of using the CSV version.

Take filing No. 775739, for example. The ASCII 28-delimited version of this filing is available from the easily guessable URL [http://query.nictusa.com/dcdev/posted/775739.fec](http://query.nictusa.com/dcdev/posted/775739.fec)

The CSV version, however, has the URL [http://query.nictusa.com/showcsv/nicweb127546/775739.fec](http://query.nictusa.com/showcsv/nicweb127546/775739.fec) -- that number before the final slash makes it harder to determine programmatically what the URL will be.

If your intention is to work with these files using a programming language, it should be fairly easy to parse the file using a delimiter other than a comma. For example, in Ruby, you would do the following:

    >> require 'csv'
    => true
    >> csv = CSV.open('775739.fec', :col_sep=>"\034")
    => <#CSV io_type:File io_path:"775739.fec" encoding:ASCII-8BIT lineno:0 col_sep:"\x1C" row_sep:"\n" quote_char:"\"">

In Python, you would do:

    >>> csv.reader(open('775739.fec', 'r'), delimiter="\034")
    <_csv.reader object at 0x1004e2210>
    >>> reader = csv.reader(open('775739.fec', 'r'), delimiter="\034")

("\034" is the octal representation of the ASCII 28 character.)

Other programming languages should have similar facilities for setting the file's delimiter.

(The FEC also provides tools for converting the ASCII 28-delimited files into CSVs [here](http://www.fec.gov/support/DataConversionTools.shtml), though I can't vouch for how useful these might be.)

If you know only the filing's ID and prefer to download the CSV, the URL for accessing the link to that version would look like [http://query.nictusa.com/cgi-bin/dcdev/forms/DL/775739/](http://query.nictusa.com/cgi-bin/dcdev/forms/DL/775739/) -- just substitute the ID of the filing you're interested in for 775739.
