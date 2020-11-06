---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452300"
---
# <span data-ttu-id="0efe1-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0efe1-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="0efe1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0efe1-102">SYNOPSIS</span></span>
<span data-ttu-id="0efe1-103">建立新的 Analysis Services 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="0efe1-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0efe1-104">句法</span><span class="sxs-lookup"><span data-stu-id="0efe1-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="0efe1-105">說明</span><span class="sxs-lookup"><span data-stu-id="0efe1-105">DESCRIPTION</span></span>
<span data-ttu-id="0efe1-106">New-AzureRmAnalysisServicesFirewallRule 會建立新的防火牆規則物件。</span><span class="sxs-lookup"><span data-stu-id="0efe1-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="0efe1-107">示例</span><span class="sxs-lookup"><span data-stu-id="0efe1-107">EXAMPLES</span></span>

### <span data-ttu-id="0efe1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0efe1-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="0efe1-109">建立名為 rule1 且起始範圍為0.0.0.0 且結束範圍255.255.255.255 的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="0efe1-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="0efe1-110">參數</span><span class="sxs-lookup"><span data-stu-id="0efe1-110">PARAMETERS</span></span>

### <span data-ttu-id="0efe1-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="0efe1-111">-FirewallRuleName</span></span>
<span data-ttu-id="0efe1-112">防火牆規則的名稱</span><span class="sxs-lookup"><span data-stu-id="0efe1-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0efe1-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="0efe1-113">-RangeStart</span></span>
<span data-ttu-id="0efe1-114">防火牆規則的範圍開始</span><span class="sxs-lookup"><span data-stu-id="0efe1-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0efe1-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="0efe1-115">-RangeEnd</span></span>
<span data-ttu-id="0efe1-116">防火牆規則的範圍結束</span><span class="sxs-lookup"><span data-stu-id="0efe1-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="0efe1-117">輸入</span><span class="sxs-lookup"><span data-stu-id="0efe1-117">INPUTS</span></span>

## <span data-ttu-id="0efe1-118">輸出</span><span class="sxs-lookup"><span data-stu-id="0efe1-118">OUTPUTS</span></span>

### <span data-ttu-id="0efe1-119">AzureAnalysisServicesFirewallRule 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="0efe1-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="0efe1-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="0efe1-120">RELATED LINKS</span></span>

[<span data-ttu-id="0efe1-121">新-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="0efe1-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
