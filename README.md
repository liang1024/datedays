# datedays

[中文介绍文档](https://github.com/liang1024/datedays/blob/main/README-CN.md)

datedays is available on PyPI:

```console
$ pip install datedays
```

Python Date Tools
* It is automatically updated every time.  
For example
* all dates within 2 days to 10 days 
* all dates of the next month.  
Get the list of days in the format "%Y-%m-%d"    

**For Example**:

all dates within 2 days to 10 days 
```
import datedays

if __name__ == '__main__':
    print(datedays.getdays()[2:10]) 
```
output:
```
['2022-08-11', '2022-08-12', '2022-08-13', '2022-08-14', '2022-08-15', '2022-08-16', '2022-08-17', '2022-08-18']
```

other methods：

method| desc
--- | :---:
datedays.getdays()[1:31] |Date within 30 days(From tomorrow)
datedays.getcurrent_days() | Get the remaining days of this month（Including today）
datedays.getnext_days() | Get all dates of the next month
