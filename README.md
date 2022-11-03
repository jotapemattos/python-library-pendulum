# Pendulum

### Introdução 

Pendulum é uma biblioteca com a funcionalidade de facilitar a manipulação de datas em python.
Essa biblioteca é bascicamente um *datetime*, porém melhorada.
Apesar do *datetime* ser perfomático, ele não é muito funcional em casos mais complexos como por exemplo:

- Descobrir se o ano é bissexto;

- Qual o horário em Berlim, Paris, etc;

- Quanto tempo falta para quarta-feira da próxma semana.

Fatores como subtrair dias de uma data atual são mais simples utilizando pendulum, uma vez que não é necessário mudar a o mês ou verificar a base do mês;

É uma biblioteca third-party, por isso é necessário fazer a instalação.

### Instalação

O Pendulum é compatível com as versões Python 2.7 e 3.4+

Para instalar é simples, basta digitar o seguinte comando no terminal de sua máquina:

`$ pip install pendulum`

## Utilizando pendulum

####  Alguns atributos

```python

import pendulum
#atributes

dt = pendulum.now() #now representa o horário da máquina em que o sistema está sendo executado

dt.year #2022

dt.month #11

dt.day #03

dt.day_of_week #4

dt.hour 
```

### Algumas funcionalidades

```python

#descobrir a idade passando a data de nascimento como parâmetro
print(pendulum.datetime(2004, 6, 28).age)
#18

#descobrir se o ano é bissexto
year = pendulum.datetime(2020, 5, 30)
print(year.is_leap_year())
#True

year = pendulum.now()
print(year.is_leap_year())
#retorna um valor booleano
#False

#mostrar o horário em determinada região do mundo
now_in_paris = pendulum.now('Europe/Paris')
print(now_in_paris)

#adicionar um dia ou substrair semanas
tomorrow = pendulum.now().add(days=1)
last_week = pendulum.now().subtract(week=1)
```
  
Para mais informações, acesse: https://pendulum.eustace.io/
