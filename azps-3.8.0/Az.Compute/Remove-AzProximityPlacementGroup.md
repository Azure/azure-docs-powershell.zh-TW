---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799273"
---
# <span data-ttu-id="247c5-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="247c5-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="247c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="247c5-102">SYNOPSIS</span></span>
<span data-ttu-id="247c5-103">刪除鄰近性位置群組資源。</span><span class="sxs-lookup"><span data-stu-id="247c5-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="247c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="247c5-104">SYNTAX</span></span>

### <span data-ttu-id="247c5-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="247c5-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="247c5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="247c5-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="247c5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="247c5-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="247c5-108">說明</span><span class="sxs-lookup"><span data-stu-id="247c5-108">DESCRIPTION</span></span>
<span data-ttu-id="247c5-109">這個 Cmdlet 會刪除 [鄰近性位置] 群組資源。</span><span class="sxs-lookup"><span data-stu-id="247c5-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="247c5-110">示例</span><span class="sxs-lookup"><span data-stu-id="247c5-110">EXAMPLES</span></span>

### <span data-ttu-id="247c5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="247c5-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="247c5-112">這個命令會移除指定的鄰近性位置群組。</span><span class="sxs-lookup"><span data-stu-id="247c5-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="247c5-113">參數</span><span class="sxs-lookup"><span data-stu-id="247c5-113">PARAMETERS</span></span>

### <span data-ttu-id="247c5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="247c5-114">-AsJob</span></span>
<span data-ttu-id="247c5-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="247c5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="247c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247c5-116">-DefaultProfile</span></span>
<span data-ttu-id="247c5-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="247c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="247c5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="247c5-118">-Force</span></span>
<span data-ttu-id="247c5-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="247c5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="247c5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="247c5-120">-InputObject</span></span>
<span data-ttu-id="247c5-121">PS 鄰近性位置群組物件</span><span class="sxs-lookup"><span data-stu-id="247c5-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="247c5-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="247c5-122">-Name</span></span>
<span data-ttu-id="247c5-123">鄰近性位置群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="247c5-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="247c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="247c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="247c5-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="247c5-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="247c5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="247c5-126">-ResourceId</span></span>
<span data-ttu-id="247c5-127">[鄰近性位置] 群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="247c5-127">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="247c5-128">-確認</span><span class="sxs-lookup"><span data-stu-id="247c5-128">-Confirm</span></span>
<span data-ttu-id="247c5-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="247c5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247c5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247c5-130">-WhatIf</span></span>
<span data-ttu-id="247c5-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="247c5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247c5-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="247c5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247c5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247c5-133">CommonParameters</span></span>
<span data-ttu-id="247c5-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="247c5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247c5-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="247c5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247c5-136">輸入</span><span class="sxs-lookup"><span data-stu-id="247c5-136">INPUTS</span></span>

### <span data-ttu-id="247c5-137">System.object</span><span class="sxs-lookup"><span data-stu-id="247c5-137">System.String</span></span>

### <span data-ttu-id="247c5-138">PSProximityPlacementGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="247c5-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="247c5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="247c5-139">OUTPUTS</span></span>

### <span data-ttu-id="247c5-140">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="247c5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="247c5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="247c5-141">NOTES</span></span>

## <span data-ttu-id="247c5-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="247c5-142">RELATED LINKS</span></span>
