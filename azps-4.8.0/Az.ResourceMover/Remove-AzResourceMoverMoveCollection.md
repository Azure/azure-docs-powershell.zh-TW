---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135453"
---
# <span data-ttu-id="e4924-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="e4924-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="e4924-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4924-102">SYNOPSIS</span></span>
<span data-ttu-id="e4924-103">刪除移動收藏。</span><span class="sxs-lookup"><span data-stu-id="e4924-103">Deletes a move collection.</span></span>

## <span data-ttu-id="e4924-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4924-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4924-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4924-105">DESCRIPTION</span></span>
<span data-ttu-id="e4924-106">刪除移動收藏。</span><span class="sxs-lookup"><span data-stu-id="e4924-106">Deletes a move collection.</span></span>

## <span data-ttu-id="e4924-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4924-107">EXAMPLES</span></span>

### <span data-ttu-id="e4924-108">範例1：從指定的訂閱移除移動集合</span><span class="sxs-lookup"><span data-stu-id="e4924-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="e4924-109">從指定的訂閱中移除移動集合。</span><span class="sxs-lookup"><span data-stu-id="e4924-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="e4924-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4924-110">PARAMETERS</span></span>

### <span data-ttu-id="e4924-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4924-111">-AsJob</span></span>
<span data-ttu-id="e4924-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="e4924-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e4924-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4924-113">-DefaultProfile</span></span>
<span data-ttu-id="e4924-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4924-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4924-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4924-115">-Name</span></span>
<span data-ttu-id="e4924-116">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="e4924-116">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4924-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e4924-117">-NoWait</span></span>
<span data-ttu-id="e4924-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="e4924-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4924-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4924-119">-PassThru</span></span>
<span data-ttu-id="e4924-120">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="e4924-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4924-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4924-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4924-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4924-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="e4924-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4924-123">-SubscriptionId</span></span>
<span data-ttu-id="e4924-124">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="e4924-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="e4924-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e4924-125">-Confirm</span></span>
<span data-ttu-id="e4924-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4924-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4924-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4924-127">-WhatIf</span></span>
<span data-ttu-id="e4924-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4924-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4924-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4924-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4924-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4924-130">CommonParameters</span></span>
<span data-ttu-id="e4924-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4924-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4924-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e4924-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4924-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e4924-133">INPUTS</span></span>

## <span data-ttu-id="e4924-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e4924-134">OUTPUTS</span></span>

### <span data-ttu-id="e4924-135">IOperationStatus （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="e4924-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="e4924-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e4924-136">NOTES</span></span>

<span data-ttu-id="e4924-137">別名</span><span class="sxs-lookup"><span data-stu-id="e4924-137">ALIASES</span></span>

## <span data-ttu-id="e4924-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4924-138">RELATED LINKS</span></span>
