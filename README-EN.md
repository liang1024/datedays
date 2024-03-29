# datedays


## What can it do?

* [1. Get common date data](#datadays)
* [2. Operating excel report](#excel)
* [3. Perform common encryption signature](#hash)
* [4. Obtain the encrypted signature of the file](#file)
* [5. Other](#other)

datedays is available on PyPI:

```console
$ pip install datedays
```

**for example**:

```python
import datedays

if __name__ == '__main__':
    print('now :', datedays.getnow())  # format_=Format such as:%Y-%m-%d %H:%M:%S
    print('-' * 30)
    print('tomorrow:', datedays.gettomorrow())
    print('the day after tomorrow:', datedays.gettomorrow(days=2))  # Days is the number of days
    print('after 30 days:', datedays.gettomorrow(days=30))
    print('after 180 days:', datedays.gettomorrow(days=180))
    print('after 1000 days:', datedays.gettomorrow(days=1000))
    print('-' * 30)
    print('yesterday:', datedays.getyesterday())
    print('the day before yesterday:', datedays.getyesterday(days=2))
    print('180 days ago:', datedays.getyesterday(days=180))
    print('1000 days ago:', datedays.getyesterday(days=1000))
```

```
now : 2022-08-19 15:13:44
------------------------------
tomorrow: 2022-08-20
the day after tomorrow: 2022-08-21
after 30 days: 2022-09-18
after 180 days: 2023-02-15
after 1000 days: 2025-05-15
------------------------------
yesterday: 2022-08-18
the day before yesterday: 2022-08-17
180 days ago: 2022-02-20
1000 days ago: 2019-11-23
```

### Still updating

## 1. Get common date data

Method | description | return result | parameter<a id = "datadays"></a>
:---: | :---:| :---:| :---:
getnow() | get today's date | for example: 2022-08-16 17:56:17|
gettomorrow() | tomorrow | 2022-08-17 | select the next day (just pass in the number you want)
getyesterday() | yesterday | 2022-08-15 | select the last day (just pass in the desired number)
getdays() | default date list within three months |... (test printing is recommended) | number = number of months you want
getnowtimestamp() | get the current timestamp | 1660644568238 | default milliseconds (optional seconds, milliseconds, microseconds)
gettodaydays() | get the list of remaining days of this month by default |... (it is recommended to test and print) | you can specify a day of a month to get the remaining days of the month
getnextdays() | get the total number of days of the next month by default |... (test printing is recommended) | you can specify the month and the number of months
getstr2timestamp() | date string to timestamp |... (test printing is recommended) | parameter 1: date, parameter 2: date format
gettimestamp2str() | timestamp to date string |... (test printing is recommended) | parameter 1:timestamp
getstartend() | get interval days or days list |... (test printing is recommended) | parameter 1:start date, parameter 2:end date parameter 3:return list
headers2dict() | copy headers string convert dict |... (test printing is recommended) | parameter 1: headers string

## 2. Operate excel report

Method | description | return result | parameter<a id = "excel"></a>
:---: | :---:| :---:| :---:
excel_write_openpyxl() | write excel report |... (recommended test) | filename: file name, data: data to be saved, format: [first line], [second line], [Third Line]...]
excel_read_openpyxl() | read excel report |... (recommended test) | filename: filename, sheet_ Index: subscript of sheet
excel_read_xlrd() | read excel report (support XLS) |... (recommended test) | filename: filename, sheet_ Index: subscript of sheet

## 3. Perform common encryption signature

Method | description | return result | parameter <a id = "hash"></a>
:---: | :---:| :---:| :---:
md2() | MD2 encryption |... (recommended test) | body: encrypted content, encode: encoding format
md5() | MD5 encryption |... (default 32-bit result) | body: encrypted content, encode: encoding format, length_: Return length, optional 16
sha1() | SHA1 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha2_224() |SHA2_224 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha2_256() |SHA2_256 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha2_384() |SHA2_384 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha2_512() |SHA2_512 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha3_224() |SHA3_224 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha3_256() |SHA3_256 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha3_384() |SHA3_384 encryption |... (recommended test) | body: encrypted content, encode: encoding format
sha3_512() |SHA3_512 encryption |... (recommended test) | body: encrypted content, encode: encoding format

## 4. Obtain the encrypted signature of the file

Method | description | return result | parameter <a id = "file"></a>
:---: | :---:| :---:| :---:
encrypt_smallfile() | encrypt small files |... (recommended test) | filename: filename, mode: default MD5 (optional encryption above)
encrypt_bigfile() | encrypt large files |... (recommended test) | filename: filename, mode: default MD5 (optional encryption above)

## Other...

Method | description | return result | parameter <a id = "other"></a>
:---: | :---:| :---:| :---:
getuuid() | get uuid(support1,3,4,5) |... (recommended test) | mode:default uuid4,merge:replace('-', '')
getrandompassword() | randomly generated password |... (recommended test) | k: result length, more_characters: recommended !@#$%.*&+-

**For Example**

all dates within 2 days to 10 days

```
import datedays

if __name__ == '__main__':
    print(datedays.getdays()[2:10]) 
```

output

```
['2022-08-11', '2022-08-12', '2022-08-13', '2022-08-14', '2022-08-15', '2022-08-16', '2022-08-17', '2022-08-18']
```

I hope it can help you!

