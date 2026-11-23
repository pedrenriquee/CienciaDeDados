# Como executar o projeto no Power BI

## Pré-requisitos

Para executar o projeto, é necessário ter:

- Power BI Desktop instalado.
- Microsoft Windows.
- Os dois arquivos disponíveis neste repositório.

O Power BI Desktop pode ser obtido no [site oficial da Microsoft](https://www.microsoft.com/power-platform/products/power-bi/desktop).

## Tutorial — Como executar o projeto

### 1. Baixar os arquivos

Acesse a pasta do projeto no GitHub:

[ProjetoA1 — Ciência de Dados](https://github.com/pedrenriquee/CienciaDeDados/tree/main/ProjetoA1)

Baixe os arquivos `ABVE_Eletrificados.pbix` e `base_abve_nacional_2022_2026.xlsx`.

Também é possível baixar o repositório completo utilizando a opção **Code → Download ZIP** na página principal do repositório.

### 2. Organizar os arquivos no computador

Crie uma pasta no disco local com o seguinte caminho:

```text
C:\PowerBI\ProjetoA1
```

Coloque os dois arquivos dentro dessa pasta, mantendo a seguinte organização:

```text
C:\PowerBI\ProjetoA1\
│
├── ABVE_Eletrificados.pbix
└── base_abve_nacional_2022_2026.xlsx
```

Esse será o caminho de referência utilizado nas próximas etapas.

### 3. Abrir o relatório no Power BI

1. Abra o Power BI Desktop.
2. Selecione **Arquivo → Abrir**.
3. Navegue até `C:\PowerBI\ProjetoA1`.
4. Abra o arquivo `ABVE_Eletrificados.pbix`.

O relatório poderá apresentar os dados anteriormente importados, mas a conexão com o Excel precisará ser ajustada para permitir a atualização.

### 4. Configurar a base de dados no Power Query

Como o relatório foi desenvolvido utilizando um arquivo Excel local, a origem dos dados pode estar vinculada ao caminho utilizado no computador original.

Para alterar essa configuração:

1. No Power BI Desktop, clique em **Transformar dados**.
2. No Editor do Power Query, selecione a consulta responsável por importar a base Excel.
3. No painel **Etapas Aplicadas**, localize a etapa **Fonte**.
4. Clique no ícone de engrenagem ao lado da etapa, caso esteja disponível.
5. Altere o caminho do arquivo para:

   ```text
   C:\PowerBI\ProjetoA1\base_abve_nacional_2022_2026.xlsx
   ```

6. Confirme a alteração.

**Alternativa — Editor Avançado**

Se não for possível alterar o caminho pela engrenagem:

1. Selecione a consulta correspondente ao Excel.
2. Clique em **Editor Avançado**.
3. Localize a expressão `File.Contents`, responsável por indicar o arquivo de origem.

Um exemplo de conexão é:

```powerquery
Fonte = Excel.Workbook(
    File.Contents("C:\PowerBI\ProjetoA1\base_abve_nacional_2022_2026.xlsx"),
    null,
    true
)
```

Substitua somente o caminho dentro de `File.Contents`, preservando as demais etapas e transformações existentes na consulta.

**Importante:** caso existam outras consultas que utilizem diretamente o arquivo Excel, verifique se todas apontam para o novo caminho.

### 5. Aplicar as alterações e atualizar o relatório

Após configurar a origem:

1. Clique em **Fechar e Aplicar** no Editor do Power Query.
2. Aguarde o processamento das consultas.
3. Na tela principal do Power BI Desktop, clique em **Atualizar**.
4. Aguarde a conclusão do carregamento.
5. Verifique se as visualizações foram carregadas corretamente.

Caso seja solicitada autenticação para o arquivo local, selecione o método apropriado, normalmente **Anônimo**, para um arquivo Excel local sem autenticação adicional.
