---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127380"
---
# <span data-ttu-id="137ee-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="137ee-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="137ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="137ee-102">SYNOPSIS</span></span>
<span data-ttu-id="137ee-103">提交要求內文中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="137ee-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="137ee-104">在成功完成時，會在 moveState "CommitPending" 或 "CommitFailed" 的 moveResources 上觸發 commit 作業，moveResource moveState 執行轉換以進行確認。</span><span class="sxs-lookup"><span data-stu-id="137ee-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="137ee-105">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="137ee-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="137ee-106">句法</span><span class="sxs-lookup"><span data-stu-id="137ee-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="137ee-107">說明</span><span class="sxs-lookup"><span data-stu-id="137ee-107">DESCRIPTION</span></span>
<span data-ttu-id="137ee-108">提交要求內文中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="137ee-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="137ee-109">在成功完成時，會在 moveState "CommitPending" 或 "CommitFailed" 的 moveResources 上觸發 commit 作業，moveResource moveState 執行轉換以進行確認。</span><span class="sxs-lookup"><span data-stu-id="137ee-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="137ee-110">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="137ee-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="137ee-111">示例</span><span class="sxs-lookup"><span data-stu-id="137ee-111">EXAMPLES</span></span>

### <span data-ttu-id="137ee-112">範例1：在確認資源前驗證 dependecies</span><span class="sxs-lookup"><span data-stu-id="137ee-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="137ee-113">在確認資源前驗證 dependecies。</span><span class="sxs-lookup"><span data-stu-id="137ee-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="137ee-114">範例2：使用「MoveResource Name」作為輸入來確認移動集合中的資源集</span><span class="sxs-lookup"><span data-stu-id="137ee-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="137ee-115">在移動集合中使用「MoveResource Name」做為輸入來認可資源集</span><span class="sxs-lookup"><span data-stu-id="137ee-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="137ee-116">範例3：使用 "SourceARMID" 做為輸入，在移動集合中確認資源集</span><span class="sxs-lookup"><span data-stu-id="137ee-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="137ee-117">使用 "SourceARMID" 做為輸入來認可移動集合中的資源集</span><span class="sxs-lookup"><span data-stu-id="137ee-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="137ee-118">參數</span><span class="sxs-lookup"><span data-stu-id="137ee-118">PARAMETERS</span></span>

### <span data-ttu-id="137ee-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="137ee-119">-AsJob</span></span>
<span data-ttu-id="137ee-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="137ee-120">Run the command as a job</span></span>

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

### <span data-ttu-id="137ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137ee-121">-DefaultProfile</span></span>
<span data-ttu-id="137ee-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="137ee-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="137ee-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="137ee-123">-MoveCollectionName</span></span>
<span data-ttu-id="137ee-124">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="137ee-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="137ee-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="137ee-125">-MoveResource</span></span>
<span data-ttu-id="137ee-126">取得或設定資源識別碼的清單，根據預設，接受移動資源識別碼，除非輸入類型是透過 moveResourceInputType 屬性交換。</span><span class="sxs-lookup"><span data-stu-id="137ee-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="137ee-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="137ee-127">-MoveResourceInputType</span></span>
<span data-ttu-id="137ee-128">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="137ee-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="137ee-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="137ee-129">-NoWait</span></span>
<span data-ttu-id="137ee-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="137ee-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="137ee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="137ee-131">-ResourceGroupName</span></span>
<span data-ttu-id="137ee-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="137ee-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="137ee-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="137ee-133">-SubscriptionId</span></span>
<span data-ttu-id="137ee-134">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="137ee-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="137ee-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="137ee-135">-ValidateOnly</span></span>
<span data-ttu-id="137ee-136">取得或設定一個值，指出該作業是否只需要執行預先必備的操作。</span><span class="sxs-lookup"><span data-stu-id="137ee-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="137ee-137">-確認</span><span class="sxs-lookup"><span data-stu-id="137ee-137">-Confirm</span></span>
<span data-ttu-id="137ee-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="137ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="137ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="137ee-139">-WhatIf</span></span>
<span data-ttu-id="137ee-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="137ee-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="137ee-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="137ee-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="137ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137ee-142">CommonParameters</span></span>
<span data-ttu-id="137ee-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="137ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137ee-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="137ee-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137ee-145">輸入</span><span class="sxs-lookup"><span data-stu-id="137ee-145">INPUTS</span></span>

## <span data-ttu-id="137ee-146">輸出</span><span class="sxs-lookup"><span data-stu-id="137ee-146">OUTPUTS</span></span>

### <span data-ttu-id="137ee-147">IOperationStatus （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="137ee-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="137ee-148">筆記</span><span class="sxs-lookup"><span data-stu-id="137ee-148">NOTES</span></span>

<span data-ttu-id="137ee-149">別名</span><span class="sxs-lookup"><span data-stu-id="137ee-149">ALIASES</span></span>

## <span data-ttu-id="137ee-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="137ee-150">RELATED LINKS</span></span>

