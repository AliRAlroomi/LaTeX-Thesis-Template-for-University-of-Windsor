# LaTeX-Thesis-Template-for-University-of-Windsor
This Thesis Template is created by me as a tool to help graduate students of the University of Windsor in writing their theses and dissertations
It is based on the university standard class [http://rcim.ca/Resources.shtml] created by Till Kuendiger, which is shown below and attached in this project:

								A Thesis Document Class
				Research Centre for Integrated Microsystems
								University of Windsor
							
								Current Version:	0.33

This document class is a derivative of the standard 'book' document class available through LaTeX2e, and hence requires all of the support files for the book document class to be installed.  All of the same document options which work for book documents should work for this class as well.

By default the body baselinestretch is set to 50% (as per University guidelines). This may be overriden with the command (to 35% in this example):

\renewcommand{\lspacing}{1.35}

Two shortcut's have been added which may be used to simple switch from single space and "double space" (i.e. to whatever lspacing is set to):

\ssp	for single spacing
\dsp	for `lspacing` spacing

The Thesis/Disertation should have the following page order (as per University guidelines).  All of these pages should appear in the "frontmatter" in order to meet requirements regarding page number set be graduate studies:
	1	Title page
	2	Copyright page
	3	Approval page
	4	Abstract
	5	Dedication page (optional)
	6	Acknowledgements (optional)
	7	Table of Contents
	8	List of Figures
	9	List of Tables
	
Followed by the main matter of the thesis.
	

Usage:
------

\documentclass[options]{vlsithesis}

New Variables
-------------
In addition to the usual \title and \author fields there are:

	\degree	
	This should be the degree type. e.g. Master of Applied Science.
	
	\doctype	
	This should be either Thesis or Dissertation.
	
	\numberofmembers
	The number of committee members, this field may range from 1 to 6.

	\membera, \memberb, \memberc ....
	The names of respective committe members. These field may be left empty

	\depta, \deptb, \deptc ....
	The departments of the respective committe members.  These field may be left empty

	\year
	The current year.

	\defensedate
	The scheduled date of the defense.

New Environments
----------------
Dedications:  This environemnt correctly setups a dedication's page.  It is assumed that the dedication will fit within one page of text.

Example useage:

\begin{dedication}
\vspace*{2.5in}
To me, the only person worth my company
\vfill
\end{dedication}

Vita Auctoris: This environment is to be used for the Vita Auctoris.  It is to be the last page/section in the Thesis (after all other backmatter).

Example usage:

\begin{vita}
Marry scott was born in 1976 in Windsor, Ontario. She ....
\end{vita}

New Commands
------------

	\makecopyright
	Generates a copyright page.  This sould be used in the front matter.

	\makeapproval
	This generates the approval page.  Should be used in the front matter.

	\chapterabstract{text}
	This command lets the user enter a small abstract that will be included in the chapter mark/heading.  If desired it should be executed prior to the \chapter command which should contain the text. e.g.:

			\chapterabstract{Hello World}
			\chapter{Introduction}



Till Kuendiger
