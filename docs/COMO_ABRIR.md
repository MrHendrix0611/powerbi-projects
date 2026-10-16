# Guia de abertura dos relatórios

## Requisitos

- Windows com Power BI Desktop instalado.
- Para o projeto VAREON, uma versão atualizada do Power BI Desktop com suporte a **PBIP / PBIR / TMDL**.
- Espaço disponível para carregar os arquivos e atualizar as consultas.

## Arquivos do Power BI

| Projeto | Arquivo de abertura | Fonte disponível |
|---|---|---|
| ABC Equipamentos | `projetos/01-vendas-abc/Vendas.pbix` | Cinco arquivos CSV |
| Logística | `projetos/02-logistica/Logistica/Logistica.pbix` | CSV, Excel, JSON e XML |
| Crefisa | `projetos/03-credito-crefisa/Crefis14.pbix` | `BD/Base-Emp.xlsx` |
| VAREON | `projetos/04-vareon-intelligence-360/CommerceIntelligence360.pbip` | CSV e consultas do modelo semântico |

## Atualização de dados

Os relatórios PBIX podem preservar caminhos absolutos de arquivo da máquina onde foram criados. Após baixar o repositório, a abertura do `.pbix` pode funcionar com dados já carregados, mas a **atualização** poderá exigir reconfiguração das origens.

1. Abra o relatório no Power BI Desktop.
2. Acesse **Página Inicial → Transformar Dados → Configurações de Fonte de Dados**.
3. Utilize **Alterar Fonte** para selecionar as bases incluídas no respectivo projeto.
4. Clique em **Fechar e Aplicar** e depois em **Atualizar**.
5. Confira as medidas e visualizações.

**Observação:** a organização preserva os arquivos originais de dados e de relatório. Uma alteração de pasta após a extração não muda automaticamente caminhos absolutos salvos internamente no PBIX. No projeto PBIP, mantenha as pastas `Report` e `SemanticModel` lado a lado, conforme entregues.

## Publicação no GitHub

Depois de extrair a pasta `powerbi-projects`, crie um repositório vazio com esse nome e execute os comandos abaixo em um terminal aberto na raiz da pasta:

```powershell
git init
git branch -M main
git add .
git commit -m "feat: adiciona projetos Power BI SENAI"
git remote add origin https://github.com/SEU_USUARIO/powerbi-projects.git
git push -u origin main
```

Os arquivos `.pbix` e `.pbip` devem ser abertos no Power BI Desktop, e não diretamente no visualizador do GitHub.
