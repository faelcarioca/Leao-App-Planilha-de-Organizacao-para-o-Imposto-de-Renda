# 🦁 Leão App — Planilha de Organização para o Imposto de Renda

Planilha em Excel que reúne, em um só lugar, as informações essenciais para preencher a **Declaração de Imposto de Renda de Pessoa Física (IRPF)**: dados do contribuinte, saldos em bancos e lançamento mensal de receitas.

> Projeto de portfólio: demonstra como transformar uma planilha comum em uma pequena **aplicação** com navegação, validação de dados e interface própria, usando apenas recursos nativos do Excel (sem macros).

---

## 📌 O problema

Na época da declaração, é comum precisar vasculhar e-mails, apps de banco e PDFs para juntar CPF, informes de rendimento, saldos e receitas do ano. A ideia desta planilha é **centralizar e padronizar** essas informações ao longo do ano, para que a declaração seja só consultar e copiar.

## 🧭 Como funciona

A planilha tem três abas de preenchimento, organizadas como um fluxo guiado:

| Aba | O que faz |
|---|---|
| **1 · TITULAR** | Cadastro do contribuinte: nome, CPF, nascimento, título de eleitor, cônjuge, endereço, contatos e perguntas de triagem (houve alterações desde a última entrega? cônjuge dependente? reside no exterior?). |
| **2 · INFORMES** | Informes de rendimentos bancários: para cada banco, instituição (lista suspensa), valor atual e nome do arquivo anexo (PDF do informe). Calcula automaticamente o **total** de patrimônio informado. |
| **3 · NOTAS** | Tabela de entradas mês a mês: data, categoria (Holerite, CNPJ ou Freelance) e valor, com filtros e linhas zebradas. |

## ✨ Recursos de Excel utilizados

- **Navegação por botões**: menu lateral com botões clicáveis (formas com hiperlinks internos) para alternar entre as abas, mais botão "Próximo". Funciona como uma interface de app.
- **Validação de dados com listas suspensas**
  - Lista de bancos com código e nome (ex.: `260 - Nubank`), alimentada por uma **aba oculta (`BANCOS`)** como base de dados.
  - Respostas `SIM`/`NÃO` nas perguntas de triagem.
  - Categorias de receita (`HOLERITE`, `CNPJ`, `FREELANCE`).
- **Fórmulas**: `SOMA` consolidando os valores dos bancos no total de patrimônio.
- **Tabela estruturada do Excel** (`Tabela2`) para as receitas, com filtro automático, estilo e expansão automática ao incluir novas linhas.
- **Formatação numérica personalizada**: CPF (`000.000.000-00`), CEP (`00000-000`), telefone e celular com DDD, título de eleitor em blocos de 4 dígitos, datas e moeda em R$ — o usuário digita só números e a máscara é aplicada.
- **Proteção de abas** para evitar alterações acidentais na estrutura.
- **Design próprio**: paleta escura com verde, identidade visual (logo e tipografia) e layout consistente nas três abas.

## 🚀 Como usar

1. Baixe o arquivo `.xlsx` e abra no Excel (versão desktop recomendada, para os botões de navegação funcionarem).
2. Navegue pelo menu lateral e preencha as abas na ordem.
3. Em **INFORMES**, escolha o banco na lista e anexe (referencie) o nome do PDF do informe.
4. Em **NOTAS**, lance cada receita recebida no ano.
5. Na hora de declarar, consulte a planilha como seu "dossiê" de dados.

## ⚠️ Observações

- Todos os dados presentes no arquivo são **fictícios**, apenas para demonstração.
- A planilha é um **organizador pessoal**: não transmite nem calcula a declaração, e não substitui o programa oficial da Receita Federal nem orientação contábil.
- Por conter dados pessoais, não compartilhe sua versão preenchida.

## 🛠️ Possíveis evoluções

- Total e subtotais por categoria na aba NOTAS (`SOMASE`).
- Resumo/painel com gráficos de receitas por mês.
- Abas para despesas dedutíveis (saúde, educação), bens e direitos, e dependentes.
- Alertas de campos obrigatórios não preenchidos (formatação condicional).

## 👤 Autor

**Rafael Moraes** — [LinkedIn](https://www.linkedin.com/in/moraesrafael/)
