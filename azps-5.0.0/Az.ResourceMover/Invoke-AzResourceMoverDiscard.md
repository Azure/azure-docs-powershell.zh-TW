---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287263"
---
# <span data-ttu-id="4d178-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="4d178-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="4d178-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d178-102">SYNOPSIS</span></span>
<span data-ttu-id="4d178-103">捨棄包含在要求主體中的資源集。</span><span class="sxs-lookup"><span data-stu-id="4d178-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="4d178-104">在成功完成時，會在 moveState "CommitPending" 或 "DiscardFailed" 的 moveResources 上觸發放棄作業，moveResource moveState 會轉換成 MovePending。</span><span class="sxs-lookup"><span data-stu-id="4d178-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="4d178-105">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="4d178-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="4d178-106">句法</span><span class="sxs-lookup"><span data-stu-id="4d178-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d178-107">說明</span><span class="sxs-lookup"><span data-stu-id="4d178-107">DESCRIPTION</span></span>
<span data-ttu-id="4d178-108">捨棄包含在要求主體中的資源集。</span><span class="sxs-lookup"><span data-stu-id="4d178-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="4d178-109">在成功完成時，會在 moveState "CommitPending" 或 "DiscardFailed" 的 moveResources 上觸發放棄作業，moveResource moveState 會轉換成 MovePending。</span><span class="sxs-lookup"><span data-stu-id="4d178-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="4d178-110">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="4d178-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="4d178-111">示例</span><span class="sxs-lookup"><span data-stu-id="4d178-111">EXAMPLES</span></span>

### <span data-ttu-id="4d178-112">範例1：在放棄資源前驗證 dependecies。</span><span class="sxs-lookup"><span data-stu-id="4d178-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="4d178-113">在放棄資源前驗證 dependecies。</span><span class="sxs-lookup"><span data-stu-id="4d178-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="4d178-114">範例2：使用 "MoveResource Name" 做為輸入，放棄資源的移動</span><span class="sxs-lookup"><span data-stu-id="4d178-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="4d178-115">使用「MoveResource Name」做為輸入，放棄資源的移動。</span><span class="sxs-lookup"><span data-stu-id="4d178-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="4d178-116">範例3：捨棄使用 "SourceARMID" 做為輸入的資源移動</span><span class="sxs-lookup"><span data-stu-id="4d178-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="4d178-117">使用 "SourceARMID" 做為輸入，放棄移動資源。</span><span class="sxs-lookup"><span data-stu-id="4d178-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="4d178-118">參數</span><span class="sxs-lookup"><span data-stu-id="4d178-118">PARAMETERS</span></span>

### <span data-ttu-id="4d178-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d178-119">-AsJob</span></span>
<span data-ttu-id="4d178-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="4d178-120">Run the command as a job</span></span>

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

### <span data-ttu-id="4d178-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d178-121">-DefaultProfile</span></span>
<span data-ttu-id="4d178-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d178-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d178-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="4d178-123">-MoveResource</span></span>
<span data-ttu-id="4d178-124">取得或設定資源識別碼的清單，根據預設，接受移動資源識別碼，除非輸入類型是透過 moveResourceInputType 屬性交換。</span><span class="sxs-lookup"><span data-stu-id="4d178-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d178-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="4d178-125">-MoveResourceInputType</span></span>
<span data-ttu-id="4d178-126">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="4d178-126">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d178-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d178-127">-Name</span></span>
<span data-ttu-id="4d178-128">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="4d178-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4d178-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4d178-129">-NoWait</span></span>
<span data-ttu-id="4d178-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="4d178-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4d178-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d178-131">-ResourceGroupName</span></span>
<span data-ttu-id="4d178-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d178-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4d178-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d178-133">-SubscriptionId</span></span>
<span data-ttu-id="4d178-134">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4d178-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="4d178-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="4d178-135">-ValidateOnly</span></span>
<span data-ttu-id="4d178-136">取得或設定一個值，指出該作業是否只需要執行預先必備的操作。</span><span class="sxs-lookup"><span data-stu-id="4d178-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="4d178-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4d178-137">-Confirm</span></span>
<span data-ttu-id="4d178-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4d178-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d178-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d178-139">-WhatIf</span></span>
<span data-ttu-id="4d178-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d178-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d178-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d178-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d178-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d178-142">CommonParameters</span></span>
<span data-ttu-id="4d178-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d178-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d178-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4d178-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d178-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4d178-145">INPUTS</span></span>

## <span data-ttu-id="4d178-146">輸出</span><span class="sxs-lookup"><span data-stu-id="4d178-146">OUTPUTS</span></span>

### <span data-ttu-id="4d178-147">IOperationStatus （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="4d178-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="4d178-148">筆記</span><span class="sxs-lookup"><span data-stu-id="4d178-148">NOTES</span></span>

<span data-ttu-id="4d178-149">別名</span><span class="sxs-lookup"><span data-stu-id="4d178-149">ALIASES</span></span>

## <span data-ttu-id="4d178-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d178-150">RELATED LINKS</span></span>

