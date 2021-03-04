---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 5a9415b5590b6f78c5ca703dba8293c153de819d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913941"
---
# <span data-ttu-id="9aedc-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="9aedc-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="9aedc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9aedc-102">SYNOPSIS</span></span>
<span data-ttu-id="9aedc-103">刪除資料箱工作</span><span class="sxs-lookup"><span data-stu-id="9aedc-103">Deletes the databox job</span></span>

## <span data-ttu-id="9aedc-104">語法</span><span class="sxs-lookup"><span data-stu-id="9aedc-104">SYNTAX</span></span>

### <span data-ttu-id="9aedc-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9aedc-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aedc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aedc-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aedc-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aedc-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aedc-108">描述</span><span class="sxs-lookup"><span data-stu-id="9aedc-108">DESCRIPTION</span></span>
<span data-ttu-id="9aedc-109">**Remove-AzDataBoxJob** Cmdlet 是用來從資料箱工作清單中刪除完成的資料箱工作。</span><span class="sxs-lookup"><span data-stu-id="9aedc-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="9aedc-110">例子</span><span class="sxs-lookup"><span data-stu-id="9aedc-110">EXAMPLES</span></span>

### <span data-ttu-id="9aedc-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9aedc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="9aedc-112">刪除指定的資料箱工作</span><span class="sxs-lookup"><span data-stu-id="9aedc-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="9aedc-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="9aedc-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="9aedc-114">在未確認的情況下強制刪除指定的資料箱工作</span><span class="sxs-lookup"><span data-stu-id="9aedc-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="9aedc-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="9aedc-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="9aedc-116">刪除指定的資料箱工作</span><span class="sxs-lookup"><span data-stu-id="9aedc-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="9aedc-117">參數</span><span class="sxs-lookup"><span data-stu-id="9aedc-117">PARAMETERS</span></span>

### <span data-ttu-id="9aedc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aedc-118">-DefaultProfile</span></span>
<span data-ttu-id="9aedc-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9aedc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aedc-120">-強制</span><span class="sxs-lookup"><span data-stu-id="9aedc-120">-Force</span></span>
<span data-ttu-id="9aedc-121">強制移除而不確認</span><span class="sxs-lookup"><span data-stu-id="9aedc-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="9aedc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aedc-122">-InputObject</span></span>
<span data-ttu-id="9aedc-123">類型 PSDataBoxJob 的 InputObject</span><span class="sxs-lookup"><span data-stu-id="9aedc-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aedc-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9aedc-124">-Name</span></span>
<span data-ttu-id="9aedc-125">資料箱工作名稱</span><span class="sxs-lookup"><span data-stu-id="9aedc-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aedc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9aedc-126">-PassThru</span></span>
<span data-ttu-id="9aedc-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="9aedc-127">PassThru</span></span>

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

### <span data-ttu-id="9aedc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aedc-128">-ResourceGroupName</span></span>
<span data-ttu-id="9aedc-129">資料箱工作資源組名</span><span class="sxs-lookup"><span data-stu-id="9aedc-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aedc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aedc-130">-ResourceId</span></span>
<span data-ttu-id="9aedc-131">資料箱工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9aedc-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aedc-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9aedc-132">-Confirm</span></span>
<span data-ttu-id="9aedc-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9aedc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aedc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aedc-134">-WhatIf</span></span>
<span data-ttu-id="9aedc-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9aedc-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9aedc-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9aedc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aedc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aedc-137">CommonParameters</span></span>
<span data-ttu-id="9aedc-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9aedc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aedc-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9aedc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aedc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9aedc-140">INPUTS</span></span>

### <span data-ttu-id="9aedc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9aedc-141">System.String</span></span>

## <span data-ttu-id="9aedc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9aedc-142">OUTPUTS</span></span>

### <span data-ttu-id="9aedc-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="9aedc-143">System.Void</span></span>

## <span data-ttu-id="9aedc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9aedc-144">NOTES</span></span>

## <span data-ttu-id="9aedc-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9aedc-145">RELATED LINKS</span></span>
