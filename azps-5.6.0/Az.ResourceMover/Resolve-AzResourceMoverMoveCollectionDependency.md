---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: 6812849fc8fe4aa8dab21f9bbcfc13891c45e0ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914417"
---
# <span data-ttu-id="c6298-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="c6298-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="c6298-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6298-102">SYNOPSIS</span></span>
<span data-ttu-id="c6298-103">計算、解決及驗證移動集合中 moveResources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="c6298-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="c6298-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6298-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c6298-105">描述</span><span class="sxs-lookup"><span data-stu-id="c6298-105">DESCRIPTION</span></span>
<span data-ttu-id="c6298-106">計算、解決及驗證移動集合中 moveResources 的相依性。</span><span class="sxs-lookup"><span data-stu-id="c6298-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="c6298-107">例子</span><span class="sxs-lookup"><span data-stu-id="c6298-107">EXAMPLES</span></span>

### <span data-ttu-id="c6298-108">範例 1：計算、解決及驗證 Move 集合中移動資源的相依性。</span><span class="sxs-lookup"><span data-stu-id="c6298-108">Example 1: Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 2/9/2021 2:05:04 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/c2ad006
                 6-6a69-45fe-aa70-193c240a9bc0
Message        : The resolve dependencies operation of one or more resources has failed. Check the move status of the resource for more details.
                     Possible Causes: The resolve dependencies operation of one ore more resources has failed.
                     Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : c2ad0066-6a69-45fe-aa70-193c240a9bc0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 2:05:00 AM
Status         : Succeeded
```

<span data-ttu-id="c6298-109">計算、解決及驗證 Move 集合中移動資源的相依性。</span><span class="sxs-lookup"><span data-stu-id="c6298-109">Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>

## <span data-ttu-id="c6298-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6298-110">PARAMETERS</span></span>

### <span data-ttu-id="c6298-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6298-111">-AsJob</span></span>
<span data-ttu-id="c6298-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="c6298-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c6298-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6298-113">-DefaultProfile</span></span>
<span data-ttu-id="c6298-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6298-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6298-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c6298-115">-MoveCollectionName</span></span>
<span data-ttu-id="c6298-116">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="c6298-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c6298-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c6298-117">-NoWait</span></span>
<span data-ttu-id="c6298-118">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="c6298-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c6298-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6298-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6298-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c6298-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c6298-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6298-121">-SubscriptionId</span></span>
<span data-ttu-id="c6298-122">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6298-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="c6298-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c6298-123">-Confirm</span></span>
<span data-ttu-id="c6298-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6298-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6298-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6298-125">-WhatIf</span></span>
<span data-ttu-id="c6298-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6298-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6298-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6298-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6298-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6298-128">CommonParameters</span></span>
<span data-ttu-id="c6298-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6298-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6298-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6298-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6298-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c6298-131">INPUTS</span></span>

## <span data-ttu-id="c6298-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c6298-132">OUTPUTS</span></span>

### <span data-ttu-id="c6298-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="c6298-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="c6298-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c6298-134">NOTES</span></span>

<span data-ttu-id="c6298-135">別名</span><span class="sxs-lookup"><span data-stu-id="c6298-135">ALIASES</span></span>

## <span data-ttu-id="c6298-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6298-136">RELATED LINKS</span></span>

