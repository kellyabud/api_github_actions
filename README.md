# Teste de API com Postman e Newman

Este repositório contém coleções de testes e scripts para automatizar testes de API usando o Postman e o Newman.

## Pré-requisitos

- [Postman](https://www.postman.com/downloads/)
- [Newman](https://www.npmjs.com/package/newman)

## Instalação

1. Instale o Postman baixando-o do [site oficial](https://www.postman.com/downloads/).

2. Instale o Newman globalmente usando o npm:

   ```bash
   npm install -g newman

3. Exporte do Postman a coleção e ambiente.

4. Abra o terminal e navegue até o diretório do projeto.
- Execute o seguinte comando para executar os testes:
newman run ./collections/sua_colecao.json -e ./environments/seu_ambiente.json
- Substitua sua_colecao.json e seu_ambiente.json pelos nomes de arquivo apropriados.

5. Relatórios com Newman
- O Newman gera relatórios que podem ser salvos ou integrados ao seu pipeline de CI/CD. Os relatórios podem ser encontrados no diretório ./reports.
Para baixar o reporter HTML Extra (htlmlextra) para Newman, você precisa instalá-lo como uma dependência global do Newman usando o npm. 
#Execute o seguinte comando no terminal para fazer o download do reporter HTML Extra:
npm install -g newman-reporter-htmlextra
- Gerar relatório:
newman run ./collections/sua_colecao.json -e ./environments/seu_ambiente.json -r htmlextra --reporter-htmlextra-displayProgressBar
Substitua sua_colecao.json e seu_ambiente.json pelos nomes de arquivo apropriados.

6. Mudando o título do relatório
- Para mudar o título do relatório gerado pelo reporter HTML Extra (htmlextra) no Newman, você pode usar o comando:
newman run collection.json -e environment.json --reporters htmlextra --reporter-htmlextra-title "Título do Relatório"
Substitua sua_colecao.json e seu_ambiente.json pelos nomes de arquivo apropriados.










