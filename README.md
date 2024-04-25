# dib3_utils

Biblioteca com ferramentas úteis para cálculos com contratos de depósitos interbancários (DI) da B3. Sem dependências externas e simples API.


# Instalação
```
pip install dib3_utils
```

# Uso
```python
import datetime
import dib3_utils
```
```
>>> dib3_utils.vencimento('DI1F30')
datetime.date(2030, 1, 2)

>>> dib3_utils.dias_uteis_vencimento('DI1F30') 
1424

>>> dib3_utils.dias_corridos_vencimento('DI1F30') 
2079

>>> dib3_utils.pu(ticker='DI1F30', taxa=0.11)   
55448.42

>>> dib3_utils.taxa(ticker='DI1F30', pu=55448.42) 
0.11

>>> dib3_utils.dv01(ticker='DI1F30', taxa=0.11)   
28.22