---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 491d86aa474fb5c392c2d9360657cd1a91072154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613037"
---
# <span data-ttu-id="342a2-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="342a2-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="342a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="342a2-102">SYNOPSIS</span></span>
<span data-ttu-id="342a2-103">如果工作處於 cancellable 狀態，則會取消正在進行的 databox 工作。</span><span class="sxs-lookup"><span data-stu-id="342a2-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="342a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="342a2-104">SYNTAX</span></span>

### <span data-ttu-id="342a2-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="342a2-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="342a2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="342a2-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="342a2-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="342a2-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="342a2-108">說明</span><span class="sxs-lookup"><span data-stu-id="342a2-108">DESCRIPTION</span></span>
<span data-ttu-id="342a2-109">**AzDataBoxJob** Cmdlet 可用來取消 databox 作業。</span><span class="sxs-lookup"><span data-stu-id="342a2-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="342a2-110">示例</span><span class="sxs-lookup"><span data-stu-id="342a2-110">EXAMPLES</span></span>

### <span data-ttu-id="342a2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="342a2-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="342a2-112">取消指定的 databox 工作</span><span class="sxs-lookup"><span data-stu-id="342a2-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="342a2-113">範例2</span><span class="sxs-lookup"><span data-stu-id="342a2-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="342a2-114">不經確認即強行取消指定的 databox 作業</span><span class="sxs-lookup"><span data-stu-id="342a2-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="342a2-115">範例3</span><span class="sxs-lookup"><span data-stu-id="342a2-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="342a2-116">取消指定的 databox 工作</span><span class="sxs-lookup"><span data-stu-id="342a2-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="342a2-117">參數</span><span class="sxs-lookup"><span data-stu-id="342a2-117">PARAMETERS</span></span>

### <span data-ttu-id="342a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342a2-118">-DefaultProfile</span></span>
<span data-ttu-id="342a2-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="342a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="342a2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="342a2-120">-Force</span></span>
<span data-ttu-id="342a2-121">不需確認就強行停止</span><span class="sxs-lookup"><span data-stu-id="342a2-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="342a2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="342a2-122">-InputObject</span></span>
<span data-ttu-id="342a2-123">類型 PSDataBoxJob 的 InputObject</span><span class="sxs-lookup"><span data-stu-id="342a2-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="342a2-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="342a2-124">-Name</span></span>
<span data-ttu-id="342a2-125">Databox 工作名稱</span><span class="sxs-lookup"><span data-stu-id="342a2-125">Databox Job Name</span></span>

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

### <span data-ttu-id="342a2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="342a2-126">-PassThru</span></span>
<span data-ttu-id="342a2-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="342a2-127">PassThru</span></span>

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

### <span data-ttu-id="342a2-128">-原因</span><span class="sxs-lookup"><span data-stu-id="342a2-128">-Reason</span></span>
<span data-ttu-id="342a2-129">取消的原因</span><span class="sxs-lookup"><span data-stu-id="342a2-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="342a2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="342a2-130">-ResourceGroupName</span></span>
<span data-ttu-id="342a2-131">Databox 工作資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="342a2-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="342a2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="342a2-132">-ResourceId</span></span>
<span data-ttu-id="342a2-133">Databox 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="342a2-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="342a2-134">-確認</span><span class="sxs-lookup"><span data-stu-id="342a2-134">-Confirm</span></span>
<span data-ttu-id="342a2-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="342a2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="342a2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="342a2-136">-WhatIf</span></span>
<span data-ttu-id="342a2-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="342a2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="342a2-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="342a2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="342a2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342a2-139">CommonParameters</span></span>
<span data-ttu-id="342a2-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="342a2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342a2-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="342a2-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342a2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="342a2-142">INPUTS</span></span>

### <span data-ttu-id="342a2-143">System.object</span><span class="sxs-lookup"><span data-stu-id="342a2-143">System.String</span></span>

## <span data-ttu-id="342a2-144">輸出</span><span class="sxs-lookup"><span data-stu-id="342a2-144">OUTPUTS</span></span>

### <span data-ttu-id="342a2-145">System.void</span><span class="sxs-lookup"><span data-stu-id="342a2-145">System.Void</span></span>

## <span data-ttu-id="342a2-146">筆記</span><span class="sxs-lookup"><span data-stu-id="342a2-146">NOTES</span></span>

## <span data-ttu-id="342a2-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="342a2-147">RELATED LINKS</span></span>