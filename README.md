# Círculo Atemporal — monitor de disponibilidade

Monitor diário, aproximadamente a cada cinco minutos, entre 8h e 22h no fuso
America/Sao_Paulo. A primeira execução está prevista para 8h03; agendamentos do
GitHub podem atrasar ou não executar. O monitor reduz a suspensão por inatividade,
sem garantir que o plano gratuito permaneça sempre disponível.

Consulta somente `GET https://circulo-atemporal-api.onrender.com/health`.
Não inclui código do backend, contatos, respostas, senhas ou chaves de API.
Não acessa o banco nem inicia fluxos ou aprovações. Não altera planos ou serviços.

Usa runner padrão em repositório público, sem cache ou artefatos. O trabalho é
bloqueado se o repositório se tornar privado. Horas ativas do Render continuam
consumindo a franquia compartilhada de 750 horas/mês; cerca de 420–434 horas por
mês para 14 horas diárias, mais o período de inatividade antes de suspender.
O GitHub pode desabilitar agendamentos após 60 dias sem atividade no repositório.

## Operação

Consulte as execuções em Actions → Daytime Circulo API health. Para interromper,
use Disable workflow no menu dessa automação. Run workflow permite um teste
manual, mas respeita a mesma janela de horário.

Referências:
- https://render.com/docs/free
- https://docs.github.com/en/billing/concepts/product-billing/github-actions
- https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule
