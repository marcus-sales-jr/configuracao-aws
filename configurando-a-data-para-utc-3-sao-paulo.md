Ajustando a data e hora no Amazon Linux para o Brasil (UTC -3 – São Paulo)
---
Basta executar o seguinte comando como root
```
ln -sf /usr/share/zoneinfo/America/Sao_Paulo /etc/localtime
```
Em seguida exexutar o comando date para verificar se o resultado era o esperado.
```
date
```
