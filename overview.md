Overview
==========

The Federal Election Commission offers three general types of downloadable campaign finance data: individual electronic filings in CSV format covering most committees, fixed-width bulk data via FTP from all committees and summary files (both fixed-width and CSV) covering two-year election cycles. Electronic filings are available in real time as they are filed, while the other two types are updated on a regular basis. Let's take them in turn.

Electronic Filings
========

Most committees registered with the FEC are required to file all of their reports electronically. There are two significant exceptions: committees of U.S. Senate candidates (and two senatorial party committees), which file with the Secretary of the Senate, and [committees that raise or spend less than $50,000 in a calendar year](http://fec.gov/ans/answers_filing.shtml#Do_I_need_to_file_electronically), or expect to do so. Electronic filing applies to U.S. House and presidential candidate committees, non-candidate political committees (typically knows as PACs), national, state and local political party committees registered with the FEC and individuals or organizations engaged in independent spending. Electronic filing was mandated in 2001.

Electronic filings can be found via the [FEC's search form](http://www.fec.gov/finance/disclosure/efile_search.shtml), which has a number of options for filtering the results to a particular committee, a particular date or more. The search results include the option to View or Download individual filings, which present the data in HTML and delimited (see __delimiters__) formats, respectively. Individual filings contain all of the records for that filing, stacked on top of each other in varying delimited layouts ([A zip file containing the formats is on FEC.gov](http://www.fec.gov/elecfil/eFilingFormats.zip).)

Even though committees file reports [on a regular schedule](http://www.fec.gov/info/report_dates.shtml), electronic filings occur nearly every day of the year. Some are amendments of previous filings, others are filed in advance (or after) a deadline, and others are filed as changes warrant. Filings that are __amendments__ are indicated in the data, and serve as complete replacements for the original filings.

Bulk FTP Data
========

The FEC has offered bulk data for years, and [its offerings](http://www.fec.gov/finance/disclosure/ftp_download.shtml) include summary and detailed files covering committees, candidates and contributions. The bulk files are updated weekly, late on Sunday nights, so depending on your timing and needs the bulk files may not be suitable for every task. The advantage of the bulk files is that they are vetted by the FEC, with some of the records standardized (by adding FEC-issued committee ids, for example) and others removed to prevent duplicate records from appearing. The summary files are in fixed-width format, while the detailed files are pipe-delimited.

The [summary files](http://www.fec.gov/finance/disclosure/ftpsum.shtml) include canonical data for candidates and committees - one record for each candidate or committee per two-year election cycle, depending on the file selected. There are two candidate summary files -- one for campaigns that have elections in the current cycle, and one for all candidates no matter if they face election in the cycle or not -- and they can differ in amounts and timeliness. The [current campaigns file](ftp://ftp.fec.gov/FEC/webl12.zip) may be more timely, but also contains a single total for PAC contributions (compared to totals for different kinds of PACs in the other file) and some of its totals may contain double-counted transactions.

The [all candidates file](ftp://ftp.fec.gov/FEC/weball12.zip) can be updated slightly less frequently than the current campaigns one, but it contains more detailed breakdowns of certain types of transactions as noted above. The possibility of double-counting some kinds of transactions - transfers to and from authorized committees of a candidate - also exists.

The FEC previously used to generate candidate summary files at the end of the election cycle that included totals for different types of PACs, but discontinued these files after the 2005-2006 cycle. Files are available from 1979-80 through 2005-06.

There's one more thing to look out for - the way that the FEC used to store its data (detailed and summary) relied on the use of [an "overpunch" character](http://www.fec.gov/finance/disclosure/ftpsum.shtml#overpunch) to represent negative amounts. This [recently changed for the detailed contribution files](http://www.fec.gov/blog/disclosure/entry/indiv_oth_and_pas2_file), but it's possible that older summary files still contain such characters, and that the amount fields should be imported as text and then converted to numeric columns, accounting for negative amounts. 