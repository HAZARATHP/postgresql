# postgresqlhttps://github.com/HAZARATHP/SQL.git

procedure_demo=# CREATE OR REPLACE PROCEDURE genre_insert_data("GenreId" integer, "Name" character varying)

procedure_demo-# LANGUAGE SQL

procedure_demo-# AS $$

procedure_demo$# INSERT INTO public."Genre" VALUES ("GenreId", "Name");

procedure_demo$# $$;

CREATE PROCEDURE

procedure_demo=# CALL genre_insert_data(26,'Pop');

CALL

procedure_demo=# select * from public."Genre" where "GenreId" = 26;

 GenreId | Name

---------+------

   26 | Pop

(1 row)
