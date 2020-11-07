---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624738"
---
# <span data-ttu-id="73761-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="73761-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="73761-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73761-102">SYNOPSIS</span></span>
<span data-ttu-id="73761-103">建立新的 Analysis Services 防火牆配置</span><span class="sxs-lookup"><span data-stu-id="73761-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73761-104">句法</span><span class="sxs-lookup"><span data-stu-id="73761-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## <span data-ttu-id="73761-105">說明</span><span class="sxs-lookup"><span data-stu-id="73761-105">DESCRIPTION</span></span>
<span data-ttu-id="73761-106">New-AzureRmAnalysisServicesFirewallConfig 會建立新的防火牆 config 物件</span><span class="sxs-lookup"><span data-stu-id="73761-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="73761-107">示例</span><span class="sxs-lookup"><span data-stu-id="73761-107">EXAMPLES</span></span>

### <span data-ttu-id="73761-108">範例1</span><span class="sxs-lookup"><span data-stu-id="73761-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

<span data-ttu-id="73761-109">建立防火牆規則 config，但不啟用 power bi 服務。</span><span class="sxs-lookup"><span data-stu-id="73761-109">Creates a firewall rule config without enabling power bi service.</span></span>

## <span data-ttu-id="73761-110">參數</span><span class="sxs-lookup"><span data-stu-id="73761-110">PARAMETERS</span></span>

### <span data-ttu-id="73761-111">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="73761-111">-EnablePowerBIService</span></span>
<span data-ttu-id="73761-112">指示是否啟用 PowerBI 服務的標誌</span><span class="sxs-lookup"><span data-stu-id="73761-112">A flag to indicate if enable PowerBI service</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73761-113">-FirewallRules</span><span class="sxs-lookup"><span data-stu-id="73761-113">-FirewallRules</span></span>
<span data-ttu-id="73761-114">防火牆規則清單</span><span class="sxs-lookup"><span data-stu-id="73761-114">A list of firewall rules</span></span>

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="73761-115">輸入</span><span class="sxs-lookup"><span data-stu-id="73761-115">INPUTS</span></span>

## <span data-ttu-id="73761-116">輸出</span><span class="sxs-lookup"><span data-stu-id="73761-116">OUTPUTS</span></span>

### <span data-ttu-id="73761-117">AzureAnalysisServicesFirewallConfig 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="73761-117">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="73761-118">相關連結</span><span class="sxs-lookup"><span data-stu-id="73761-118">RELATED LINKS</span></span>

[<span data-ttu-id="73761-119">新-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="73761-119">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
