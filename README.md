# Projeto-Curso-de-sql-exercicio-one


## Criando as tabelas
 ```sql
CREATE TABLE Pais(
    Nome varchar(35),
    Continente varchar(35),
    Pop float,
    PIB float,
    Expec_vida float
);

CREATE TABLE Cidade(
    Nome varchar(35),
    Pais varchar(35),
    Pop float,
    Capital varchar(1)
);

CREATE TABLE Rio(
    Nome varchar(35),
    Origem varchar(35),
    Comprimento integer
);

INSERT INTO Pais (Nome, Continente, Pop, PIB, Expec_vida)
VALUES
    ('Brasil', 'América do Sul', 213993437, 1.48e12, 75.7),
    ('EUA', 'América do Norte', 332915073, 21.43e12, 78.9),
    ('China', 'Ásia', 1444216107, 16.23e12, 76.9),
    ('Índia', 'Ásia', 1393409038, 2.87e12, 69.7),
    ('Rússia', 'Europa/Ásia', 145912025, 1.47e12, 72.6),
    ('Canadá', 'América do Norte', 38240680, 1.85e12, 82.3),
    ('Austrália', 'Oceania', 25556600, 1.39e12, 83.3),
    ('África do Sul', 'África', 59622350, 351.43e9, 64.1),
    ('México', 'América do Norte', 129166028, 1.28e12, 75.2),
    ('Japão', 'Ásia', 126050804, 5.08e12, 84.6);

-- Inserir dados na tabela Cidade
INSERT INTO Cidade (Nome, Pais, Pop, Capital)
VALUES
    ('Rio de Janeiro', 'Brasil', 6747815, 'N'),
    ('Nova York', 'EUA', 8336817, 'N'),
    ('Pequim', 'China', 21700000, 'C'),
    ('Mumbai', 'Índia', 20069405, 'N'),
    ('Moscou', 'Rússia', 12616816, 'C'),
    ('Toronto', 'Canadá', 2731571, 'N'),
    ('Sydney', 'Austrália', 5230330, 'N'),
    ('Cidade do Cabo', 'África do Sul', 3786991, 'N'),
    ('Cidade do México', 'México', 9209944, 'C'),
    ('Tóquio', 'Japão', 37393129, 'C');

-- Inserir dados na tabela Rio
INSERT INTO Rio (Nome, Origem, Comprimento)
VALUES
    ('Amazonas', 'Peru', 6575),
    ('Mississipi', 'EUA', 6275),
    ('Yangtze', 'China', 6300),
    ('Ganges', 'Índia', 2510),
    ('Volga', 'Rússia', 3531),
    ('Mackenzie', 'Canadá', 4241),
    ('Murray-Darling', 'Austrália', 3374),
    ('Orange', 'Lesoto', 2160),
    ('Grande', 'México', 3184),
    ('Shinano', 'Japão', 367);
 ```
#### Exercicio 1
- Liste todas as cidades e os países aos quais pertencem. 
- Resposta:

```sql
SELECT Nome, Pais FROM Cidade;
```
 #### Exercicio 2
- Liste todas as cidades que são capitais.  
- Resposta:

```sql
select Nome, Pais, Capital  from Cidade where Capital='C';
```

  #### Exercicio 3
- Liste todos os atributos dos países onde a expectativa de vida é menor que 70 anos.   
- Resposta:

```sql
select * from Pais where Expec_vida<70;
```
 
  #### Exercicio 4
- Obsoleto.   
- Resposta:

```sql
```
 
  #### Exercicio 5
-  Quais é o nome e a população da capital do país onde o rio St. Lawrence tem sua nascente. 
- Resposta:

```sql
```
 
   #### Exercicio 6
-  Qual é a média da população das cidades que não são capitais.  
- Resposta:

```sql
```
  
   #### Exercicio 7
- Para cada continente retorne o PIB médio de seus países.  
- Resposta:

```sql
select Continente, avg(PIB)
from Pais
where continente='América do Norte';
```
 
   #### Exercicio 8
- Liste o comprimentos dos rios da tabela Rio.    
- Resposta:

```sql
SELECT Comprimento FROM Rio;
```

   #### Exercicio 9
- Liste os países cujo PIB é maior que o PIB é do Canada   
- Resposta:

```sql
SELECT Nome,PIB FROM Pais WHERE PIB>1850000000000;
``` 













