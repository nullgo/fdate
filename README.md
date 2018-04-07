# fdate
Formats date string as 'yyyy-mm-dd' and interacts directly on strings.

Useage
-------

Cf. blow::

  >>> fd = Fdate('2018/4/7')
  >>> fd
  '2018-04-07'
  >>> fd = Fdate().from_timestamp(1523030400)
  >>> fd
  '2018-04-07'
  >>> fd.to_timestamp()
  1523030400
  >>> fd + 8
  '2018-04-15'
  >>> fd -= 7
  >>> fd
  '2018-03-31'
  >>> fd.is_last_day(of='M')  # last day of the month
  True
  >>> fd - '2018-04-30'
  -30
  >>> fd.rank  # '2018-03-31' is the 90th day of the year
  90
  >>> Fdate('2018-04-30') >= '2018-03-31'
  True
  >>> [x for x in drange('2018-03-30', '2018-04-03')]
  ['2018-03-30', '2018-03-31', '2018-04-01', '2018-04-02', '2018-04-03']
  >>> [x for x in drange('2018-04-03', '2018-03-30')]
  ['2018-04-03', '2018-04-02', '2018-04-01', '2018-03-31', '2018-03-30']
