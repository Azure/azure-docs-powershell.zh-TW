---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: f8a50a7e9686a3e40f517992e6c4de9912e8671b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905198"
---
# <span data-ttu-id="b3148-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="b3148-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="b3148-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3148-102">SYNOPSIS</span></span>
<span data-ttu-id="b3148-103">從訂閱或管理群組移除藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="b3148-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="b3148-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3148-104">SYNTAX</span></span>

### <span data-ttu-id="b3148-105">BySubscriptionAndName (預設) </span><span class="sxs-lookup"><span data-stu-id="b3148-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3148-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="b3148-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3148-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="b3148-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3148-108">描述</span><span class="sxs-lookup"><span data-stu-id="b3148-108">DESCRIPTION</span></span>
<span data-ttu-id="b3148-109">移除已指派給訂閱的藍圖。</span><span class="sxs-lookup"><span data-stu-id="b3148-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="b3148-110">例子</span><span class="sxs-lookup"><span data-stu-id="b3148-110">EXAMPLES</span></span>

### <span data-ttu-id="b3148-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b3148-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="b3148-112">從指定的訂閱移除以名稱指定的藍圖工作分派。</span><span class="sxs-lookup"><span data-stu-id="b3148-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="b3148-113">執行命令之前，Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3148-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="b3148-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3148-114">PARAMETERS</span></span>

### <span data-ttu-id="b3148-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3148-115">-DefaultProfile</span></span>
<span data-ttu-id="b3148-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3148-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3148-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3148-117">-InputObject</span></span>
<span data-ttu-id="b3148-118">藍圖工作分派物件。</span><span class="sxs-lookup"><span data-stu-id="b3148-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3148-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b3148-119">-ManagementGroupId</span></span>
<span data-ttu-id="b3148-120">儲存藍圖工作分派之管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3148-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3148-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3148-121">-Name</span></span>
<span data-ttu-id="b3148-122">藍圖工作分派名稱。</span><span class="sxs-lookup"><span data-stu-id="b3148-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3148-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3148-123">-PassThru</span></span>
<span data-ttu-id="b3148-124">設定完成之後，Cmdlet 會返回代表已移除藍圖工作分派的物件。</span><span class="sxs-lookup"><span data-stu-id="b3148-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="b3148-125">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b3148-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3148-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3148-126">-SubscriptionId</span></span>
<span data-ttu-id="b3148-127">部署藍圖指派的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3148-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3148-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b3148-128">-Confirm</span></span>
<span data-ttu-id="b3148-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3148-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3148-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3148-130">-WhatIf</span></span>
<span data-ttu-id="b3148-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3148-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3148-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3148-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3148-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3148-133">CommonParameters</span></span>
<span data-ttu-id="b3148-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3148-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3148-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3148-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3148-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b3148-136">INPUTS</span></span>

### <span data-ttu-id="b3148-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b3148-137">System.String</span></span>

### <span data-ttu-id="b3148-138">Microsoft.Azure.Commands.藍圖.models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="b3148-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="b3148-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b3148-139">OUTPUTS</span></span>

### <span data-ttu-id="b3148-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="b3148-140">System.Object</span></span>
## <span data-ttu-id="b3148-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b3148-141">NOTES</span></span>

## <span data-ttu-id="b3148-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3148-142">RELATED LINKS</span></span>
