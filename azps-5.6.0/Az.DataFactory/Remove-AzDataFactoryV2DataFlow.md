---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 66f5cf02c4f50c699f790ec2790080fa37ab166d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916574"
---
# <span data-ttu-id="90009-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="90009-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="90009-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90009-102">SYNOPSIS</span></span>
<span data-ttu-id="90009-103">從 Data Factory 移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="90009-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="90009-104">語法</span><span class="sxs-lookup"><span data-stu-id="90009-104">SYNTAX</span></span>

### <span data-ttu-id="90009-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="90009-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90009-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="90009-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90009-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="90009-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90009-108">描述</span><span class="sxs-lookup"><span data-stu-id="90009-108">DESCRIPTION</span></span>
<span data-ttu-id="90009-109">此Remove-AzDataFactoryV2DataFlow Cmdlet 會從 Azure Data Factory 移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="90009-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="90009-110">例子</span><span class="sxs-lookup"><span data-stu-id="90009-110">EXAMPLES</span></span>

### <span data-ttu-id="90009-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="90009-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="90009-112">此命令會從名為 WikiADF 的資料工廠移除名為 Dataflow5 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="90009-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="90009-113">參數</span><span class="sxs-lookup"><span data-stu-id="90009-113">PARAMETERS</span></span>

### <span data-ttu-id="90009-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="90009-114">-DataFactoryName</span></span>
<span data-ttu-id="90009-115">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="90009-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90009-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90009-116">-DefaultProfile</span></span>
<span data-ttu-id="90009-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90009-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90009-118">-強制</span><span class="sxs-lookup"><span data-stu-id="90009-118">-Force</span></span>
<span data-ttu-id="90009-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="90009-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="90009-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90009-120">-InputObject</span></span>
<span data-ttu-id="90009-121">資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="90009-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90009-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="90009-122">-Name</span></span>
<span data-ttu-id="90009-123">資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="90009-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90009-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90009-124">-ResourceGroupName</span></span>
<span data-ttu-id="90009-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="90009-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90009-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90009-126">-ResourceId</span></span>
<span data-ttu-id="90009-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="90009-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90009-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90009-128">-PassThru</span></span>
<span data-ttu-id="90009-129">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="90009-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="90009-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="90009-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="90009-131">-確認</span><span class="sxs-lookup"><span data-stu-id="90009-131">-Confirm</span></span>
<span data-ttu-id="90009-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90009-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90009-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90009-133">-WhatIf</span></span>
<span data-ttu-id="90009-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90009-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90009-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90009-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90009-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90009-136">CommonParameters</span></span>
<span data-ttu-id="90009-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90009-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90009-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90009-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90009-139">輸入</span><span class="sxs-lookup"><span data-stu-id="90009-139">INPUTS</span></span>

### <span data-ttu-id="90009-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="90009-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="90009-141">System.String</span><span class="sxs-lookup"><span data-stu-id="90009-141">System.String</span></span>

## <span data-ttu-id="90009-142">輸出</span><span class="sxs-lookup"><span data-stu-id="90009-142">OUTPUTS</span></span>

### <span data-ttu-id="90009-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="90009-143">System.Void</span></span>

### <span data-ttu-id="90009-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90009-144">System.Boolean</span></span>

## <span data-ttu-id="90009-145">筆記</span><span class="sxs-lookup"><span data-stu-id="90009-145">NOTES</span></span>
<span data-ttu-id="90009-146">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="90009-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="90009-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="90009-147">RELATED LINKS</span></span>

[<span data-ttu-id="90009-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="90009-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="90009-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="90009-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

