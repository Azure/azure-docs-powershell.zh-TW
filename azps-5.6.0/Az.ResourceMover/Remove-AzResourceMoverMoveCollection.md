---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914425"
---
# <span data-ttu-id="2a422-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="2a422-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="2a422-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2a422-102">SYNOPSIS</span></span>
<span data-ttu-id="2a422-103">刪除移動集合。</span><span class="sxs-lookup"><span data-stu-id="2a422-103">Deletes a move collection.</span></span>

## <span data-ttu-id="2a422-104">語法</span><span class="sxs-lookup"><span data-stu-id="2a422-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2a422-105">描述</span><span class="sxs-lookup"><span data-stu-id="2a422-105">DESCRIPTION</span></span>
<span data-ttu-id="2a422-106">刪除移動集合。</span><span class="sxs-lookup"><span data-stu-id="2a422-106">Deletes a move collection.</span></span>

## <span data-ttu-id="2a422-107">例子</span><span class="sxs-lookup"><span data-stu-id="2a422-107">EXAMPLES</span></span>

### <span data-ttu-id="2a422-108">範例 1：移除移動集合。</span><span class="sxs-lookup"><span data-stu-id="2a422-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="2a422-109">移除移動集合。</span><span class="sxs-lookup"><span data-stu-id="2a422-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="2a422-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a422-110">PARAMETERS</span></span>

### <span data-ttu-id="2a422-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a422-111">-AsJob</span></span>
<span data-ttu-id="2a422-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="2a422-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2a422-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a422-113">-DefaultProfile</span></span>
<span data-ttu-id="2a422-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a422-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a422-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a422-115">-Name</span></span>
<span data-ttu-id="2a422-116">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="2a422-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="2a422-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2a422-117">-NoWait</span></span>
<span data-ttu-id="2a422-118">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="2a422-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2a422-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a422-119">-PassThru</span></span>
<span data-ttu-id="2a422-120">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="2a422-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a422-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a422-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a422-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2a422-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="2a422-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a422-123">-SubscriptionId</span></span>
<span data-ttu-id="2a422-124">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a422-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="2a422-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2a422-125">-Confirm</span></span>
<span data-ttu-id="2a422-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2a422-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a422-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a422-127">-WhatIf</span></span>
<span data-ttu-id="2a422-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a422-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a422-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a422-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a422-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a422-130">CommonParameters</span></span>
<span data-ttu-id="2a422-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2a422-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a422-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a422-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a422-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2a422-133">INPUTS</span></span>

## <span data-ttu-id="2a422-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2a422-134">OUTPUTS</span></span>

### <span data-ttu-id="2a422-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="2a422-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="2a422-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2a422-136">NOTES</span></span>

<span data-ttu-id="2a422-137">別名</span><span class="sxs-lookup"><span data-stu-id="2a422-137">ALIASES</span></span>

## <span data-ttu-id="2a422-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a422-138">RELATED LINKS</span></span>

