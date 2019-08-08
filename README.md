### pycassa
---
https://github.com/pycassa/pycassa

```py
import pycassa
pool = pycassa.ConnectionPool('Keyspace1')
pool = pycassa.ConnectionPool('Keyspace1', server_list=['192.168.2.10'])

pool = pycassa.ConnectionPool('Keyspace1')
cf = pycassa.ColumnFamily(pool, 'Standard1')
cf.insert('foo', {'column1': 'val1'})
cf.get('foo')

cf.insert('foo', {'column1': 'val2'})
cf.get('foo')

cf.insert('bar', {'column1': 'val3', 'column2': 'val4'})
cf.multiget(['foo', 'bar'])
cf.get_count('bar')

list(cf.get_range())
list(cf.get_range(row_count=1))

cf.remove('bar', columns=['column1'])
cf.get('bar')
cf.remove('bar')
cf.get('bar')
```

```sh
pip install pycassa
pip install thrift
python setup.py install
```

```
```
