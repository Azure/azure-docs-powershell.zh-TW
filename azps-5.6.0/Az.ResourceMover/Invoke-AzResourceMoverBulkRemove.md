---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914450"
---
# <span data-ttu-id="b62a0-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="b62a0-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="b62a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b62a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b62a0-103">移除移動集合中要求內建的一組移動資源。</span><span class="sxs-lookup"><span data-stu-id="b62a0-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="b62a0-104">這項功能是使用服務完成。</span><span class="sxs-lookup"><span data-stu-id="b62a0-104">The orchestration is done by service.</span></span>
<span data-ttu-id="b62a0-105">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="b62a0-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b62a0-106">語法</span><span class="sxs-lookup"><span data-stu-id="b62a0-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b62a0-107">描述</span><span class="sxs-lookup"><span data-stu-id="b62a0-107">DESCRIPTION</span></span>
<span data-ttu-id="b62a0-108">移除移動集合中要求內建的一組移動資源。</span><span class="sxs-lookup"><span data-stu-id="b62a0-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="b62a0-109">這項功能是使用服務完成。</span><span class="sxs-lookup"><span data-stu-id="b62a0-109">The orchestration is done by service.</span></span>
<span data-ttu-id="b62a0-110">為了協助使用者完成作業的先決條件，用戶端可以使用 validateOnly 屬性設為 True 來呼叫作業。</span><span class="sxs-lookup"><span data-stu-id="b62a0-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b62a0-111">例子</span><span class="sxs-lookup"><span data-stu-id="b62a0-111">EXAMPLES</span></span>

### <span data-ttu-id="b62a0-112">範例 1：從移動集合移除移動資源之前，先驗證其可靠性</span><span class="sxs-lookup"><span data-stu-id="b62a0-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="b62a0-113">從移動集合移除移動資源之前，先驗證其可靠性。</span><span class="sxs-lookup"><span data-stu-id="b62a0-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="b62a0-114">範例 2：使用 "MoveResource Name" 做為輸入，從移動集合移除移動資源</span><span class="sxs-lookup"><span data-stu-id="b62a0-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="b62a0-115">使用「MoveResource 名稱」做為輸入，從移動集合移除移動資源</span><span class="sxs-lookup"><span data-stu-id="b62a0-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="b62a0-116">範例 3：使用 "SourceARMID" 做為輸入，從移動集合移除移動資源</span><span class="sxs-lookup"><span data-stu-id="b62a0-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="b62a0-117">使用 「SourceARMID」做為輸入，從移動集合移除移動資源</span><span class="sxs-lookup"><span data-stu-id="b62a0-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="b62a0-118">參數</span><span class="sxs-lookup"><span data-stu-id="b62a0-118">PARAMETERS</span></span>

### <span data-ttu-id="b62a0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b62a0-119">-AsJob</span></span>
<span data-ttu-id="b62a0-120">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b62a0-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b62a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62a0-121">-DefaultProfile</span></span>
<span data-ttu-id="b62a0-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b62a0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b62a0-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="b62a0-123">-MoveCollectionName</span></span>
<span data-ttu-id="b62a0-124">.</span><span class="sxs-lookup"><span data-stu-id="b62a0-124">.</span></span>

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

### <span data-ttu-id="b62a0-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="b62a0-125">-MoveResource</span></span>
<span data-ttu-id="b62a0-126">根據預設，它會接受移動資源識別碼的清單，除非輸入類型是透過 moveResourceInputType 屬性切換。</span><span class="sxs-lookup"><span data-stu-id="b62a0-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b62a0-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="b62a0-127">-MoveResourceInputType</span></span>
<span data-ttu-id="b62a0-128">定義移動資源輸入類型。</span><span class="sxs-lookup"><span data-stu-id="b62a0-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="b62a0-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b62a0-129">-NoWait</span></span>
<span data-ttu-id="b62a0-130">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b62a0-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b62a0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b62a0-131">-ResourceGroupName</span></span>
<span data-ttu-id="b62a0-132">.</span><span class="sxs-lookup"><span data-stu-id="b62a0-132">.</span></span>

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

### <span data-ttu-id="b62a0-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b62a0-133">-SubscriptionId</span></span>
<span data-ttu-id="b62a0-134">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b62a0-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="b62a0-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="b62a0-135">-ValidateOnly</span></span>
<span data-ttu-id="b62a0-136">獲取或設定一個值，指出該作業是否需要執行先決條件。</span><span class="sxs-lookup"><span data-stu-id="b62a0-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="b62a0-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b62a0-137">-Confirm</span></span>
<span data-ttu-id="b62a0-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b62a0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62a0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62a0-139">-WhatIf</span></span>
<span data-ttu-id="b62a0-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b62a0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b62a0-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b62a0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b62a0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62a0-142">CommonParameters</span></span>
<span data-ttu-id="b62a0-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b62a0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62a0-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b62a0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62a0-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b62a0-145">INPUTS</span></span>

## <span data-ttu-id="b62a0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b62a0-146">OUTPUTS</span></span>

### <span data-ttu-id="b62a0-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b62a0-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="b62a0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b62a0-148">NOTES</span></span>

<span data-ttu-id="b62a0-149">別名</span><span class="sxs-lookup"><span data-stu-id="b62a0-149">ALIASES</span></span>

## <span data-ttu-id="b62a0-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b62a0-150">RELATED LINKS</span></span>

