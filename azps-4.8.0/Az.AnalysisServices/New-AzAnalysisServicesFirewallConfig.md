---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129347"
---
# <span data-ttu-id="e6411-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e6411-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="e6411-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6411-102">SYNOPSIS</span></span>
<span data-ttu-id="e6411-103">建立新的 Analysis Services 防火牆配置</span><span class="sxs-lookup"><span data-stu-id="e6411-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="e6411-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6411-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6411-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6411-105">DESCRIPTION</span></span>
<span data-ttu-id="e6411-106">New-AzAnalysisServicesFirewallConfig 會建立新的防火牆 config 物件</span><span class="sxs-lookup"><span data-stu-id="e6411-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="e6411-107">示例</span><span class="sxs-lookup"><span data-stu-id="e6411-107">EXAMPLES</span></span>

### <span data-ttu-id="e6411-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e6411-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="e6411-109">建立具有兩個規則的防火牆 config 物件，同時啟用 Power BI 服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="e6411-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="e6411-110">參數</span><span class="sxs-lookup"><span data-stu-id="e6411-110">PARAMETERS</span></span>

### <span data-ttu-id="e6411-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6411-111">-DefaultProfile</span></span>
<span data-ttu-id="e6411-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6411-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6411-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="e6411-113">-EnablePowerBIService</span></span>
<span data-ttu-id="e6411-114">指示防火牆是否允許 Power BI 存取的標誌</span><span class="sxs-lookup"><span data-stu-id="e6411-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="e6411-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="e6411-115">-FirewallRule</span></span>
<span data-ttu-id="e6411-116">防火牆規則清單</span><span class="sxs-lookup"><span data-stu-id="e6411-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="e6411-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6411-117">CommonParameters</span></span>
<span data-ttu-id="e6411-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6411-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6411-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6411-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6411-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e6411-120">INPUTS</span></span>

### <span data-ttu-id="e6411-121">[System.object]. 清單 ' 1 [AnalysisServices. PsAzureAnalysisServicesFirewallRule，AnalysisServices，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="e6411-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6411-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e6411-122">OUTPUTS</span></span>

### <span data-ttu-id="e6411-123">PsAzureAnalysisServicesFirewallConfig 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="e6411-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="e6411-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e6411-124">NOTES</span></span>

## <span data-ttu-id="e6411-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6411-125">RELATED LINKS</span></span>

[<span data-ttu-id="e6411-126">新-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e6411-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)