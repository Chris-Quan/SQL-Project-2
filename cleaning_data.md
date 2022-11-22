What issues will you address by cleaning the data?





Queries:
Below, provide the SQL queries you used to clean your data.



## 1. product prices are off by 1000000x
```
    UPDATE all_sessions
    SET productprice = productprice/1000000

    UPDATE analytics
    SET unit_price = unit_price/1000000
```

## 2. remove duplicate data
```
    ALTER TABLE all_sessions
    DROP COLUMN transactionrevenue
    DROP COLUMN transactionrevenue
    DROP COLUMN transactionrevenue
```


## 3. remove tables with only nulls  
```
    ALTER TABLE all_sessions
    DROP COLUMN productRefundAmount
```