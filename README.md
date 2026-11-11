# 🦁 Leão App — Planilha de Organização para o Imposto de Renda

Projeto de portfólio: demonstra como transformar uma planilha comum em uma pequena **aplicação** com navegação, validação de dados e interface própria, usando apenas recursos nativos do Excel (sem macros).

---

## 📌 O problema

A ideia desta planilha é **centralizar e padronizar** informações pessoais e financeiras como CPF, informes de rendimento, saldos e receitas ao longo do ano, para que a declaração seja só consultar e copiar.

## 🧭 Como funciona

A planilha tem três abas de preenchimento, organizadas como um fluxo guiado:

- **1 · TITULAR**
Cadastro do contribuinte: nome, CPF, nascimento, título de eleitor, cônjuge, endereço, contatos e perguntas de triagem (houve alterações desde a última entrega? cônjuge dependente? reside no exterior?).
<img alt="previa" src="https://github.com/jogaaivei/Leao-App-Planilha-de-Organizacao-para-o-Imposto-de-Renda/blob/main/images/titular.png" />

- **2 · INFORMES**
Informes de rendimentos bancários: para cada banco, instituição (lista suspensa), valor atual e nome do arquivo anexo (PDF do informe). Calcula automaticamente o **total** de patrimônio informado.
<img alt="previa" src="https://github.com/jogaaivei/Leao-App-Planilha-de-Organizacao-para-o-Imposto-de-Renda/blob/main/images/informes.png" />

- **3 · NOTAS**
Tabela de entradas mês a mês: data, categoria (Holerite, CNPJ ou Freelance) e valor, com filtros e linhas zebradas.
<img alt="previa" src="https://github.com/jogaaivei/Leao-App-Planilha-de-Organizacao-para-o-Imposto-de-Renda/blob/main/images/notas.png" />

## ✨ Recursos de Excel utilizados

- **Navegação por botões**: menu lateral com botões clicáveis (formas com hiperlinks internos) para alternar entre as abas, mais botão "Próximo". Funciona como uma interface de app.
- **Validação de dados com listas suspensas**
  - Lista de bancos com código e nome, alimentada por uma **aba oculta (`BANCOS`)** como base de dados.
  - Respostas `SIM`/`NÃO` nas perguntas de triagem.
  - Categorias de receita (`HOLERITE`, `CNPJ`, `FREELANCE`).
- **Fórmulas**: `SOMA` consolidando os valores dos bancos no total de patrimônio.
- **Tabela estruturada do Excel** (`Tabela2`) para as receitas, com filtro automático, estilo e expansão automática ao incluir novas linhas.
- **Formatação numérica personalizada**: CPF (`000.000.000-00`), CEP (`00000-000`), telefone e celular com DDD, título de eleitor em blocos de 4 dígitos, datas e moeda em R$ — o usuário digita só números e a máscara é aplicada.
- **Proteção de abas** para evitar alterações acidentais na estrutura.
- **Design próprio**: paleta escura com verde, identidade visual (logo e tipografia) e layout consistente nas três abas.

## 🚀 Como usar

1. Baixe o arquivo `.xlsx` e abra no Excel (versão 2007 mais atual recomendada para fins de compatibilidade).
2. Navegue pelo menu lateral e preencha as abas na ordem.
3. Em **INFORMES**, escolha o banco na lista e anexe (referencie) o nome do PDF do informe.
4. Em **NOTAS**, lance cada receita recebida no ano.
5. Na hora de declarar, consulte a planilha como seu "dossiê" de dados.

## ⚠️ Observações

- Todos os dados presentes no arquivo são **fictícios**, apenas para demonstração.
- A planilha é um **organizador pessoal**: não transmite nem calcula a declaração, e não substitui o programa oficial da Receita Federal nem orientação contábil.
- Por conter dados pessoais, não compartilhe sua versão preenchida.

## 👤 Autor

**Rafael Moraes** — [LinkedIn](https://www.linkedin.com/in/moraesrafael/)
