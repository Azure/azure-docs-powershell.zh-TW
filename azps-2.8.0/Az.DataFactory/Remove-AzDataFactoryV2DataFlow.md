---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 75c155b765a1bcbc565a85fc0f47130a6d2a5cf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612942"
---
# <span data-ttu-id="ab809-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="ab809-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="ab809-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab809-102">SYNOPSIS</span></span>
<span data-ttu-id="ab809-103">從資料工廠移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="ab809-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="ab809-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab809-104">SYNTAX</span></span>

### <span data-ttu-id="ab809-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="ab809-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab809-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab809-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab809-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab809-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab809-108">說明</span><span class="sxs-lookup"><span data-stu-id="ab809-108">DESCRIPTION</span></span>
<span data-ttu-id="ab809-109">Remove-AzDataFactoryV2DataFlow Cmdlet 會從 Azure 資料工廠中移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="ab809-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="ab809-110">示例</span><span class="sxs-lookup"><span data-stu-id="ab809-110">EXAMPLES</span></span>

### <span data-ttu-id="ab809-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ab809-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="ab809-112">這個命令會從資料工廠（名為 WikiADF）移除名為 dataflow5 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ab809-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="ab809-113">參數</span><span class="sxs-lookup"><span data-stu-id="ab809-113">PARAMETERS</span></span>

### <span data-ttu-id="ab809-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ab809-114">-DataFactoryName</span></span>
<span data-ttu-id="ab809-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="ab809-115">The data factory name.</span></span>

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

### <span data-ttu-id="ab809-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab809-116">-DefaultProfile</span></span>
<span data-ttu-id="ab809-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab809-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab809-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ab809-118">-Force</span></span>
<span data-ttu-id="ab809-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ab809-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ab809-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab809-120">-InputObject</span></span>
<span data-ttu-id="ab809-121">資料流程程物件。</span><span class="sxs-lookup"><span data-stu-id="ab809-121">The data flow object.</span></span>

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

### <span data-ttu-id="ab809-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab809-122">-Name</span></span>
<span data-ttu-id="ab809-123">資料流程程名稱。</span><span class="sxs-lookup"><span data-stu-id="ab809-123">The data flow name.</span></span>

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

### <span data-ttu-id="ab809-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab809-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab809-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab809-125">The resource group name.</span></span>

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

### <span data-ttu-id="ab809-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab809-126">-ResourceId</span></span>
<span data-ttu-id="ab809-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab809-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ab809-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab809-128">-PassThru</span></span>
<span data-ttu-id="ab809-129">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="ab809-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="ab809-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ab809-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab809-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ab809-131">-Confirm</span></span>
<span data-ttu-id="ab809-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab809-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab809-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab809-133">-WhatIf</span></span>
<span data-ttu-id="ab809-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab809-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab809-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab809-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab809-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab809-136">CommonParameters</span></span>
<span data-ttu-id="ab809-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab809-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab809-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ab809-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab809-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ab809-139">INPUTS</span></span>

### <span data-ttu-id="ab809-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="ab809-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="ab809-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ab809-141">System.String</span></span>

## <span data-ttu-id="ab809-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ab809-142">OUTPUTS</span></span>

### <span data-ttu-id="ab809-143">System.void</span><span class="sxs-lookup"><span data-stu-id="ab809-143">System.Void</span></span>

### <span data-ttu-id="ab809-144">System.object</span><span class="sxs-lookup"><span data-stu-id="ab809-144">System.Boolean</span></span>

## <span data-ttu-id="ab809-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ab809-145">NOTES</span></span>
<span data-ttu-id="ab809-146">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="ab809-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ab809-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab809-147">RELATED LINKS</span></span>

[<span data-ttu-id="ab809-148">AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="ab809-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="ab809-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="ab809-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

