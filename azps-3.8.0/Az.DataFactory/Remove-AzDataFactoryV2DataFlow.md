---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956412"
---
# <span data-ttu-id="90320-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="90320-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="90320-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90320-102">SYNOPSIS</span></span>
<span data-ttu-id="90320-103">從資料工廠移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="90320-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="90320-104">句法</span><span class="sxs-lookup"><span data-stu-id="90320-104">SYNTAX</span></span>

### <span data-ttu-id="90320-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="90320-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90320-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="90320-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90320-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="90320-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90320-108">說明</span><span class="sxs-lookup"><span data-stu-id="90320-108">DESCRIPTION</span></span>
<span data-ttu-id="90320-109">Remove-AzDataFactoryV2DataFlow Cmdlet 會從 Azure 資料工廠中移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="90320-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="90320-110">示例</span><span class="sxs-lookup"><span data-stu-id="90320-110">EXAMPLES</span></span>

### <span data-ttu-id="90320-111">範例1</span><span class="sxs-lookup"><span data-stu-id="90320-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="90320-112">這個命令會從資料工廠（名為 WikiADF）移除名為 dataflow5 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="90320-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="90320-113">參數</span><span class="sxs-lookup"><span data-stu-id="90320-113">PARAMETERS</span></span>

### <span data-ttu-id="90320-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="90320-114">-DataFactoryName</span></span>
<span data-ttu-id="90320-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="90320-115">The data factory name.</span></span>

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

### <span data-ttu-id="90320-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90320-116">-DefaultProfile</span></span>
<span data-ttu-id="90320-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90320-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90320-118">-Force</span><span class="sxs-lookup"><span data-stu-id="90320-118">-Force</span></span>
<span data-ttu-id="90320-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="90320-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="90320-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90320-120">-InputObject</span></span>
<span data-ttu-id="90320-121">資料流程程物件。</span><span class="sxs-lookup"><span data-stu-id="90320-121">The data flow object.</span></span>

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

### <span data-ttu-id="90320-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="90320-122">-Name</span></span>
<span data-ttu-id="90320-123">資料流程程名稱。</span><span class="sxs-lookup"><span data-stu-id="90320-123">The data flow name.</span></span>

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

### <span data-ttu-id="90320-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90320-124">-ResourceGroupName</span></span>
<span data-ttu-id="90320-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90320-125">The resource group name.</span></span>

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

### <span data-ttu-id="90320-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90320-126">-ResourceId</span></span>
<span data-ttu-id="90320-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="90320-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="90320-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90320-128">-PassThru</span></span>
<span data-ttu-id="90320-129">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="90320-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="90320-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="90320-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="90320-131">-確認</span><span class="sxs-lookup"><span data-stu-id="90320-131">-Confirm</span></span>
<span data-ttu-id="90320-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90320-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90320-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90320-133">-WhatIf</span></span>
<span data-ttu-id="90320-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90320-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90320-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90320-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90320-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90320-136">CommonParameters</span></span>
<span data-ttu-id="90320-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90320-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90320-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90320-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90320-139">輸入</span><span class="sxs-lookup"><span data-stu-id="90320-139">INPUTS</span></span>

### <span data-ttu-id="90320-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="90320-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="90320-141">System.object</span><span class="sxs-lookup"><span data-stu-id="90320-141">System.String</span></span>

## <span data-ttu-id="90320-142">輸出</span><span class="sxs-lookup"><span data-stu-id="90320-142">OUTPUTS</span></span>

### <span data-ttu-id="90320-143">System.void</span><span class="sxs-lookup"><span data-stu-id="90320-143">System.Void</span></span>

### <span data-ttu-id="90320-144">System.object</span><span class="sxs-lookup"><span data-stu-id="90320-144">System.Boolean</span></span>

## <span data-ttu-id="90320-145">筆記</span><span class="sxs-lookup"><span data-stu-id="90320-145">NOTES</span></span>
<span data-ttu-id="90320-146">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="90320-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="90320-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="90320-147">RELATED LINKS</span></span>

[<span data-ttu-id="90320-148">AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="90320-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="90320-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="90320-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

