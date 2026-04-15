# Sistema de Gerenciamento de Reservas de Hotel (Jan/2026)

## 1. Introdução

## 2. Visão Geral
 
## 3. Requisitos Específicos

### 3.1 Requisitos Funcionais
#### RF-010 - reserva dos quartos

Versão 1.0 – Janeiro de 2026
- Na priemira versão, o sistema permitia que os usuários realizassem reservas com antecedência mínima de 24 horas e máxima de 6 meses.
  
Versão 2.0 - Fevereiro de 2026
- Depois da solicitação do departamento de vendas, colocaram uma regra para os clientes VIP. Os clientes agora tem a possibilidade de reservas com ate 1 ano de antecedencia, e não tem um preço adicional.

Versão 3.0 - Março de 2026
- Antes a empresa permitia a reserva de ultima hora com menos de 2 horas de antecedencia, mas agora decidiram colocar um preço adicional de 15% para o valor da reserva, para compensar o atraso da reserva.

## 4. Controle de Versão


### 4.1 Histórico de Versões

|Versão|Data|Autor|Mudança|
|------|----|-----|-------|
|1.0|2026-01|Hotel|Criação inicial com limite de reservas entre 24h e 6 meses|
|2.0|2026-02|Hotel|Possibilidade de reservas com até 1 ano de antecedência para os clientes VIP|
|3.0|2026-03|Hotel|Liberaram as reservas de última hora com a taxa adicional de 15%|

 
#### Registro do Git
- git commit -m "feat: adiciona a antecedencia de reservas"
- git commit -m "feat: adiciona reservas com até 1 ano de antecedência para os clientes VIP"
- git commit -m "feat: adiciona reservas de última hora com preço adicional de 15%"


#### Análise de Impacto

- A mudança feita na versão 3.0 pode afetar algumas outras funcionalidades do sistema, principalmente aquelas relacionadas a reservas, pagamentos e comunicação com o cliente.

### Requisitos que podem ser afetados
 - Pagamentos – Ter que  incluir o cálculo automático da taxa adicional de 15% nas reservas de última hora.
 - As notificações – o sistema deve avisar ao cliente que a reserva possui uma taxa adicional.
 - Pessoas usando – é importante saber corretamente quais são as pessoas que usa  clientes VIP.
 - Reserva dos quartos – Talvez seja necessario mudar as regras para permitir reservas feitas muito próximas do horário da reserva.
  
##### Stakeholders que devem aprovar a mudança
      - finaceira 
      - desenvolvimento
      - as vendas

Médio

Essa mudança vai precisar de alguns ajustes no sistema. Tem que atualizar as regras de reservas, calcular a taxa adicional e garantir que a pessoa veja direitinho o valor final da reserva.


## 5. Conclusão
As versões RF-010 ajuda a acompanhar as mudanças de ideias do hotel.
Registrar esse histórico ajuda a equipe a acompanhar as mudanças feitas ao longo do projeto e a entender com mais facilidade os impactos de cada alteração.