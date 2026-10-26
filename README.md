# forge-probe

Playbook "sonda" (no-op) usado para gravar amostras do contrato da API de um automation controller compatível com AWX: job fatiado, workflow job e artifacts de `set_stats`.

## O que o playbook faz

O `forge_probe.yml` executa somente duas tarefas:
- `debug`;
- `set_stats`, publicando um marcador, `awx_job_id`, `awx_workflow_job_id` e a lista de hosts.

Ele foi feito para rodar com `ansible_connection=local`. Não acessa host remoto, não usa `become`, não instala nada e não chama serviço externo.

## Por que o repositório é público

O projeto do controller faz checkout deste repositório sem credencial. Por isso aqui só existe este playbook, sem nenhum dado de ambiente.

## Origem

A fonte é `tools/contract_capture/probe/forge_probe.yml` do repositório SamurAI Forge, que é privado. Qualquer alteração deve ser feita lá e copiada para cá.
