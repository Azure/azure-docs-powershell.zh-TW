---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914438"
---
# <span data-ttu-id="68a93-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="68a93-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="68a93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="68a93-102">SYNOPSIS</span></span>
<span data-ttu-id="68a93-103">初始化準備要求內建的一組資源。</span><span class="sxs-lookup"><span data-stu-id="68a93-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="68a93-104">準備作業是在 moveState 'PreparePending' 或 'PrepareFailed' 的 moveResources 上，在成功完成 moveResource moveState 時，執行移轉至 MovePending。</span><span class="sxs-lookup"><span data-stu-id="68a93-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="68a93-105">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="68a93-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="68a93-106">語法</span><span class="sxs-lookup"><span data-stu-id="68a93-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68a93-107">描述</span><span class="sxs-lookup"><span data-stu-id="68a93-107">DESCRIPTION</span></span>
<span data-ttu-id="68a93-108">初始化準備要求內建的一組資源。</span><span class="sxs-lookup"><span data-stu-id="68a93-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="68a93-109">準備作業是在 moveState 'PreparePending' 或 'PrepareFailed' 的 moveResources 上，在成功完成 moveResource moveState 時，執行移轉至 MovePending。</span><span class="sxs-lookup"><span data-stu-id="68a93-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="68a93-110">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="68a93-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="68a93-111">例子</span><span class="sxs-lookup"><span data-stu-id="68a93-111">EXAMPLES</span></span>

### <span data-ttu-id="68a93-112">範例 1：在準備資源之前驗證其可靠性。</span><span class="sxs-lookup"><span data-stu-id="68a93-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="68a93-113">取得也需要準備的所需從屬資源。</span><span class="sxs-lookup"><span data-stu-id="68a93-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="68a93-114">在準備資源之前驗證可靠性。</span><span class="sxs-lookup"><span data-stu-id="68a93-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="68a93-115">取得也需要準備的所需從屬資源。</span><span class="sxs-lookup"><span data-stu-id="68a93-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="68a93-116">範例 2：使用「MoveResource Name」做為輸入，為 Move 集合中的一組資源初始化準備。</span><span class="sxs-lookup"><span data-stu-id="68a93-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="68a93-117">使用「MoveResource 名稱」做為輸入，為移動集合中的一組資源初始化準備。</span><span class="sxs-lookup"><span data-stu-id="68a93-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="68a93-118">範例 3：使用 「SourceARMID」初始化準備移動集合中的一組資源。</span><span class="sxs-lookup"><span data-stu-id="68a93-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="68a93-119">使用 「SourceARMID」為移動集合中的一組資源初始化準備。</span><span class="sxs-lookup"><span data-stu-id="68a93-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="68a93-120">參數</span><span class="sxs-lookup"><span data-stu-id="68a93-120">PARAMETERS</span></span>

### <span data-ttu-id="68a93-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68a93-121">-AsJob</span></span>
<span data-ttu-id="68a93-122">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="68a93-122">Run the command as a job</span></span>

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

### <span data-ttu-id="68a93-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a93-123">-DefaultProfile</span></span>
<span data-ttu-id="68a93-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="68a93-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a93-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="68a93-125">-MoveCollectionName</span></span>
<span data-ttu-id="68a93-126">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="68a93-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="68a93-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="68a93-127">-MoveResource</span></span>
<span data-ttu-id="68a93-128">根據預設，它會接受移動資源識別碼的清單，除非輸入類型是透過 moveResourceInputType 屬性切換。</span><span class="sxs-lookup"><span data-stu-id="68a93-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="68a93-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="68a93-129">-MoveResourceInputType</span></span>
<span data-ttu-id="68a93-130">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="68a93-130">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="68a93-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68a93-131">-NoWait</span></span>
<span data-ttu-id="68a93-132">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="68a93-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68a93-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a93-133">-ResourceGroupName</span></span>
<span data-ttu-id="68a93-134">資源組名。</span><span class="sxs-lookup"><span data-stu-id="68a93-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="68a93-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68a93-135">-SubscriptionId</span></span>
<span data-ttu-id="68a93-136">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="68a93-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="68a93-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="68a93-137">-ValidateOnly</span></span>
<span data-ttu-id="68a93-138">獲取或設定一個值，指出該作業是否需要執行先決條件。</span><span class="sxs-lookup"><span data-stu-id="68a93-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="68a93-139">-確認</span><span class="sxs-lookup"><span data-stu-id="68a93-139">-Confirm</span></span>
<span data-ttu-id="68a93-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="68a93-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a93-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a93-141">-WhatIf</span></span>
<span data-ttu-id="68a93-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68a93-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68a93-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68a93-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a93-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a93-144">CommonParameters</span></span>
<span data-ttu-id="68a93-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="68a93-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a93-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68a93-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a93-147">輸入</span><span class="sxs-lookup"><span data-stu-id="68a93-147">INPUTS</span></span>

## <span data-ttu-id="68a93-148">輸出</span><span class="sxs-lookup"><span data-stu-id="68a93-148">OUTPUTS</span></span>

### <span data-ttu-id="68a93-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="68a93-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="68a93-150">筆記</span><span class="sxs-lookup"><span data-stu-id="68a93-150">NOTES</span></span>

<span data-ttu-id="68a93-151">別名</span><span class="sxs-lookup"><span data-stu-id="68a93-151">ALIASES</span></span>

## <span data-ttu-id="68a93-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="68a93-152">RELATED LINKS</span></span>

