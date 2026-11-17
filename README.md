# TorreCheck ⚡

**Aplicativo Android para organizar vistorias em linhas de transmissão de energia, com foco no trabalho em campo e no uso offline.**

> **Status:** MVP em desenvolvimento. Etapas 1 e 2 implementadas e validadas em um dispositivo Android real. **Código-fonte completo em preparação para publicação neste repositório.**

## O problema

Profissionais que inspecionam linhas de transmissão costumam registrar fotos da base de cada torre, do trecho anterior e do trecho seguinte, além de ocorrências como erosão, vegetação e dificuldades de acesso. Organizar essas imagens manualmente por cidade, linha e torre gera retrabalho.

## A solução

O **TorreCheck** organiza o fluxo **Cidade → Linha de transmissão → Torre → Vistoria**, com identificação livre das torres. O objetivo é registrar fotografias durante a inspeção e exportá-las posteriormente em pastas organizadas, sem renomear imagem por imagem.

A interface prioriza **botões grandes, alto contraste e funcionamento offline** para locais com conectividade limitada.

## O que já funciona

- Cadastro, edição e consulta de cidades;
- Linhas de transmissão vinculadas a cidades;
- Torres com identificação livre (ex.: `T-24A` e `Torre 24/A`);
- Prevenção de duplicidades e proteção de relacionamentos entre cadastros;
- Persistência de dados em SQLite, mesmo após fechar o aplicativo;
- Operação em modo avião e contadores de cadastros na tela inicial;
- Interface validada no Android real.

## Próximas entregas

- [x] **Etapa 1:** estrutura Flutter, interface e primeiro APK de desenvolvimento;
- [x] **Etapa 2:** cadastros offline com SQLite e testes;
- [ ] **Etapa 3:** câmera e fotos obrigatórias/extras por vistoria;
- [ ] **Etapa 4:** fluxo de inspeção e retomada de vistorias;
- [ ] **Etapa 5:** exportação ZIP por cidade, linha, torre e data;
- [ ] **Etapa 6:** testes finais e distribuição.

> **Importante:** captura de fotos, relatório e exportação ZIP são recursos planejados e **ainda não estão implementados**.

## Tecnologias

- **Flutter 3.50 / Dart 3.14**
- **Android**
- **SQLite** com `sqflite`
- **Riverpod** para gerenciamento de estado
- **Flutter Test** e `sqflite_common_ffi` para testes locais

## Validação

Na Etapa 2, o projeto passou por análise estática sem problemas, **47 testes automatizados aprovados** e testes reais no Xiaomi 12, incluindo criação de cadastros, validação de duplicidades, persistência e funcionamento offline.

## Privacidade

O repositório deve conter somente código-fonte e material demonstrativo. Dados de terceiros, fotos reais de inspeções, coordenadas sensíveis, arquivos de banco de dados e credenciais **não devem ser publicados**.

## Sobre o projeto

Projeto de portfólio criado a partir de uma necessidade real de trabalho de campo. Desenvolvimento com apoio de ferramentas de IA e validação manual no ambiente local.

---
**Em desenvolvimento.** O código-fonte completo e as instruções de execução serão adicionados após a conferência dos arquivos do projeto.
