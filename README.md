# datedays

[中文介绍文档](https://github.com/liang1024/datedays/blob/main/README-CN.md)

datedays is available on PyPI:

```console
$ pip install datedays
```

Get the list of days in the format "%Y-%m-%d"  
When we want a lot of time This library can be used for this fixed format date array

For Example 1:

**Get the required date quantity list（within 3 months by default）**  
Test time 2022-08-05

```
import datedays

if __name__ == '__main__':
    print(datedays.getdays()[:3])  # Three days
    print(datedays.getdays()[:10])  # Ten days
    print(datedays.getdays())
```

```
['2022-08-05', '2022-08-06', '2022-08-07']
['2022-08-05', '2022-08-06', '2022-08-07', '2022-08-08', '2022-08-09', '2022-08-10', '2022-08-11', '2022-08-12', '2022-08-13', '2022-08-14']
['2022-08-05', '2022-08-06', '2022-08-07', ..., '2022-11-29', '2022-11-30']
```

For Example 2:  

**Get the remaining days of the specified month,**  
**```current_date=None```If the date is empty,**  
**the current remaining days will be obtained**

```
import datedays

if __name__ == '__main__':
    print(datedays.getcurrent_days())
```

```
['2022-08-05', '2022-08-06',... '2022-08-30', '2022-08-31']
```

For Example 3:

**Return to the next month date list (automatically cross year)**

```
import datedays

if __name__ == '__main__':
    print(datedays.getnext_days())
```

```
['2022-09-01', '2022-09-02', ... '2022-09-29', '2022-09-30']
```
