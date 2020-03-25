
## Postgres tools

create table
```
create table table_name(
    id bigserial primary key not null,
    image_url varchar(1024),
    feature bytea,
    quality real,
    pose json,
    age int,
    rect json,
    age int, 
    gender smallint,
    capture_time timestamp
    ) -- distributed by (id); --for greenplum;
```

delete a table
```
drop table table_name;
```

export table from database to csv file
```
\copy (select id, encode(feature, 'hex'), image_url from table_name) to 'relative_path' with delimiter ',' csv header; 
```

import table from csv file
```
\copy face361 from '$absolute_path' delimiter ',' csv;
```
