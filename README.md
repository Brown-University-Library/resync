======
resync
======

resync is ResourceSync client and library in python.

Typical client usage to synchronize from a source at http://source.example.com/
to a set of local files in /tmp/my_source_example_com:

> resync http://source.example.com/ /tmp/my_source_example_com

Typical library usage in a source:

```python
from resync.resource_list import ResourceList
from resync.resource import Resource

rl = ResourceList()
rl.add( Resource('http://example.com/res1', lastmod='2013-01-01') )
rl.add( Resource('http://example.com/res2', lastmod='2013-01-02') )
print rl.as_xml(rl)
```

Installation
------------

The client and library are designed to work with Python 2.6 or 2.7. You may check the version running on your system with:

    python --version

To download and install the reync client and library, which is currently available only from [Github](https://github.com/resync/resync) (not yet on pypi). 

    cd /tmp
    git clone git://github.com/resync/resync.git
    cd resync/
    python setup.py build
    sudo python setup.py install

This will install the library code in the appropriate place within your python setup, and the client (resync) in an appropriate system path (perhaps /usr/local/bin).

See also
--------

http://github.com/resync/simulator

Copyright and License
---------------------

Copyright 2012,2013 Simeon Warner

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
   
See LICENSE.txt