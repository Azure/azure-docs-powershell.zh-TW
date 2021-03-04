---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: e075da17009c863e8c564eb5379495a1bdaff505
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914441"
---
# <span data-ttu-id="131d1-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="131d1-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="131d1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="131d1-102">SYNOPSIS</span></span>
<span data-ttu-id="131d1-103">移動要求內內容中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="131d1-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="131d1-104">移動作業是在 moveResources 位於 moveState 'MovePending' 或 'MoveFailed'之後觸發，在成功完成 moveResource moveState 時，會執行轉場至 CommitPending。</span><span class="sxs-lookup"><span data-stu-id="131d1-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="131d1-105">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="131d1-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="131d1-106">語法</span><span class="sxs-lookup"><span data-stu-id="131d1-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="131d1-107">描述</span><span class="sxs-lookup"><span data-stu-id="131d1-107">DESCRIPTION</span></span>
<span data-ttu-id="131d1-108">移動要求內內容中包含的一組資源。</span><span class="sxs-lookup"><span data-stu-id="131d1-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="131d1-109">移動作業是在 moveResources 位於 moveState 'MovePending' 或 'MoveFailed'之後觸發，在成功完成 moveResource moveState 時，會執行轉場至 CommitPending。</span><span class="sxs-lookup"><span data-stu-id="131d1-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="131d1-110">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="131d1-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="131d1-111">例子</span><span class="sxs-lookup"><span data-stu-id="131d1-111">EXAMPLES</span></span>

### <span data-ttu-id="131d1-112">範例 1：在資源的啟動移動之前，先驗證其可靠性。</span><span class="sxs-lookup"><span data-stu-id="131d1-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly


AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 9:39:37 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 9:39:37 AM
Status         : Succeeded

```

<span data-ttu-id="131d1-113">在針對資源啟動移動之前，先驗證其可靠性。</span><span class="sxs-lookup"><span data-stu-id="131d1-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="131d1-114">範例 2：使用「MoveResource Name」做為輸入，為 Move 集合中的資源集合初始化移動。</span><span class="sxs-lookup"><span data-stu-id="131d1-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" 

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 11:56:33 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 11:55:21 AM
Status         : Succeeded

```

<span data-ttu-id="131d1-115">使用「MoveResource 名稱」做為輸入，為 Move 集合中的資源集合初始化移動。</span><span class="sxs-lookup"><span data-stu-id="131d1-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="131d1-116">範例 3：在 Move 集合中，使用 "SourceARMID" 做為輸入，為一組資源初始化移動。</span><span class="sxs-lookup"><span data-stu-id="131d1-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:01:35 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:00:21 PM
Status         : Succeeded

```

<span data-ttu-id="131d1-117">使用 「SourceARMID」 做為輸入，為 Move 集合中的資源集合初始化移動。</span><span class="sxs-lookup"><span data-stu-id="131d1-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="131d1-118">參數</span><span class="sxs-lookup"><span data-stu-id="131d1-118">PARAMETERS</span></span>

### <span data-ttu-id="131d1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="131d1-119">-AsJob</span></span>
<span data-ttu-id="131d1-120">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="131d1-120">Run the command as a job</span></span>

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

### <span data-ttu-id="131d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131d1-121">-DefaultProfile</span></span>
<span data-ttu-id="131d1-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="131d1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131d1-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="131d1-123">-MoveCollectionName</span></span>
<span data-ttu-id="131d1-124">移動集合名稱。</span><span class="sxs-lookup"><span data-stu-id="131d1-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="131d1-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="131d1-125">-MoveResource</span></span>
<span data-ttu-id="131d1-126">根據預設，它會接受移動資源識別碼的清單，除非輸入類型是透過 moveResourceInputType 屬性切換。</span><span class="sxs-lookup"><span data-stu-id="131d1-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="131d1-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="131d1-127">-MoveResourceInputType</span></span>
<span data-ttu-id="131d1-128">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="131d1-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="131d1-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="131d1-129">-NoWait</span></span>
<span data-ttu-id="131d1-130">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="131d1-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="131d1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131d1-131">-ResourceGroupName</span></span>
<span data-ttu-id="131d1-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="131d1-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="131d1-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="131d1-133">-SubscriptionId</span></span>
<span data-ttu-id="131d1-134">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="131d1-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="131d1-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="131d1-135">-ValidateOnly</span></span>
<span data-ttu-id="131d1-136">獲取或設定一個值，指出該作業是否需要執行先決條件。</span><span class="sxs-lookup"><span data-stu-id="131d1-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="131d1-137">-確認</span><span class="sxs-lookup"><span data-stu-id="131d1-137">-Confirm</span></span>
<span data-ttu-id="131d1-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="131d1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131d1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131d1-139">-WhatIf</span></span>
<span data-ttu-id="131d1-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="131d1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131d1-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="131d1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131d1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131d1-142">CommonParameters</span></span>
<span data-ttu-id="131d1-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="131d1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131d1-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="131d1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131d1-145">輸入</span><span class="sxs-lookup"><span data-stu-id="131d1-145">INPUTS</span></span>

## <span data-ttu-id="131d1-146">輸出</span><span class="sxs-lookup"><span data-stu-id="131d1-146">OUTPUTS</span></span>

### <span data-ttu-id="131d1-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="131d1-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="131d1-148">筆記</span><span class="sxs-lookup"><span data-stu-id="131d1-148">NOTES</span></span>

<span data-ttu-id="131d1-149">別名</span><span class="sxs-lookup"><span data-stu-id="131d1-149">ALIASES</span></span>

## <span data-ttu-id="131d1-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="131d1-150">RELATED LINKS</span></span>

