Desafio Prático GitHub Actions
Objetivo: Entender como funcionam as variáveis no GitHub Actions e os diferentes tipos de escopo.

O que foi feito
Criei um workflow usando ubuntu-latest para testar variáveis globais, variáveis de step, GITHUB_ENV, variáveis padrão do GitHub e também secrets e variables.

Testes
Variáveis globais
Funcionaram em todos os steps.
App: MeuApp
Versão: 1.0
Variável de step
Funcionou apenas no step onde foi criada.
Variável temporária: TEMP123
Tentando usar em outro step:

Step temp:
A variável não apareceu, mostrando que o escopo é só naquele step.

GITHUB_ENV
Criei uma variável que funcionou nos próximos steps.
Nova variável: GeradaNoWorkflow
Variáveis padrão
Usei variáveis do próprio GitHub.
Usuário: arthurzacasantos
Sistema: Linux
Secrets e Variables
A variável apareceu normal:
URL ambiente: https://api.meuprojeto.com
O secret não apareceu:
Token (oculto): ***

Conclusão
As variáveis globais funcionam em todo o workflow.
As variáveis de step só funcionam no próprio step.
O GITHUB_ENV permite usar variáveis entre steps.
Secrets são protegidos e não aparecem no log.
Status:
Deu tudo certo e o workflow executou sem erros.
