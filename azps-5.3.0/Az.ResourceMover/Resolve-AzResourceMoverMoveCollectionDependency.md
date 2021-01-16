---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435566"
---
# <span data-ttu-id="5290a-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="5290a-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="5290a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5290a-102">SYNOPSIS</span></span>
<span data-ttu-id="5290a-103">計算、解析並驗證移動集合中 moveResources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="5290a-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="5290a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5290a-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5290a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5290a-105">DESCRIPTION</span></span>
<span data-ttu-id="5290a-106">計算、解析並驗證移動集合中 moveResources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="5290a-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="5290a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5290a-107">EXAMPLES</span></span>

### <span data-ttu-id="5290a-108">範例1：計算、解析和驗證移動集合中 moveresources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="5290a-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="5290a-109">計算、解析並驗證移動集合中 moveresources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="5290a-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="5290a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5290a-110">PARAMETERS</span></span>

### <span data-ttu-id="5290a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5290a-111">-AsJob</span></span>
<span data-ttu-id="5290a-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="5290a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5290a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5290a-113">-DefaultProfile</span></span>
<span data-ttu-id="5290a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5290a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5290a-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="5290a-115">-MoveCollectionName</span></span>
<span data-ttu-id="5290a-116">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="5290a-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="5290a-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5290a-117">-NoWait</span></span>
<span data-ttu-id="5290a-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="5290a-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5290a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5290a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5290a-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5290a-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="5290a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5290a-121">-SubscriptionId</span></span>
<span data-ttu-id="5290a-122">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5290a-122">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5290a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="5290a-123">-Confirm</span></span>
<span data-ttu-id="5290a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5290a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5290a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5290a-125">-WhatIf</span></span>
<span data-ttu-id="5290a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5290a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5290a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5290a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5290a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5290a-128">CommonParameters</span></span>
<span data-ttu-id="5290a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5290a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5290a-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5290a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5290a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5290a-131">INPUTS</span></span>

## <span data-ttu-id="5290a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5290a-132">OUTPUTS</span></span>

### <span data-ttu-id="5290a-133">IOperationStatus （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="5290a-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="5290a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5290a-134">NOTES</span></span>

<span data-ttu-id="5290a-135">別名</span><span class="sxs-lookup"><span data-stu-id="5290a-135">ALIASES</span></span>

## <span data-ttu-id="5290a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5290a-136">RELATED LINKS</span></span>

