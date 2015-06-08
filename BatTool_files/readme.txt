^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ 
  ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^
^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^  

Overview of the readme file:

The first time you use BatTool, you will need to 
install the package. Subsequent times, you will
only need to load the package, unless you have
installed a new version of R.

You will need to change the working directory in R for 
both installation and use of the package. The working
directory should contain the following user files and sub-folders:

Open_BatTool_script.R
GUI_User_Manual.pdf
BatTool_X.X.zip (where X.X is the current version, e.g, 5.3)
readme.txt (this file)
Editable_input_files_by_User
	- IndianaBatAndHibData.csv
	- LambdaEstimatseFromObservations.csv
	- WNS_other_1.csv
	- WNS_other_2.csv
	- whitenoseBeginYears.csv
	- whitenoseProbabilitiesIb.csv
	- whitenoseProbabilitiesLbb.csv
	- take parameters.csv

This readme file contains 3 secitons:
1) Installing the tool
2) Loading the tool
3) Finding more help about the tool

^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ 
  ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^
^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^  

Install steps for the BatTool package:

1) Open R and change your working directory to the 
   location of package (BatTool_X.X.zip) where X.X 
   is the version number (e.g., 5.0). This should
   also be the location where you want to use the
   package (e.g., a file in 
   "My documents/MyBatAssessment"). This may be done 
   through either the R's menu system or through 
   terminal commands in R.

   With R's menu system:
   
	File -> Change dir 
	and then navigate and select your file. 

	There are video tutorials of this step
	on web. As an example a Google search for
	"change working directory r windows"
	found a video tutorial demonstrating this 
	process:
	http://www.youtube.com/watch?v=CCMVaRRLqYw

   -----OR-----

   Through the terminal in R:
	getwd()	##Current working directory
	setwd("C:/your/path/here")
		##Make sure to keep everything in this folder
		##NOTE THE BACKSLASHES INSTEAD OF FORWARD SLASHES
	getwd()	##Notice the change in working directory

2) Install the required package gWidgetstcltk with 
   either the R GUI (Toolbar and menu system):

   Packages -> Install Package(s)

   -----OR-----

   install.packages("gWidgetstcltk")

   Choose the Cran mirror nearest to you (any of the US mirros should be okay).

3) Install the BatTool package with either the
   R GUI (Toolbar and menu system):

   Packages -> Install Package(s) from local zip files...

   -----OR------

   Install the package in R by running this line of code: 
   install.packages("./BatTool_X.X.zip", repo = NULL)
   Where X.X is the version number (e.g., 5.0)

This installation step will need to be repeated if either
a new version of R is installed on your computer or a new 
version of the tool is released and you wish to upgrade.

^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ 
  ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^
^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^

Using the Tool: 

Change your working directory to the place where you are
keeping the package files.

To load the package, type 
	library(BatTool)
	
To launch the GUI, type 
	demo("GUIcode")
	
Be sure your working directory also contains the 
following files:
- Year white-nose syndrome occurred or is expected to occur:
  whitenoseBeginYear.csv

- FWS-derived consequences of WNS on Indiana bats:
  whitenoseProbabilitiesIb.csv	

- Frick et al consequences of WNS on Little Brown bats:
  whitenoseProbabilitiesLBB.csv		

- User specified consequences of WNS for scenario 1:
  WNS_other_1.csv
- User specified consequences of WNS for scenario 2:
  WNS_other_2.csv

- Modeled estimates of population rate of change
  LambdaEstimatesFromObservations.csv	

- Population counts for wintering populations
  IndianaBatAndHibData.csv			

^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ 
  ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^
^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^ ^o^

All documentation for R may be accessed from within R.
To do access the help files, load the help file for the 
BatTool package:
	??BatTool 

The Vignette is the User Manual for the GUI
The other help page contains the command line function
for BatTool. Note that after clicking on the package 
help page, you will need to click on "Index" to see the 
functions in the package. The "Index" is hidden in the
middle of the bottom of the page. 

Command line users will likely want to use either the 
	main_pop
function or the
	pop_stochastic 
function.

Type 
	example(main_pop) 
or 
	example(pop_stochastic)
to see examples of the functions. Type
	?main_pop 
or 
	?pop_stochastic	
to see the functions help files.
