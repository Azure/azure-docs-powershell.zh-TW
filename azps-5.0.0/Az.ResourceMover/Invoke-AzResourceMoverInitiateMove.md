---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287260"
---
# <span data-ttu-id="08781-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="08781-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="08781-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08781-102">SYNOPSIS</span></span>
<span data-ttu-id="08781-103">移動包含在要求主體中的資源集。</span><span class="sxs-lookup"><span data-stu-id="08781-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="08781-104">在 moveResources 處於 moveState "MovePending" 或 "MoveFailed" 之後，就會觸發移動作業，moveResource moveState 會轉換成 CommitPending。</span><span class="sxs-lookup"><span data-stu-id="08781-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="08781-105">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="08781-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="08781-106">句法</span><span class="sxs-lookup"><span data-stu-id="08781-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08781-107">說明</span><span class="sxs-lookup"><span data-stu-id="08781-107">DESCRIPTION</span></span>
<span data-ttu-id="08781-108">移動包含在要求主體中的資源集。</span><span class="sxs-lookup"><span data-stu-id="08781-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="08781-109">在 moveResources 處於 moveState "MovePending" 或 "MoveFailed" 之後，就會觸發移動作業，moveResource moveState 會轉換成 CommitPending。</span><span class="sxs-lookup"><span data-stu-id="08781-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="08781-110">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="08781-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="08781-111">示例</span><span class="sxs-lookup"><span data-stu-id="08781-111">EXAMPLES</span></span>

### <span data-ttu-id="08781-112">範例1：在開始移動資源之前驗證 dependecies。</span><span class="sxs-lookup"><span data-stu-id="08781-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="08781-113">在開始移動資源之前驗證 dependecies。</span><span class="sxs-lookup"><span data-stu-id="08781-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="08781-114">範例2：使用 "MoveResource Name" 作為輸入來啟動移動集合中的資源集合</span><span class="sxs-lookup"><span data-stu-id="08781-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="08781-115">在移動集合中，使用 "MoveResource Name" 做為輸入的資源集合開始移動。</span><span class="sxs-lookup"><span data-stu-id="08781-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="08781-116">範例3：使用 "SourceARMID" 做為輸入，在移動集合中開始移動一組資源</span><span class="sxs-lookup"><span data-stu-id="08781-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="08781-117">在移動集合中使用 "SourceARMID" 做為輸入的資源集合開始移動。</span><span class="sxs-lookup"><span data-stu-id="08781-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="08781-118">參數</span><span class="sxs-lookup"><span data-stu-id="08781-118">PARAMETERS</span></span>

### <span data-ttu-id="08781-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08781-119">-AsJob</span></span>
<span data-ttu-id="08781-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="08781-120">Run the command as a job</span></span>

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

### <span data-ttu-id="08781-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08781-121">-DefaultProfile</span></span>
<span data-ttu-id="08781-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08781-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08781-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="08781-123">-MoveCollectionName</span></span>
<span data-ttu-id="08781-124">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="08781-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="08781-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="08781-125">-MoveResource</span></span>
<span data-ttu-id="08781-126">取得或設定資源識別碼的清單，根據預設，接受移動資源識別碼，除非輸入類型是透過 moveResourceInputType 屬性交換。</span><span class="sxs-lookup"><span data-stu-id="08781-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="08781-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="08781-127">-MoveResourceInputType</span></span>
<span data-ttu-id="08781-128">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="08781-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="08781-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="08781-129">-NoWait</span></span>
<span data-ttu-id="08781-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="08781-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="08781-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08781-131">-ResourceGroupName</span></span>
<span data-ttu-id="08781-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08781-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="08781-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08781-133">-SubscriptionId</span></span>
<span data-ttu-id="08781-134">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="08781-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="08781-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="08781-135">-ValidateOnly</span></span>
<span data-ttu-id="08781-136">取得或設定一個值，指出該作業是否只需要執行預先必備的操作。</span><span class="sxs-lookup"><span data-stu-id="08781-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="08781-137">-確認</span><span class="sxs-lookup"><span data-stu-id="08781-137">-Confirm</span></span>
<span data-ttu-id="08781-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08781-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08781-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08781-139">-WhatIf</span></span>
<span data-ttu-id="08781-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08781-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08781-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08781-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08781-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08781-142">CommonParameters</span></span>
<span data-ttu-id="08781-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08781-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08781-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08781-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08781-145">輸入</span><span class="sxs-lookup"><span data-stu-id="08781-145">INPUTS</span></span>

## <span data-ttu-id="08781-146">輸出</span><span class="sxs-lookup"><span data-stu-id="08781-146">OUTPUTS</span></span>

### <span data-ttu-id="08781-147">IOperationStatus （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="08781-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="08781-148">筆記</span><span class="sxs-lookup"><span data-stu-id="08781-148">NOTES</span></span>

<span data-ttu-id="08781-149">別名</span><span class="sxs-lookup"><span data-stu-id="08781-149">ALIASES</span></span>

## <span data-ttu-id="08781-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="08781-150">RELATED LINKS</span></span>

