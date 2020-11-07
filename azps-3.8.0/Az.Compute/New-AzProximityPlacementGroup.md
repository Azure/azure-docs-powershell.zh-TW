---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: cf8c4867fcc623065cce73fa392cb78d513200fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957394"
---
# <span data-ttu-id="b39a4-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="b39a4-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="b39a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b39a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b39a4-103">建立鄰近性位置群組資源。</span><span class="sxs-lookup"><span data-stu-id="b39a4-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="b39a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b39a4-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b39a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="b39a4-105">DESCRIPTION</span></span>
<span data-ttu-id="b39a4-106">這個 Cmdlet 會建立鄰近性位置群組資源。</span><span class="sxs-lookup"><span data-stu-id="b39a4-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="b39a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="b39a4-107">EXAMPLES</span></span>

### <span data-ttu-id="b39a4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b39a4-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="b39a4-109">這個命令會在指定的位置建立鄰近性位置群組。</span><span class="sxs-lookup"><span data-stu-id="b39a4-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="b39a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="b39a4-110">PARAMETERS</span></span>

### <span data-ttu-id="b39a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b39a4-111">-AsJob</span></span>
<span data-ttu-id="b39a4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b39a4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b39a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39a4-113">-DefaultProfile</span></span>
<span data-ttu-id="b39a4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b39a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b39a4-115">-位置</span><span class="sxs-lookup"><span data-stu-id="b39a4-115">-Location</span></span>
<span data-ttu-id="b39a4-116">資源位置</span><span class="sxs-lookup"><span data-stu-id="b39a4-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39a4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b39a4-117">-Name</span></span>
<span data-ttu-id="b39a4-118">鄰近性位置群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b39a4-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b39a4-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="b39a4-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="b39a4-120">指定鄰近性位置群組的類型。</span><span class="sxs-lookup"><span data-stu-id="b39a4-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="b39a4-121">可能的值包括：標準或超</span><span class="sxs-lookup"><span data-stu-id="b39a4-121">Possible values are: Standard or Ultra</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b39a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="b39a4-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b39a4-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="b39a4-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="b39a4-124">-Tag</span></span>
<span data-ttu-id="b39a4-125">資源標記</span><span class="sxs-lookup"><span data-stu-id="b39a4-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39a4-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b39a4-126">-Confirm</span></span>
<span data-ttu-id="b39a4-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b39a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b39a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b39a4-128">-WhatIf</span></span>
<span data-ttu-id="b39a4-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b39a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b39a4-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b39a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b39a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39a4-131">CommonParameters</span></span>
<span data-ttu-id="b39a4-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b39a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39a4-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b39a4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39a4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b39a4-134">INPUTS</span></span>

### <span data-ttu-id="b39a4-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b39a4-135">System.String</span></span>

## <span data-ttu-id="b39a4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b39a4-136">OUTPUTS</span></span>

### <span data-ttu-id="b39a4-137">PSProximityPlacementGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b39a4-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="b39a4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b39a4-138">NOTES</span></span>

## <span data-ttu-id="b39a4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b39a4-139">RELATED LINKS</span></span>
