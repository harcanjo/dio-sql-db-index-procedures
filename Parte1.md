# Parte 1 – Criando índices em Banco de Dados 

1. Para encontrar o departamento que tem mais pessoas:
```sql
SELECT department, COUNT(*) as num_people
FROM employees
GROUP BY department
ORDER BY num_people DESC
LIMIT 1;
```

2. Quais são os departamentos por cidade? 
```sql
SELECT city, department
FROM employees
GROUP BY city, department;

```

3. Relação de empregrados por departamento? 
```sql
SELECT department, COUNT(*) as num_employees
FROM employees
GROUP BY department;
```