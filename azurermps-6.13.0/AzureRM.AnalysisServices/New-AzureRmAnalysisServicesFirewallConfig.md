---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 2369720eb3a2df1e1c65df727cb02c1464ddc218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623946"
---
# <span data-ttu-id="102d2-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="102d2-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="102d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="102d2-102">SYNOPSIS</span></span>
<span data-ttu-id="102d2-103">建立新的 Analysis Services 防火牆配置</span><span class="sxs-lookup"><span data-stu-id="102d2-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="102d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="102d2-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="102d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="102d2-105">DESCRIPTION</span></span>
<span data-ttu-id="102d2-106">New-AzureRmAnalysisServicesFirewallConfig 會建立新的防火牆 config 物件</span><span class="sxs-lookup"><span data-stu-id="102d2-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="102d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="102d2-107">EXAMPLES</span></span>

### <span data-ttu-id="102d2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="102d2-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="102d2-109">建立具有兩個規則的防火牆 config 物件，同時啟用 Power BI 服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="102d2-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="102d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="102d2-110">PARAMETERS</span></span>

### <span data-ttu-id="102d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102d2-111">-DefaultProfile</span></span>
<span data-ttu-id="102d2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="102d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="102d2-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="102d2-113">-EnablePowerBIService</span></span>
<span data-ttu-id="102d2-114">指示防火牆是否允許 Power BI 存取的標誌</span><span class="sxs-lookup"><span data-stu-id="102d2-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="102d2-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="102d2-115">-FirewallRule</span></span>
<span data-ttu-id="102d2-116">防火牆規則清單</span><span class="sxs-lookup"><span data-stu-id="102d2-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102d2-117">CommonParameters</span></span>
<span data-ttu-id="102d2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="102d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102d2-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="102d2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102d2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="102d2-120">INPUTS</span></span>

### <span data-ttu-id="102d2-121">[System.object]。清單 ' 1 [AnalysisServices. PsAzureAnalysisServicesFirewallRule，AnalysisServices，版本 = 0.6.11.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="102d2-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.Commands.AnalysisServices, Version=0.6.11.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="102d2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="102d2-122">OUTPUTS</span></span>

### <span data-ttu-id="102d2-123">PsAzureAnalysisServicesFirewallConfig 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="102d2-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="102d2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="102d2-124">NOTES</span></span>

## <span data-ttu-id="102d2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="102d2-125">RELATED LINKS</span></span>

[<span data-ttu-id="102d2-126">新-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="102d2-126">New-AzureRmAnalysisServicesFirewallRule</span></span>](./New-AzureRmAnalysisServicesFirewallRule.md)
