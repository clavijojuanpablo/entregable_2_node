# Entrega # 2

## 🔗 Link al DBDiagram
[Haz click aquí](https://dbdiagram.io/d/62f46ab7c2d9cf52fa871856)

## 🍔 Trabajo del BLOG

También lo puede encontrar en el .txt que se encuentra en el repositorio.

```bash
CREATE TABLE "users" (
"id" serial PRIMARY KEY,
"name" varchar NOT NULL,
"email" varchar UNIQUE NOT NULL,
"edad" int NOT NULL,
"password" varchar NOT NULL
);
CREATE TABLE "posts" (
  "id" serial PRIMARY KEY,
  "title" varchar NOT NULL,
  "content" varchar NOT NULL,
  "author_id" int NOT NULL,
  "created" timestamp DEFAULT 'now()'
);
CREATE TABLE "comments" (
  "id" serial PRIMARY KEY,
  "user_id" int NOT NULL,
  "post_id" int NOT NULL,
  "age" int NOT NULL,
  "content" varchar NOT NULL
);
ALTER TABLE "posts" ADD FOREIGN KEY ("author_id") REFERENCES "users" ("id");
ALTER TABLE "comments" ADD FOREIGN KEY ("post_id") REFERENCES "posts" ("id");
ALTER TABLE "comments" ADD FOREIGN KEY ("user_id") REFERENCES "users" ("id");
insert into users (
	name,
	email,
	edad,
	password
) values (
	'Moises',
	'moises@gmail.com',
	21,
	'1234'
), (
	'Jorge',
	'jorge@gmail.com',
	21,
	'abcd'
), (
	'Duvan',
	'duvan@gmail.com',
	21,
	'9876'
), (
	'Santiago',
	'santiago@gmail.com',
	21,
	'1234'
), (
	'Juan Pablo',
	'juan@gmail.com',
	21,
	'1234'
), (
	'Paulina',
	'paulina@gmail.com',
	21,
	'1234'
);
insert into posts (
	title,
	content,
	author_id
) values (
	'Learning SQL',
	'learning learninglearninglearninglearninglearning learning learning',
	4
), (
	'Learning React',
	'learning learninglearninglearning',
	1
), (
	'Learning Node',
	'learning  learninglearninglearning learninglearninglearning learninglearninglearning learninglearninglearning',
	5
);
insert into comments (
	user_id,
	post_id,
	age,
	content
) values (
	2,
	1,
	18,
	'Primer Comentario'
), (
	5,
	3,
	18,
	'Segundo Comentario'
), (
	4,
	1,
	18,
	'Tercer Comentario'
);
```
    
