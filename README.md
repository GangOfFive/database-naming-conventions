**Tabla de Contenidos**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

- [Estándares de base de datos para Gang of Five](#est%C3%A1ndares-de-base-de-datos-para-gang-of-five)
	- [Tablas](#tablas)
	- [Atributos](#atributos)
	- [Procedimientos Almacenados](#procedimientos-almacenados)
	- [Triggers](#triggers)
	- [Vistas](#vistas)

# Estándares de base de datos para *Gang of Five*

## Tablas
 - Todas las tablas deben tener un atributo `id`, el cual será su llave primaria.
 - Los nombres de las tablas deben ir en minúscula, ser plurales, y separando las
   palabras con un guión bajo:
   - `users`
   - `permissions`
   - `roles`
   - `private_messages`
  - Las tablas utilizadas para relaciones se deben llamar de la siguiente manera: `table1_table2`.

## Atributos
 - Misma convención de nombramiento que las tablas.
 - Si el atributo es una llave foránea, se debe llamar de la siguiente manerae: `table_id` (singular).
   Por ejemplo, si la tabla `private_messages` tiene una llave foránea para un usuario,
   ésta se deberá llamar `user_id`.

## Procedimientos Almacenados
 - Utilizar `camelCase` y anteponer `sp_`:
   - `sp_findUsers`
   - `sp_cleanupExpiredEvents`

## Triggers
 - Utilizar `camelCase` y anteponer `tg_`.
   Después colocar el nombre de la tabla afectada y la operación:
   - `tg_usersDelete`
   - `th_eventsInsert`

## Vistas
 - Utilizar `camelCase` y anteponer `v_`:
   - `v_usersMostPopular`
   - `v_eventsMostAttended`
