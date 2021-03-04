---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 4936571126a00d34fc91d2f7cbd85b232f18b4fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914202"
---
# <span data-ttu-id="6ba4e-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6ba4e-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="6ba4e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ba4e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba4e-103">建立新的 Analysis Services 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="6ba4e-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="6ba4e-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ba4e-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ba4e-105">描述</span><span class="sxs-lookup"><span data-stu-id="6ba4e-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba4e-106">此New-AzAnalysisServicesFirewallRule會建立一個新的防火牆規則物件。</span><span class="sxs-lookup"><span data-stu-id="6ba4e-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="6ba4e-107">例子</span><span class="sxs-lookup"><span data-stu-id="6ba4e-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba4e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6ba4e-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="6ba4e-109">建立名為 rule1 的防火牆規則，其起始範圍為 0.0.0.0，結尾範圍為 255.255.255.255。</span><span class="sxs-lookup"><span data-stu-id="6ba4e-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="6ba4e-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ba4e-110">PARAMETERS</span></span>

### <span data-ttu-id="6ba4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba4e-111">-DefaultProfile</span></span>
<span data-ttu-id="6ba4e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ba4e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba4e-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="6ba4e-113">-FirewallRuleName</span></span>
<span data-ttu-id="6ba4e-114">防火牆規則的名稱</span><span class="sxs-lookup"><span data-stu-id="6ba4e-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba4e-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="6ba4e-115">-RangeEnd</span></span>
<span data-ttu-id="6ba4e-116">防火牆規則的範圍結尾</span><span class="sxs-lookup"><span data-stu-id="6ba4e-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba4e-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="6ba4e-117">-RangeStart</span></span>
<span data-ttu-id="6ba4e-118">防火牆規則的範圍開始</span><span class="sxs-lookup"><span data-stu-id="6ba4e-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba4e-119">CommonParameters</span></span>
<span data-ttu-id="6ba4e-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ba4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba4e-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6ba4e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba4e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6ba4e-122">INPUTS</span></span>

### <span data-ttu-id="6ba4e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6ba4e-123">System.String</span></span>

## <span data-ttu-id="6ba4e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6ba4e-124">OUTPUTS</span></span>

### <span data-ttu-id="6ba4e-125">Microsoft.Azure.Commands.AnalysisServices.models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6ba4e-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="6ba4e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6ba4e-126">NOTES</span></span>

## <span data-ttu-id="6ba4e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ba4e-127">RELATED LINKS</span></span>

[<span data-ttu-id="6ba4e-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="6ba4e-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)