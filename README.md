# Sistema de Controle Financeiro Pessoal

## Descrição do Projeto
Este é um Sistema de Controle Financeiro Pessoal desenvolvido em .NET Core. O sistema permite que o usuário registre receitas, despesas, visualize gráficos de fluxo de caixa e gere relatórios financeiros mensais. 

### Funcionalidades Principais:
- **Cadastro de Receitas e Despesas**: Registre transações financeiras com informações detalhadas.
- **Categorização de Transações**: Categorize despesas e receitas por tipo (alimentação, transporte, etc.).
- **Gráficos de Fluxo de Caixa**: Visualize gráficos dinâmicos das entradas e saídas financeiras.
- **Relatórios Financeiros Mensais**: Gere relatórios mensais com o saldo final e resumo de transações.

---

## Estrutura do Projeto

### Camadas do Sistema:

1. **API (Back-end)**: 
   - Desenvolvida em ASP.NET Core como uma API RESTful para gerenciar as transações financeiras.
   - Utiliza **Entity Framework Core** para interação com o banco de dados SQL Server.

2. **Banco de Dados**:
   - Utiliza **SQL Server** para armazenar as transações (receitas e despesas) e outras informações relevantes.

3. **Interface Front-end (opcional)**: 
   - Pode ser feita com **Blazor**, **Razor Pages**, ou uma aplicação web com **React** ou **Angular** que consuma a API.

4. **Relatórios e Gráficos**:
   - Geração de relatórios financeiros em PDF ou Excel.
   - Visualização de gráficos dinâmicos com **Chart.js**.

---

## API: Estrutura e Endpoints

### Modelo de Dados (Transação)

```csharp
public class Transacao
{
    public int Id { get; set; }
    public string Tipo { get; set; }  // Receita ou Despesa
    public string Categoria { get; set; }  // Exemplo: Alimentação, Transporte
    public decimal Valor { get; set; }
    public DateTime Data { get; set; }
    public string Descricao { get; set; }
}
