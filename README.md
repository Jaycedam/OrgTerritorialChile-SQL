# Organización Territorial de Chile

Script SQL utilizado en Oracle SQL Developer para poblar tablas de la organización terrotorial de Chile (Región - Provincia - Comuna)

Puedes crear tus propias tablas utilizando la siguiente cardinalidad **REGION 1:N PROVINCIA 1:N COMUNA**

## Script

Esta sección utiliza una tabla de referencia **REGION(id, región)**

*SNIPPET*

>INSERT INTO REGION VALUES(1, 'Arica y Parinacota');

>INSERT INTO REGION VALUES(2, 'Tarapacá');

>INSERT INTO REGION VALUES(3, 'Antofagasta');


 
Esta sección distribuye las Provincias de Chile por Región. Tabla de referencia **PROVINCIA(id, provincia, region_fk)**

*SNIPPET*

>**ARICA Y PARINACOTA**

>INSERT INTO PROVINCIA VALUES(1, 'Arica', 1);

>INSERT INTO PROVINCIA VALUES(2, 'Parinacota', 1);

>**TARAPACÁ**

>INSERT INTO PROVINCIA VALUES(3, 'Iquique', 2);

>INSERT INTO PROVINCIA VALUES(4, 'Tamarugal', 2);



Las comunas son distribuidas por provincia. Tabla de referencia **COMUNA(id, comuna, provincia_fk)**

*SNIPPET*

>**ARICA**

>INSERT INTO COMUNA VALUES(1, 'Arica', 1);
>INSERT INTO COMUNA VALUES(2, 'Camarones', 1);

>**PARINACOTA**

>INSERT INTO COMUNA VALUES(3, 'Putre', 2);

>INSERT INTO COMUNA VALUES(4, 'General Lagos', 2);

