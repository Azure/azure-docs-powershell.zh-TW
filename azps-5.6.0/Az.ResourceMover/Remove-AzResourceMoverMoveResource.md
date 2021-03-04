---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914418"
---
# <span data-ttu-id="ac0e3-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ac0e3-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="ac0e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ac0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0e3-103">刪除移動集合中的移動資源。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="ac0e3-104">語法</span><span class="sxs-lookup"><span data-stu-id="ac0e3-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ac0e3-105">描述</span><span class="sxs-lookup"><span data-stu-id="ac0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="ac0e3-106">刪除移動集合中的移動資源。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="ac0e3-107">例子</span><span class="sxs-lookup"><span data-stu-id="ac0e3-107">EXAMPLES</span></span>

### <span data-ttu-id="ac0e3-108">範例 1：從移動集合移除一個 Move Rresource。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="ac0e3-109">從移動集合移除一個 Move Rresource。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="ac0e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac0e3-110">PARAMETERS</span></span>

### <span data-ttu-id="ac0e3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac0e3-111">-AsJob</span></span>
<span data-ttu-id="ac0e3-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="ac0e3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ac0e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0e3-113">-DefaultProfile</span></span>
<span data-ttu-id="ac0e3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac0e3-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ac0e3-115">-MoveCollectionName</span></span>
<span data-ttu-id="ac0e3-116">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ac0e3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac0e3-117">-Name</span></span>
<span data-ttu-id="ac0e3-118">移動資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0e3-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac0e3-119">-NoWait</span></span>
<span data-ttu-id="ac0e3-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="ac0e3-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac0e3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac0e3-121">-PassThru</span></span>
<span data-ttu-id="ac0e3-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="ac0e3-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ac0e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac0e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac0e3-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ac0e3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac0e3-125">-SubscriptionId</span></span>
<span data-ttu-id="ac0e3-126">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="ac0e3-127">-確認</span><span class="sxs-lookup"><span data-stu-id="ac0e3-127">-Confirm</span></span>
<span data-ttu-id="ac0e3-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac0e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac0e3-129">-WhatIf</span></span>
<span data-ttu-id="ac0e3-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac0e3-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac0e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0e3-132">CommonParameters</span></span>
<span data-ttu-id="ac0e3-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ac0e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0e3-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac0e3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0e3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ac0e3-135">INPUTS</span></span>

## <span data-ttu-id="ac0e3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ac0e3-136">OUTPUTS</span></span>

### <span data-ttu-id="ac0e3-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ac0e3-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="ac0e3-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ac0e3-138">NOTES</span></span>

<span data-ttu-id="ac0e3-139">別名</span><span class="sxs-lookup"><span data-stu-id="ac0e3-139">ALIASES</span></span>

## <span data-ttu-id="ac0e3-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac0e3-140">RELATED LINKS</span></span>

