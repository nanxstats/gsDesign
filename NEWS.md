3.2.0, January, 2021
 - Substantially updated unit testing to increase code coverage above 80%
 - Updated error checking messages to print function where check fails
 - Removed dependencies on plyr packages
 
3.1.1, May, 2020
- Vignettes updated
- Added hGraph() to support ggplot2 versions of multiplicity graphs
- Eliminated unnecessary check from sequentialPValue
- Targeted release to CRAN
- Removed dependencies on reshape2, plyr
- Updated continuous integration
- Updated license

3.1.0, April, 2019
- Addition of pkgdown web site
- Updated unit testing to from RUnit to testthat
- Converted to ROxygen2 generation of help files
- Converted vignettes to RMarkdown
- Added Travis-CI and Appveyor support
- Added sequentialPValue function 
- Backwards compatible addition of spending time capabilities to gsDesign and gsSurv

3.0-5, January, 2018
- registered C routines
- fix "gsbound"
- replace "array" by "rep" calls to avoid R CMD check warnings

3.0-4, September, 2017
- First Github-based release
- Cleaned up documentation for nBinomial1Sample
- Updated documentation and code (including one default value for an argument) for nBinomial1Sample to improve error handling and clarity 
- Updated sfLDOF to generalize with rho parameter; still backwards compatible for Lan-DeMets O'Brien-Fleming

3.0-3 (not released)
- Introduced spending time as a separate concept from information time to enable concepts such as calendar-based spending functions. The only user function changed is the gsDesign function and the change is the addition of the parameters usTime and lsTime; default behavior is backwards compatible.

3.0-2, February, 2016 (not released)
- Simplified conditional power section of gsDesignManual.pdf in doc directory
- Corrected basic calculation in gsCP()
- Eliminated deprecated ggplot2 function opts

3.0-1, January, 2016
- More changes to comply with R standards (in NAMESPACE - importFrom statements - and DESCRIPTION - adding plyr to imports) ensuring appropriate references.
- Deleted link in documentation that no longer exists (gsBinomialExact.Rd).
- Last planned RForge-based release; moving to Github.


3.0-0, December, 2015
- Updated xtable extension to meet R standards for extensions. 
- Fixed xtable.gsSurv and print.gsSurv to work with 1-sided designs
- Update to calls to ggplot to replace show_guide (deprecated) with show.legend arguments where used in geom_text (function from ggplot2 package) calls; no user impact
- Minor typo fixed in sfLogistic help file
- Cleaned up "imports" and "depends" in an effort to be an R "good citizen"
- Registered S3 methods in NAMESPACE

2.9-4
- Minor edit to package description to comply with R standards

2.9-3, November, 2014
- Added sfTrimmed as likely preferred spending function approach to skipping early or all interim efficacy analyses; this also can adjust bound when final analysis is performed with less than maximum planned information. Updated help(sfTrimmed) to demonstrate these capabilities.
- Added sfGapped, which is primarily intended to eliminate futility analyses later in a study; see help(sfGapped) for an example
- Added summary.spendfn to provide textual summary of spending functions; this simplified the print function for gsDesign objects
- Added sfStep which can be used to set an interim spend when the exact amount of information is unknown; an example of how this can be misused is provided in the help file.
- Fixed rounding so that gsBoundSummary, xtable.gsSurv and summary.gsDesign are consistent for gsSurv objects
