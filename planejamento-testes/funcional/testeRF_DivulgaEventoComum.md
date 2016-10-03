
# Planejamento para Teste Funcional - RF-DivulgEventComun

## Descrição do Requisito
Divulgar à comunidade de usuários evento relacionado ao sistema SempreUFG.

## Suposições e Dúvidas
- A publicação de eventos nesse requisito será somente via e-mail
- A publicação de eventos nesse requisito será somente para usuários registrados no sistema
- Evento já foi aprovado nesse caso?
	<!-- TODO: definir datas fixas para testar as divulgações -->

## Caso de Teste - Evento não aprovado não é enviado

### Entrada
Um evento enviado à análise, porém não aprovado pelo responsável.

### Resultado esperado
O Sistema deve mostrar uma mensagem de erro, e nãoi enviar o evento para nenhum interessado.

## Caso de Teste - Evento é divulgado apenas uma vez

### Entrada
Um evento válido, e que tenha sido aprovado devidamente. Uma lista de usuários que aceitaram receber eventos apenas uma vez por semana.

### Resultado esperado
O evento é enviado para o e-mail da lista de usuários definida, porém apenas uma vez.
O evento não é enviado mais de uma vez para o mesmo usuário.

## Caso de Teste - Evento é enviado à uma lista de usuários com definições de notificação semanal

### Entrada
Um evento válido, e que tenha sido aprovado.
Uma lista de usuários que aceitam notificações apenas semanalmente.

### Resultado esperado
O evento é enviado corretamente para todos os usuários na lista.
O evento é enviado de acordo com a configuração de cada usuário, por exemplo:
* João tem configuração para receber evento apenas semanalmente, e a última vez que ele recebeu uma notificação foi em 09/10/2016.
* Se a mensagem for enviada para publicação no dia 10/10/2016, então João só receberá a mensagem no dia 16/10/2016.

## Caso de Teste - Evento é enviado para todos os usuários do sistema (estresse?)

### Entrada
Um evento válido, e que tenha sido aprovado.
Evento para ser enviado no dia 10/10/2016

### Resultado esperado
O evento é enviado corretamente à todos os usuários do sistema globalmente, porém honrando as configurações de cada usuário.
Usuários semanais só verão o evento na próxima divulgação para eles.
Usuários diários verão o evento no dia 11/10/2016
Usuários mensais só verão o evento no mês 11, na <data_fixa_de_divulgação_mensal>


## Caso de Teste

### Entrada

### Resultado esperado
