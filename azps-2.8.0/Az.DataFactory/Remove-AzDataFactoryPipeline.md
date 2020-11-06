---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 6d3353e9f2daead1135b3da4ebde530137d8ae1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612946"
---
# <span data-ttu-id="87d81-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="87d81-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="87d81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87d81-102">SYNOPSIS</span></span>
<span data-ttu-id="87d81-103">從 Azure 資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="87d81-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="87d81-104">句法</span><span class="sxs-lookup"><span data-stu-id="87d81-104">SYNTAX</span></span>

### <span data-ttu-id="87d81-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="87d81-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87d81-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="87d81-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d81-107">說明</span><span class="sxs-lookup"><span data-stu-id="87d81-107">DESCRIPTION</span></span>
<span data-ttu-id="87d81-108">**AzDataFactoryPipeline** Cmdlet 會從 Azure 資料工廠中移除管線。</span><span class="sxs-lookup"><span data-stu-id="87d81-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="87d81-109">示例</span><span class="sxs-lookup"><span data-stu-id="87d81-109">EXAMPLES</span></span>

### <span data-ttu-id="87d81-110">範例1：移除管線</span><span class="sxs-lookup"><span data-stu-id="87d81-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="87d81-111">這個 Cmdlet 會從資料工廠（名為 WikiADF）移除名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="87d81-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="87d81-112">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="87d81-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="87d81-113">參數</span><span class="sxs-lookup"><span data-stu-id="87d81-113">PARAMETERS</span></span>

### <span data-ttu-id="87d81-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="87d81-114">-DataFactory</span></span>
<span data-ttu-id="87d81-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="87d81-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="87d81-116">這個 Cmdlet 會從資料工廠中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="87d81-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d81-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="87d81-117">-DataFactoryName</span></span>
<span data-ttu-id="87d81-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="87d81-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="87d81-119">這個 Cmdlet 會從資料工廠中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="87d81-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="87d81-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d81-120">-DefaultProfile</span></span>
<span data-ttu-id="87d81-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="87d81-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87d81-122">-Force</span><span class="sxs-lookup"><span data-stu-id="87d81-122">-Force</span></span>
<span data-ttu-id="87d81-123">表示此 Cmdlet 不會提示您確認就移除管線。</span><span class="sxs-lookup"><span data-stu-id="87d81-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="87d81-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="87d81-124">-Name</span></span>
<span data-ttu-id="87d81-125">指定要移除的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="87d81-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d81-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d81-126">-ResourceGroupName</span></span>
<span data-ttu-id="87d81-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87d81-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="87d81-128">這個 Cmdlet 會從群組中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="87d81-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="87d81-129">-確認</span><span class="sxs-lookup"><span data-stu-id="87d81-129">-Confirm</span></span>
<span data-ttu-id="87d81-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87d81-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d81-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d81-131">-WhatIf</span></span>
<span data-ttu-id="87d81-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87d81-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d81-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87d81-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d81-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d81-134">CommonParameters</span></span>
<span data-ttu-id="87d81-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87d81-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d81-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87d81-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d81-137">輸入</span><span class="sxs-lookup"><span data-stu-id="87d81-137">INPUTS</span></span>

### <span data-ttu-id="87d81-138">System.object</span><span class="sxs-lookup"><span data-stu-id="87d81-138">System.String</span></span>

### <span data-ttu-id="87d81-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="87d81-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="87d81-140">輸出</span><span class="sxs-lookup"><span data-stu-id="87d81-140">OUTPUTS</span></span>

### <span data-ttu-id="87d81-141">System.void</span><span class="sxs-lookup"><span data-stu-id="87d81-141">System.Void</span></span>

## <span data-ttu-id="87d81-142">筆記</span><span class="sxs-lookup"><span data-stu-id="87d81-142">NOTES</span></span>
* <span data-ttu-id="87d81-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="87d81-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="87d81-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="87d81-144">RELATED LINKS</span></span>

[<span data-ttu-id="87d81-145">AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="87d81-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="87d81-146">新-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="87d81-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="87d81-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="87d81-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="87d81-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="87d81-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="87d81-149">暫停-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="87d81-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


