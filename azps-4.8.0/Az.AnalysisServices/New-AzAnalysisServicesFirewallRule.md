---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971347"
---
# <span data-ttu-id="d2f89-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d2f89-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="d2f89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2f89-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f89-103">建立新的 Analysis Services 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="d2f89-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="d2f89-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2f89-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2f89-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2f89-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f89-106">New-AzAnalysisServicesFirewallRule 會建立新的防火牆規則物件。</span><span class="sxs-lookup"><span data-stu-id="d2f89-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="d2f89-107">示例</span><span class="sxs-lookup"><span data-stu-id="d2f89-107">EXAMPLES</span></span>

### <span data-ttu-id="d2f89-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d2f89-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="d2f89-109">建立名為 rule1 且起始範圍為0.0.0.0 且結束範圍255.255.255.255 的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="d2f89-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="d2f89-110">參數</span><span class="sxs-lookup"><span data-stu-id="d2f89-110">PARAMETERS</span></span>

### <span data-ttu-id="d2f89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f89-111">-DefaultProfile</span></span>
<span data-ttu-id="d2f89-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2f89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f89-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="d2f89-113">-FirewallRuleName</span></span>
<span data-ttu-id="d2f89-114">防火牆規則的名稱</span><span class="sxs-lookup"><span data-stu-id="d2f89-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="d2f89-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="d2f89-115">-RangeEnd</span></span>
<span data-ttu-id="d2f89-116">防火牆規則的範圍結束</span><span class="sxs-lookup"><span data-stu-id="d2f89-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="d2f89-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="d2f89-117">-RangeStart</span></span>
<span data-ttu-id="d2f89-118">防火牆規則的範圍開始</span><span class="sxs-lookup"><span data-stu-id="d2f89-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="d2f89-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f89-119">CommonParameters</span></span>
<span data-ttu-id="d2f89-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2f89-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f89-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2f89-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f89-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d2f89-122">INPUTS</span></span>

### <span data-ttu-id="d2f89-123">System.object</span><span class="sxs-lookup"><span data-stu-id="d2f89-123">System.String</span></span>

## <span data-ttu-id="d2f89-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d2f89-124">OUTPUTS</span></span>

### <span data-ttu-id="d2f89-125">PsAzureAnalysisServicesFirewallRule 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="d2f89-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="d2f89-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d2f89-126">NOTES</span></span>

## <span data-ttu-id="d2f89-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2f89-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2f89-128">新-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d2f89-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)