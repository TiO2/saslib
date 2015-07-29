# saslib
An HTML report generator to perform the meta data lookup like PROC CONTENTS in SAS.
- It reads the sas7bdat files directly, and does not need SAS installed. 
- Emulate [PROC CONTENTS](http://support.sas.com/documentation/cdl/en/proc/67327/HTML/default/viewer.htm#n1hqa4dk5tay0an15nrys1iwr5o2.htm) by jQuery and [DataTables](https://www.datatables.net/).
- Extract the meta data from all SAS7bdat files under the specified directory. 
- Support IE(>=10), firefox, chrome and any other modern browser. 

## Installation
```
pip install saslib
```
`saslib` requires [sas7bdat](https://pypi.python.org/pypi/sas7bdat) and [jinjia2](https://pypi.python.org/pypi/Jinja2/2.7.3).

## Usage

The module is very simple to use. For example, the SAS data sets under the SASHELP library could be viewed --
```python
from saslib import PROCcontents

sasdata = PROCcontents('c:/Program Files/SASHome/SASFoundation/9.3/core/sashelp')
sasdata.show()
```
The resulting HTML file from the codes above will be like [here](http://dapangmao.github.io/saslib_demo/sashelp.html).

