---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797897"
---
# <span data-ttu-id="ba6e8-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="ba6e8-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="ba6e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6e8-103">建立私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="ba6e8-103">create private link scope</span></span>

## <span data-ttu-id="ba6e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba6e8-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba6e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba6e8-105">DESCRIPTION</span></span>
<span data-ttu-id="ba6e8-106">建立私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="ba6e8-106">create private link scope</span></span>

## <span data-ttu-id="ba6e8-107">示例</span><span class="sxs-lookup"><span data-stu-id="ba6e8-107">EXAMPLES</span></span>

### <span data-ttu-id="ba6e8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ba6e8-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="ba6e8-109">在位置 "eastus" 的資源群組 "rg_name" 下，建立名為 "scope_name" 的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="ba6e8-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="ba6e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="ba6e8-110">PARAMETERS</span></span>

### <span data-ttu-id="ba6e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6e8-111">-DefaultProfile</span></span>
<span data-ttu-id="ba6e8-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba6e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba6e8-113">-位置</span><span class="sxs-lookup"><span data-stu-id="ba6e8-113">-Location</span></span>
<span data-ttu-id="ba6e8-114">位於</span><span class="sxs-lookup"><span data-stu-id="ba6e8-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba6e8-115">-Name</span></span>
<span data-ttu-id="ba6e8-116">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="ba6e8-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba6e8-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ba6e8-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e8-119">-標記</span><span class="sxs-lookup"><span data-stu-id="ba6e8-119">-Tags</span></span>
<span data-ttu-id="ba6e8-120">間</span><span class="sxs-lookup"><span data-stu-id="ba6e8-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e8-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ba6e8-121">-Confirm</span></span>
<span data-ttu-id="ba6e8-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba6e8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6e8-123">-WhatIf</span></span>
<span data-ttu-id="ba6e8-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba6e8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba6e8-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba6e8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6e8-126">CommonParameters</span></span>
<span data-ttu-id="ba6e8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba6e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6e8-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba6e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6e8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ba6e8-129">INPUTS</span></span>

### <span data-ttu-id="ba6e8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="ba6e8-130">System.String</span></span>

## <span data-ttu-id="ba6e8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ba6e8-131">OUTPUTS</span></span>

### <span data-ttu-id="ba6e8-132">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="ba6e8-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="ba6e8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ba6e8-133">NOTES</span></span>

## <span data-ttu-id="ba6e8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba6e8-134">RELATED LINKS</span></span>
