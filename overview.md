Overview
==========

The Federal Election Commission offers three general types of downloadable campaign finance data: individual electronic filings in CSV format covering most committees, pipe-delimited bulk itemized data and summary files via FTP from all committees covering two-year election cycles and specialized CSV or XML files via its [Data Catalog](http://fec.gov/data/DataCatalog.do?format=html). Electronic filings are available in real time as they are filed, while the other two types are updated on a regular basis. Let's take them in turn.

Electronic Filings
========

Most committees registered with the FEC are required to file all of their reports electronically. There are two significant exceptions: committees of U.S. Senate candidates (and two senatorial party committees), which file with the Secretary of the Senate, and [committees that raise or spend less than $50,000 in a calendar year](http://fec.gov/ans/answers_filing.shtml#Do_I_need_to_file_electronically), or expect to do so. Electronic filing applies to U.S. House and presidential candidate committees, non-candidate political committees (typically knows as PACs), national, state and local political party committees registered with the FEC and individuals or organizations engaged in independent spending. Electronic filing was mandated in 2001.

Electronic filings can be found via the [FEC's search form](http://www.fec.gov/finance/disclosure/efile_search.shtml), which has a number of options for filtering the results to a particular committee, a particular date or more. The search results include the option to View or Download individual filings, which present the data in HTML and delimited (see __delimiters__) formats, respectively. Individual filings contain all of the records for that filing, stacked on top of each other in varying delimited layouts ([A zip file containing the formats is on FEC.gov](http://www.fec.gov/elecfil/eFilingFormats.zip).)

Even though committees file reports [on a regular schedule](http://www.fec.gov/info/report_dates.shtml), electronic filings occur nearly every day of the year. Some are amendments of previous filings, others are filed in advance (or after) a deadline, and others are filed as changes warrant. Filings that are __amendments__ are indicated in the data, and serve as complete replacements for the original filings.

Bulk FTP Data
========

The FEC has offered bulk data for years, and [its offerings](http://www.fec.gov/finance/disclosure/ftp_download.shtml) include summary and detailed files covering committees, candidates and contributions. The bulk files are updated weekly, late on Sunday nights, so depending on your timing and needs the bulk files may not be suitable for every task. The advantage of the bulk files is that they are vetted by the FEC, with some of the records standardized (by adding FEC-issued committee ids, for example) and others removed to prevent duplicate records from appearing. The __summary___ files are in fixed-width format, while the __detailed__ files are either fixed-width or pipe-delimited. The FEC is increasingly moving to pipe-delimited formats.

Bulk data files are contained inside zip files stored on the FTP server, so retrieving them via a web application requires several steps. The FTP data is updated early Monday morning each week, and previous cycles are updated as well, since committees can amend filings from an earlier election cycle.

Data Catalog
========

The data catalog is a collection of some of the summary files available via FTP as well as other files covering disbursements, independent expenditures and leadership PACs, among other subjects. The files are available in CSV or XML formats, and cover single cycles (mostly 2010 and 2012, although the summary files also include 2008 data). One advantage of the data catalog files is that they can be called directly from a web application without having to unzip them, but there are some drawbacks. [Independent Expenditures](http://fec.gov/data/IndependentExpenditure.do?format=html&election_yr=2012) include both original transactions and amendments, resulting in duplicate records in those cases. In another example, the [listing of leadership PACs](http://fec.gov/data/Leadership.do?format=html&election_yr=2012) contains an entry for the corporate PAC of Interactive Corp. Most of the data catalog files are updated daily, and they are the one place where it's possible to find [candidate disbursements](http://fec.gov/data/CandidateDisbursement.do?format=html&election_yr=2012) in statewide or district-level files. The files themselves are stored on the FEC's FTP server, so it's possible to grab them directly. The FEC also maintains [a blog about its data](http://fec.gov/blog/) that includes changes and additions to its data offerings.
