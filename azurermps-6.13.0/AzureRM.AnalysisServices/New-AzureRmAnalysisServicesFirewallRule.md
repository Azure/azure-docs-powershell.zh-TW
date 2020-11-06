---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 2a47c97ea189d4064edae7a871e21465d866f1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448502"
---
# <span data-ttu-id="2c777-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2c777-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="2c777-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c777-102">SYNOPSIS</span></span>
<span data-ttu-id="2c777-103">建立新的 Analysis Services 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2c777-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c777-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c777-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String>
 [-RangeEnd] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c777-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c777-105">DESCRIPTION</span></span>
<span data-ttu-id="2c777-106">New-AzureRmAnalysisServicesFirewallRule 會建立新的防火牆規則物件。</span><span class="sxs-lookup"><span data-stu-id="2c777-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="2c777-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c777-107">EXAMPLES</span></span>

### <span data-ttu-id="2c777-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2c777-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="2c777-109">建立名為 rule1 且起始範圍為0.0.0.0 且結束範圍255.255.255.255 的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2c777-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="2c777-110">參數</span><span class="sxs-lookup"><span data-stu-id="2c777-110">PARAMETERS</span></span>

### <span data-ttu-id="2c777-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c777-111">-DefaultProfile</span></span>
<span data-ttu-id="2c777-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c777-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c777-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="2c777-113">-FirewallRuleName</span></span>
<span data-ttu-id="2c777-114">防火牆規則的名稱</span><span class="sxs-lookup"><span data-stu-id="2c777-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="2c777-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="2c777-115">-RangeEnd</span></span>
<span data-ttu-id="2c777-116">防火牆規則的範圍結束</span><span class="sxs-lookup"><span data-stu-id="2c777-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="2c777-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="2c777-117">-RangeStart</span></span>
<span data-ttu-id="2c777-118">防火牆規則的範圍開始</span><span class="sxs-lookup"><span data-stu-id="2c777-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="2c777-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c777-119">CommonParameters</span></span>
<span data-ttu-id="2c777-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c777-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c777-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c777-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c777-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2c777-122">INPUTS</span></span>

### <span data-ttu-id="2c777-123">System.object</span><span class="sxs-lookup"><span data-stu-id="2c777-123">System.String</span></span>

## <span data-ttu-id="2c777-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2c777-124">OUTPUTS</span></span>

### <span data-ttu-id="2c777-125">PsAzureAnalysisServicesFirewallRule 中的 AnalysisServices。</span><span class="sxs-lookup"><span data-stu-id="2c777-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="2c777-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2c777-126">NOTES</span></span>

## <span data-ttu-id="2c777-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c777-127">RELATED LINKS</span></span>

[<span data-ttu-id="2c777-128">新-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="2c777-128">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
