# Postgres SQL

TO_DATE
https://stackoverflow.com/questions/34329852/how-to-insert-date-values-into-table


UPSERT
https://paquier.xyz/postgresql-2/postgres-9-5-feature-highlight-upsert/

## Conversions

https://stackoverflow.com/questions/12375369/convert-hex-string-to-bigint-in-postgres
hex string to bigint (utile pour manipulation index H3)

## Indexing
Lat Lon
```
CREATE EXTENSION btree_gist;
CREATE INDEX job_locations_lat_lng ON job_locations USING gist(tenant_id, ll_to_earth(latitude, longitude));
```

## Avec Node
https://stackoverflow.com/questions/37300997/multi-row-insert-with-pg-promise
