# Metodologia de testes

## Objetivo

Validar o roteamento por setor, a prioridade atribuída e a sugestão de artigos da base Nível 0 no protótipo DeskOps.AI.

## Ambiente

- Repositório: DeskOps.AI
- Versão testada: ed4937f
- Demonstração: GitHub Pages
- Modo avaliado: motor local de regras
- IA generativa: não utilizada na avaliação

## Teste de classificação

- Amostra: 48 casos definidos previamente em `casos_classificacao.csv`.
- Critérios: setor esperado e prioridade esperada comparados ao resultado mostrado pelo protótipo.
- Registro: `resultados_classificacao.csv`.
- Acerto conjunto: setor e prioridade corretos no mesmo caso.

## Teste da base Nível 0

- Amostra: 16 casos com artigo de autoatendimento esperado, definidos em `casos_artigos_nivel0.csv`.
- Critério: artigo sugerido pelo protótipo igual ao artigo esperado.
- Registro: `resultados_artigos_nivel0.csv`.
- Execução: campo “Teste o roteamento” do painel Gestor.

## Medição de tempo

- Medida: tempo de execução da função de classificação.
- Método: executar 10.000 vezes no ambiente local e registrar a mediana.
- Escopo: não inclui rede, carregamento da página nem IA generativa.

## Limitações

- Os casos foram escritos pelo grupo.
- Não houve teste com usuários reais.
- Os dados do protótipo são mantidos no navegador.