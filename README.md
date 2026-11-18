# TorreCheck ⚡

**Aplicativo Android para organizar vistorias em linhas de transmissão de energia, com foco no trabalho em campo e no uso offline.**

> **Status:** MVP em desenvolvimento. Etapas 1, 2 e 3 implementadas e validadas em um dispositivo Android real. **Código-fonte completo em preparação para publicação neste repositório.**

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
- Interface validada no Android real;
- Criação de vistorias vinculadas às torres;
- Câmera integrada e três fotografias obrigatórias por vistoria;
- Fotos extras por categoria de ocorrência;
- Visualização, substituição e exclusão de fotos;
- Armazenamento privado de imagens e persistência offline;
- Migração SQLite v1 → v2 preservando os cadastros.

## Próximas entregas

- [x] **Etapa 1:** estrutura Flutter, interface e primeiro APK de desenvolvimento;
- [x] **Etapa 2:** cadastros offline com SQLite e testes;
- [x] **Etapa 3:** câmera e fotos obrigatórias/extras por vistoria, com correção 3.1 validada;
- [ ] **Etapa 4:** fluxo de inspeção e retomada de vistorias;
- [ ] **Etapa 5:** exportação ZIP por cidade, linha, torre e data;
- [ ] **Etapa 6:** testes finais e distribuição.

> **Importante:** a captura e a organização interna de fotos já funcionam. A conclusão de vistorias, a geração de relatórios e a exportação ZIP ainda não estão implementadas.

## Tecnologias

- **Flutter 3.50 / Dart 3.14**
- **Android**
- **SQLite** com `sqflite`
- **Riverpod** para gerenciamento de estado
- **Camera/CameraX** e **path_provider** para captura e armazenamento local
- **Flutter Test** e `sqflite_common_ffi` para testes locais

## Validação

Em 18/11/2026, após a correção 3.1, o projeto passou por análise estática sem problemas e **100 testes automatizados aprovados no Windows 10**. No Xiaomi 12 (Android 15), **11 verificações práticas aprovadas**, incluindo preservação dos cadastros após migração, captura das três imagens obrigatórias, fotos extras, substituição, exclusão, persistência após reabrir e funcionamento em modo avião.

Testes complementares de interrupção da câmera, permissão negada e reinicialização do celular ainda fazem parte da validação final.

## Privacidade

O repositório deve conter somente código-fonte e material demonstrativo. Dados de terceiros, fotos reais de inspeções, coordenadas sensíveis, arquivos de banco de dados e credenciais **não devem ser publicados**.

## Sobre o projeto

Projeto de portfólio criado a partir de uma necessidade real de trabalho de campo. Desenvolvimento com apoio de ferramentas de IA e validação manual no ambiente local.

---
**Em desenvolvimento.** O código-fonte completo e as instruções de execução serão adicionados após a conferência dos arquivos do projeto.
