Detailed files
========

The [detailed files](http://www.fec.gov/finance/disclosure/ftpdet.shtml) include cycle-specific data for committees, candidates, individual contributions and committee transactions to candidates and between committees. Each cycle, beginning with 1979-80, has five files with data representing that cycle. The current cycle and its immediate 2-3 preceding cycles also have three smaller tables that represent additions, changes and deletions to the individual contributions file. The FEC changed the format of these files from fixed-width to pipe-delimited in July 2012. These files are updated weekly on late Sunday evenings/early Monday mornings, so information submitted during the week before should be reflected in the next update. One advantage of using these files is that they represent "official" data that has been checked by the FEC. Nonetheless, there have been some errors

Committees
---------

Known as the [committee master file](http://www.fec.gov/finance/disclosure/metadata/DataDictionaryCommitteeMaster.shtml), this has a record for each committee registered with the FEC during a cycle. The ID number assigned by the FEC to each committee is unique within the cycle, but committees often exist for years or even decades. If a committee is a campaign committee for a candidate for the House, Senate or President, it will include that candidate's ID number. A committee will be one of [several types](http://www.fec.gov/finance/disclosure/metadata/CommitteeTypeCodes.shtml). Other committees may have values for party affiliation, frequency of filings and connected organization, although these values are not universally present for each committee.

Candidates
---------

Known as the [candidate master file](http://www.fec.gov/finance/disclosure/metadata/DataDictionaryCandidateMaster.shtml), this file contains one row for each candidate who either registered with the FEC or "appeared on a ballot list prepared by a state elections office." Key fields in this file include whether a candidate is an incumbent, challenger or seeking an open seat (although this field is not consistently populated), and the state and district the candidate is running in.

Candidate Committee Linkage
---------

A new offering as of July 2012, [this file](http://www.fec.gov/finance/disclosure/metadata/DataDictionaryCandCmteLinkage.shtml) contains one row for each combination of candidate and committee during an election cycle. Candidates can have a primary committee, authorized committees, joint fundraising committees and other relationships. The linkage file helps keep track of all of those relationships. In particular, joint fundraising committees can benefit multiple candidates; previously the committee master file would only list one.

Committee Contributions To Candidates
---------

[This file](http://www.fec.gov/finance/disclosure/metadata/DataDictionaryContributionstoCandidates.shtml) contains one row for each contribution from a committee to a candidate and for each independent expenditure made by a committee about a candidate. It is a subset of the file containing all transactions between one committee and another. This file can be used to calculate things such as which candidate got the most PAC money and which candidates have received contributions from a specific committee.

Any Transaction from One Committee to Another
---------

[This file](http://www.fec.gov/finance/disclosure/metadata/DataDictionaryCommitteetoCommittee.shtml) contains a row for each transaction between two committees, regardless of whether either committee is a candidate committee or not. For example, this file includes contributions from a corporate PAC to a national party committee in addition to contributions to candidate committees. The list of [transaction types](http://www.fec.gov/finance/disclosure/metadata/DataDictionaryTransactionTypeCodes.shtml) describes the kind of transaction each row represents. The quirk here is that in many cases, both sides of the transaction get separate records: one for the committee making the contribution (usually beginning with 2X) and another for the committee receiving the contribution (usually beginning with 1X). Using this file for SQL queries means including transaction type in some manner in pretty much every query; which types you want depends on a couple of factors, such as timeliness (contributing committees can file before recipient committees) or completeness (a recipient committee usually is the definitive account of what it has gotten).