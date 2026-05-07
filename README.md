 # Payload de Emissão NFS-e - Tecnospeed

Repositório com os exemplos de payload JSON para emissão de Notas Fiscais de Serviço Eletrônicas (NFS-e) via API Tecnospeed.

## Padrões Disponíveis

- **Genérico** (`exemplo-generico.json`) — Utilizado para municípios com layout próprio de comunicação com a prefeitura.
- **NACIONAL** (`exemplo-nacional.json`) — Utilizado para municípios aderentes ao padrão nacional (NFS-e Nacional).

## Estrutura Resumida

Ambos os payloads seguem a mesma estrutura base:

- Dados gerais da nota (valores, descontos, tipo de autorização)
- `prestador` — Dados da empresa emissora
- `tomador` — Dados do cliente/tomador
- `intermediario` — Dados do intermediário (quando houver)
- `rps` — Dados do RPS (série, número, datas)
- `dps` — Dados do DPS (padrão nacional)
- `servico` — Lista de serviços prestados com tributação
- `deducao` — Deduções aplicáveis
- `parcelas` — Condições de pagamento
- `despesas` — Despesas vinculadas

## Como Usar

Utilize o JSON correspondente ao padrão do município como base para montar a requisição de emissão na API.

Campos com valor `null` podem ser omitidos conforme a necessidade.
