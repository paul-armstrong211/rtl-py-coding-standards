# rtl-py-coding-standards
Centralized location for all RTL-python coding standards. 
https://github.com/cookiecutter/cookiecutter



	1- Class template
	2- Use loguru 
	3- ALWAYS version requirements. 
	4- Pep-8 at least if not black. 
		a. https://black.readthedocs.io/en/stable/installation_and_usage.html
	5- Prioritise readability at all stages if possible. 
	6- F-string for logging where possible
	7- Read me 
	8- Doc string 
	9- Cheat sheets
	10- As much as possible use os.path/basename/dirname/extsplit functions, never use .rsplit['/'] or ['.']
	11- Standardise environment variables (eg: 
	       sql_user = os.environ['MSSQL_USER']
	        sql_password = os.environ['MSSQL_PASSWORD']
	        sql_server = os.environ['MSSQL_SERVER_IP']
	        sql_port = os.environ['MSSQL_PORT']
	        sql_db = os.environ['MSSQL_DB']

Standardize the below as env. Variables too: 
https://dateutil.readthedocs.io/en/stable/relativedelta.html


Add to notes: 
https://github.com/Delgan/loguru

Notes on import ordering: 
https://www.python.org/dev/peps/pep-0008/#imports
https://github.com/reddit-archive/reddit/wiki/PythonImportGuidelines
https://code.google.com/archive/p/soc/wikis/PythonStyleGuide.wiki
https://docs.openstack.org/hacking/latest/
https://www.python.org/dev/peps/pep-0008/ 



------
https://towardsdatascience.com/minimize-for-loop-usage-in-python-78e3bc42f03f
https://towardsdatascience.com/one-simple-trick-for-speeding-up-your-python-code-with-numpy-1afc846db418


https://github.com/joshnh/Git-Commands
https://medium.com/swlh/a-failed-effort-to-get-paid-for-an-open-source-project-bd7fa4658a1e
https://towardsdatascience.com/use-cython-to-get-more-than-30x-speedup-on-your-python-code-f6cb337919b6


There’s a couple of points we can follow when looking to speed things up:
	• If there’s a for-loop over an array, there’s a good chance we can replace it with some built-in Numpy function
	• If we see any type of math, there’s a good chance we can replace it with some built-in Numpy function
Data helper only for targeting AWS
Style guide - always strings in env

https://medium.com/@collectiveacuity/argparse-vs-click-227f53f023dc

Pep - 8 with some minor tweaks

If your code is pep-8 compliant it will pass any validations, however as a general rule, wherever possible, follow the below guides too.


Line Length

From https://google.github.io/styleguide/pyguide.html

[General Guidelines > image2019-7-15_13-2-5.png]
Indentation

From https://google.github.io/styleguide/pyguide.html

[General Guidelines > image2019-7-15_13-0-21.png]


Doc Strings


Naming


List Comprehension

More of a note on performance than on style guides

List comprehensions should only be used when actually storing the output of the list comprehension, 

If you are modifying a list or dict rather use the traditional syntax:

    for x in y:

          x=x+1

http://www.moderndescartes.com/essays/python_list_comprehensions/index.html
