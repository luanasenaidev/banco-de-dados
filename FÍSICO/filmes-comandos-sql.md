# Comandos SQL - Referência 
<!-- _____________________________________________________________________---- -->
## Modelagem física

### Criar banco de dados

```sql
CREATE DATABASE filmes CHARACTER SET utf8mb4;
```
<!-- _________________________________________________________ -->
### Criar a tabela generos

```sql
CREATE TABLE generos(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    genero VARCHAR(45) NOT NULL,    
)

```
<!-- __________________________________________________________________________ -->
### Criar a tabela filmes

```sql
CREATE TABLE filmes(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    titulo VARCHAR(45) NOT NULL
    lancamento YEAR(4) NOT NULL
)

```
<!-- _________________________________________________________ -->
<!-- __________________________________________________________________ -->
### Adicionar campo/coluna em uma tabela 

```sql
ALTER TABLE filmes ADD genero_id INT NOT NULL
AFTER lancamento;

```

<!-- __________________________________________________________________ -->
### Criação da chave estrangeira (relacionamento entre tabelas)

```sql
ALTER TABLE filmes
    # CONSTRAINT é uma restrição definida no relacionamento
    ADD CONSTRAINT fk_filmes_generos

    # A chave estrangeira deve fazer refêrencia a chave primária  
    FOREIGN KEY(genero_id) REFERENCES generos(id)

```
<!-- _________________________________________________________________________ -->