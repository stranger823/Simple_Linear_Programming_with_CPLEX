## Instruction for CPLEX Python API

#### Download and install CPLEX Optimization Studio
[Download link 1](https://www-01.ibm.com/marketing/iwm/iwm/web/reg/download.do?source=ESD-ILOG-OPST-EVAL&S_TACT=000000OA&S_CMP=web_ibm_ws_ilg-opt_bod_cospreviewedition-ov&S_PKG=CRY7XML&lang=en_US&cp=UTF-8)
or[Download link 2](
http://www-01.ibm.com/software/websphere/products/optimization/cplex-studio-community-edition/)

Mac:
Install Mac Java Development Kit  - [link](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

Run: 
`chmod +x /Users/sarahdunworth/Documents/Community/Extensions/CPLEX/COSCE1263MACOS.bin`

Notes: 
Use this path in mac `/Users/sarahdunworth/Documents/Community/Extensions/CPLEX/COSCE1263MACOS.bin`


####  Download and install " Visual C++ Redistributable Packages for Visual Studio 2013 "
[link](https://www.microsoft.com/en-US/download/details.aspx?id=40784)
Notes: I guess you don't need this in MAC.

####  Install python.

####  Go to CPLEX Optimization Studio install folder.
Win:
C:\Program Files\IBM\ILOG\CPLEX_Studio_Community127
Mac:
Sarahs-MacBook-Pro:x86-64_osx sarahdunworth$ python setup.py install

I had trouble with this, initially getting a failure, then it just ran, after I retried pip install culex. I think 5 might need to happen before 4. 

Sarahs-MacBook-Pro:x86-64_osx sarahdunworth$ python setup.py execute
usage: setup.py [global_opts] cmd1 [cmd1_opts] [cmd2 [cmd2_opts] ...]
   or: setup.py --help [cmd1 cmd2 ...]
   or: setup.py --help-commands
   or: setup.py cmd --help

go to subfoler cplex\python\2.7\x64_win64 and run "python setup.py install"

Notes: 
- a. refer to this [link](
http://www.ibm.com/support/knowledgecenter/SSSA5P_12.5.1/ilog.odms.cplex.help/CPLEX/GettingStarted/topics/set_up/Python_setup.html)
- b. "x64_win64" may different in different OS

####  Run "pip install docplex"
Mac:
Run “easy_install pip”
then run “pip install docplex”


####  download sample code from 
https://github.com/IBMDecisionOptimization/docplex-examples
and unzip it

####  In console run 
python \examples\mp\modeling\diet.py

Mac:
python /Users/sarahdunworth/Documents/Community/Extensions/CPLEX/docplex-examples-master/examples/mp/modeling/diet.py

#### you will get result:
Model: diet
 - number of variables: 9
   - binary=0, integer=0, continuous=9
 - number of constraints: 7
   - linear=7
 - parameters: defaults
* model solved as function:
objective: 2.690
  "Spaghetti W/ Sauce"=2.155
  "Lowfat Milk"=1.831
  "Chocolate Chip Cookies"=10.000
  "Hotdog"=0.930
* KPI: Total Calories=2000.000
* KPI: Total Calcium=800.000
* KPI: Total Iron=11.278
* KPI: Total Vit_A=8518.433
* KPI: Total Dietary_Fiber=25.000
* KPI: Total Carbohydrates=256.806
* KPI: Total Protein=51.174