## Documentation API

```http
POST https://sql-server-oislxufxaa-et.a.run.app/api/query
```

- method
  - `POST`
- body
  ```javascript
  {
    query: string,
  }
  ```
- response

  ```javascript
  {
    error: boolean,
    data: array
  }
  ```

## Table structure

> Places

| Field                        | Type         | Null | Key | Default | Extra |
| ---------------------------- | ------------ | ---- | --- | ------- | ----- |
| Place_ID                     | varchar(45)  | NO   | PRI | NULL    |       |
| Name                         | varchar(255) | NO   |     | NULL    |       |
| FormattedPhone               | varchar(25)  | YES  |     | NULL    |       |
| FormattedAddress             | varchar(255) | YES  |     | NULL    |       |
| Latitude                     | float        | YES  |     | NULL    |       |
| Longitude                    | float        | YES  |     | NULL    |       |
| OverallRating                | float        | YES  |     | NULL    |       |
| PriceLevel                   | float        | YES  |     | NULL    |       |
| Website                      | varchar(255) | YES  |     | NULL    |       |
| UserRatingTotal              | float        | YES  |     | NULL    |       |
| ServesBeer                   | tinyint(1)   | YES  |     | NULL    |       |
| ServesWine                   | tinyint(1)   | YES  |     | NULL    |       |
| ServesVegetarianFood         | tinyint(1)   | YES  |     | NULL    |       |
| WheelchairAccessibleEntrance | tinyint(1)   | YES  |     | NULL    |       |
| Halal                        | tinyint(1)   | YES  |     | NULL    |       |
| StreetAddress                | varchar(255) | YES  |     | NULL    |       |
| District                     | varchar(255) | YES  |     | NULL    |       |
| City                         | varchar(255) | YES  |     | NULL    |       |
| Regency                      | varchar(255) | YES  |     | NULL    |       |
| Province                     | varchar(255) | YES  |     | NULL    |       |
| PostalNumber                 | varchar(25)  | YES  |     | NULL    |       |

> OperationHours

| Field           | Type        | Null | Key | Default | Extra |
| --------------- | ----------- | ---- | --- | ------- | ----- |
| Place_ID        | varchar(45) | YES  | MUL | NULL    |       |
| Monday_Open     | char(5)     | YES  |     | NULL    |       |
| Monday_Close    | char(5)     | YES  |     | NULL    |       |
| Tuesday_Open    | char(5)     | YES  |     | NULL    |       |
| Tuesday_Close   | char(5)     | YES  |     | NULL    |       |
| Wednesday_Open  | char(5)     | YES  |     | NULL    |       |
| Wednesday_Close | char(5)     | YES  |     | NULL    |       |
| Thursday_Open   | char(5)     | YES  |     | NULL    |       |
| Thursday_Close  | char(5)     | YES  |     | NULL    |       |
| Friday_Open     | char(5)     | YES  |     | NULL    |       |
| Friday_Close    | char(5)     | YES  |     | NULL    |       |
| Saturday_Open   | char(5)     | YES  |     | NULL    |       |
| Saturday_Close  | char(5)     | YES  |     | NULL    |       |
| Sunday_Open     | char(5)     | YES  |     | NULL    |       |
| Sunday_Close    | char(5)     | YES  |     | NULL    |       |

> Types

| Field      | Type        | Null | Key | Default | Extra |
| ---------- | ----------- | ---- | --- | ------- | ----- |
| Place_ID   | varchar(45) | YES  | MUL | NULL    |       |
| Bar        | tinyint(1)  | YES  |     | NULL    |       |
| Cafe       | tinyint(1)  | YES  |     | NULL    |       |
| Restaurant | tinyint(1)  | YES  |     | NULL    |       |
