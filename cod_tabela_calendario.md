Tabelas calendário são bastante úteis em projetos de BI.
Elas auxiliam na visualização e segmentação rápida dos dados ao olhar quaisquer parâmetros relacionados a uma data.

Todos os procedimentos foram realizados dentro do Power BI.

- etapa preliminar

Criação da tabela via Modelagem -> Nova tabela

### Uso de linguagem DAX

- criação da coluna com as datas base

Calendario = CALENDAR(date(2020,01,01),date(2020,12,31))

- inserção de coluna do dia

Day = day('Calendario'[Date])

- inserção de coluna do mês

Month = month('Calendario'[Date])

- inserção de coluna do ano

Year = YEAR('Calendario'[Date])

- inserção de coluna com nome do mês completo

MonthName = format('Calendario'[Date],"mmmm")

- inserção de coluna com nome do mês abreviado

MonthNameShort = format('Calendario'[Date],"mmm")

- inserção do coluna com o dia da semana abreviado

Weekday = format('Calendario'[Date],"ddd")

- inserção da coluna com o número do trimestre

Quarter = format('Calendario'[Date],"q")

- inserção da coluna com o ano e número do trimestre

Year-Quarter = Calendario[Year]&"-"&Calendario[Quarter]
