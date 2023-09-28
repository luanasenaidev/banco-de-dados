# Comandos SQL - Para CRUD (Referência)

## Resumo
C -> Create (Insere dados)
R -> Read (Ler dados)
U -> Update (Atualizar dados)
D -> Delete (Deletar dados)
<!-- _______________________________________________________________________ -->
## Insert 
## Fabricantes

```sql
INSERT INTO generos (genero) VALUES('Comédia');
INSERT INTO generos (genero) VALUES('Ação');
INSERT INTO generos (genero)
VALUES('Suspense'),('Terror'),('Aventura'),('Ficção-Científica');
```
<!-- __________________________________________________________________________________ -->
##  Insert 
## Filmes

```sql
INSERT INTO filmes (titulo, lancamento, genero_id) VALUES(
'Albergue', 
'2005',
4
);
INSERT INTO filmes (titulo, lancamento, genero_id) VALUES(
'Top Gun', 
'2022',
2
);
INSERT INTO filmes (titulo, lancamento, genero_id) VALUES(
'Se beber não case', 
'2009',
1
);