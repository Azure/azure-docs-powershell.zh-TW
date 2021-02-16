---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130875"
---
# <span data-ttu-id="8aea5-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="8aea5-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="8aea5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8aea5-102">SYNOPSIS</span></span>
<span data-ttu-id="8aea5-103">開始準備包含在要求內文中的一組資源。</span><span class="sxs-lookup"><span data-stu-id="8aea5-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="8aea5-104">[準備] 作業是在 moveState "PreparePending" 或 "PrepareFailed" 中的 moveResources 上，在成功完成後，moveResource moveState 會轉換成 MovePending。</span><span class="sxs-lookup"><span data-stu-id="8aea5-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="8aea5-105">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="8aea5-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8aea5-106">句法</span><span class="sxs-lookup"><span data-stu-id="8aea5-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8aea5-107">說明</span><span class="sxs-lookup"><span data-stu-id="8aea5-107">DESCRIPTION</span></span>
<span data-ttu-id="8aea5-108">開始準備包含在要求內文中的一組資源。</span><span class="sxs-lookup"><span data-stu-id="8aea5-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="8aea5-109">[準備] 作業是在 moveState "PreparePending" 或 "PrepareFailed" 中的 moveResources 上，在成功完成後，moveResource moveState 會轉換成 MovePending。</span><span class="sxs-lookup"><span data-stu-id="8aea5-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="8aea5-110">若要協助使用者要求作業，用戶端可以使用 validateOnly 屬性設定為 true 來進行呼叫操作。</span><span class="sxs-lookup"><span data-stu-id="8aea5-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8aea5-111">示例</span><span class="sxs-lookup"><span data-stu-id="8aea5-111">EXAMPLES</span></span>

### <span data-ttu-id="8aea5-112">範例1：在準備資源前驗證 dependecies</span><span class="sxs-lookup"><span data-stu-id="8aea5-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="8aea5-113">在準備資源前驗證 dependecies。</span><span class="sxs-lookup"><span data-stu-id="8aea5-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="8aea5-114">範例2：使用「MoveResource Name」作為輸入來開始準備移動集合中的資源集</span><span class="sxs-lookup"><span data-stu-id="8aea5-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="8aea5-115">在移動集合中，使用「MoveResource Name」做為輸入來開始準備資源集合。</span><span class="sxs-lookup"><span data-stu-id="8aea5-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="8aea5-116">範例3：使用 "SourceARMID" 在移動集合中開始準備一組資源</span><span class="sxs-lookup"><span data-stu-id="8aea5-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="8aea5-117">在移動集合中使用 "SourceARMID" 開始準備資源組。</span><span class="sxs-lookup"><span data-stu-id="8aea5-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="8aea5-118">參數</span><span class="sxs-lookup"><span data-stu-id="8aea5-118">PARAMETERS</span></span>

### <span data-ttu-id="8aea5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8aea5-119">-AsJob</span></span>
<span data-ttu-id="8aea5-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="8aea5-120">Run the command as a job</span></span>

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

### <span data-ttu-id="8aea5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aea5-121">-DefaultProfile</span></span>
<span data-ttu-id="8aea5-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8aea5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aea5-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="8aea5-123">-MoveCollectionName</span></span>
<span data-ttu-id="8aea5-124">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="8aea5-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8aea5-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="8aea5-125">-MoveResource</span></span>
<span data-ttu-id="8aea5-126">取得或設定資源識別碼的清單，根據預設，接受移動資源識別碼，除非輸入類型是透過 moveResourceInputType 屬性交換。</span><span class="sxs-lookup"><span data-stu-id="8aea5-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="8aea5-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="8aea5-127">-MoveResourceInputType</span></span>
<span data-ttu-id="8aea5-128">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="8aea5-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="8aea5-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8aea5-129">-NoWait</span></span>
<span data-ttu-id="8aea5-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="8aea5-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8aea5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aea5-131">-ResourceGroupName</span></span>
<span data-ttu-id="8aea5-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aea5-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8aea5-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8aea5-133">-SubscriptionId</span></span>
<span data-ttu-id="8aea5-134">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8aea5-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="8aea5-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="8aea5-135">-ValidateOnly</span></span>
<span data-ttu-id="8aea5-136">取得或設定一個值，指出該作業是否只需要執行預先必備的操作。</span><span class="sxs-lookup"><span data-stu-id="8aea5-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="8aea5-137">-確認</span><span class="sxs-lookup"><span data-stu-id="8aea5-137">-Confirm</span></span>
<span data-ttu-id="8aea5-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8aea5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aea5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aea5-139">-WhatIf</span></span>
<span data-ttu-id="8aea5-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8aea5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aea5-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8aea5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aea5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aea5-142">CommonParameters</span></span>
<span data-ttu-id="8aea5-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8aea5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aea5-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8aea5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aea5-145">輸入</span><span class="sxs-lookup"><span data-stu-id="8aea5-145">INPUTS</span></span>

## <span data-ttu-id="8aea5-146">輸出</span><span class="sxs-lookup"><span data-stu-id="8aea5-146">OUTPUTS</span></span>

### <span data-ttu-id="8aea5-147">IOperationStatus （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="8aea5-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="8aea5-148">筆記</span><span class="sxs-lookup"><span data-stu-id="8aea5-148">NOTES</span></span>

<span data-ttu-id="8aea5-149">別名</span><span class="sxs-lookup"><span data-stu-id="8aea5-149">ALIASES</span></span>

## <span data-ttu-id="8aea5-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8aea5-150">RELATED LINKS</span></span>

