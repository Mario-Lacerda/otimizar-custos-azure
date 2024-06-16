# Desafio Dio - Otimizando Custos no Azure



####     Projeto ainda mais completo e abrangente com mais códigos para: **Otimizando Custos no Azure**

**Introdução**

Este projeto irá guiá-lo pelos fundamentos da otimização de custos no Microsoft Azure, uma plataforma de computação em nuvem que oferece uma ampla gama de serviços para ajudá-lo a construir, implantar e gerenciar seus aplicativos de forma econômica.



### **Pré-requisitos**

- Uma conta do Microsoft Azure
- O Visual Studio 2019 ou superior
- O .NET Core SDK 3.1 ou superior



### **Instruções**

1. **Crie um novo projeto do Visual Studio.**

2. **Selecione o modelo "Aplicativo Web do ASP.NET Core".**

3. **Nomeie o projeto como "AzureCostOptimizationInAction".**

4. **Clique em "Criar".**

   

5. #### Adicione os seguintes pacotes NuGet ao projeto:

   - Microsoft.Azure.Management.CostManagement

     

6. #### Adicione as seguintes classes ao projeto:

   

   - **CostManagementService.cs:** Esta classe fornece métodos para interagir com o serviço de gerenciamento de custos do Azure.

     

7. **Adicione o seguinte código ao arquivo "Startup.cs":**

   

csharp



```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddSingleton<ICostManagementService, CostManagementService>();
}
```



1. #### **Adicione o seguinte código ao arquivo "Controllers/HomeController.cs":**

   

csharp



```csharp
public class HomeController : Controller
{
    private readonly ICostManagementService _costManagementService;

    public HomeController(ICostManagementService costManagementService)
    {
        _costManagementService = costManagementService;
    }

    public IActionResult Index()
    {
        return View();
    }

    [HttpPost]
    public async Task<IActionResult> GetCostAnalysis(string scope, string startDate, string endDate)
    {
        var costAnalysis = await _costManagementService.GetCostAnalysisAsync(scope, startDate, endDate);

        return View("CostAnalysis", costAnalysis);
    }
}
```



1. **Execute o projeto.**

   

## **Conclusão**



Este projeto fornece uma base ainda mais sólida para você começar a otimizar custos na nuvem no Microsoft Azure. Você pode usar o serviço de gerenciamento de custos para analisar seus gastos, identificar áreas de otimização e tomar medidas para reduzir seus custos.

