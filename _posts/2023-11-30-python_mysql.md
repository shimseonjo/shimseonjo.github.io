---
title: MarkDown
author: shimseonjo
date: 2023-11-30
category: Doc
layout: post
---
python 에서 mysql 데이터베이스 연결하는 방법을 배웁니다.

# 샘플 데이터베이스 다운로드
[샘플 데이터베이스 다운로드](/data/python_mysql.sql)

# 데이터베이스 연결하기
```python
# 01_connect.py
import mysql.connector
from mysql.connector import Error


def connect():
    """ Connect to MySQL database """
    conn = None
    try:
        conn = mysql.connector.connect(host='localhost',
                                       database='python_mysql',
                                       user='root',
                                       password='SecurePass1!')
        if conn.is_connected():
            print('Connected to MySQL database')

    except Error as e:
        print(e)

    finally:
        if conn is not None and conn.is_connected():
            conn.close()


if __name__ == '__main__':
    connect()
```