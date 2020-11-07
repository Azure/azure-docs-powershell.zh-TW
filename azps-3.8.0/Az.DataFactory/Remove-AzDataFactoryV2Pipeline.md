---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798838"
---
# <span data-ttu-id="9cf87-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9cf87-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="9cf87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cf87-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf87-103">從資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="9cf87-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="9cf87-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cf87-104">SYNTAX</span></span>

### <span data-ttu-id="9cf87-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="9cf87-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf87-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9cf87-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf87-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9cf87-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cf87-108">說明</span><span class="sxs-lookup"><span data-stu-id="9cf87-108">DESCRIPTION</span></span>
<span data-ttu-id="9cf87-109">Remove-AzDataFactoryV2Pipeline Cmdlet 會從 Azure 資料工廠中移除管線。</span><span class="sxs-lookup"><span data-stu-id="9cf87-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="9cf87-110">示例</span><span class="sxs-lookup"><span data-stu-id="9cf87-110">EXAMPLES</span></span>

### <span data-ttu-id="9cf87-111">範例1：移除管線</span><span class="sxs-lookup"><span data-stu-id="9cf87-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="9cf87-112">這個 Cmdlet 會從資料工廠（名為 WikiADF）移除名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="9cf87-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="9cf87-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="9cf87-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="9cf87-114">參數</span><span class="sxs-lookup"><span data-stu-id="9cf87-114">PARAMETERS</span></span>

### <span data-ttu-id="9cf87-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9cf87-115">-DataFactoryName</span></span>
<span data-ttu-id="9cf87-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cf87-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9cf87-117">這個 Cmdlet 會從資料工廠中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="9cf87-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9cf87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf87-118">-DefaultProfile</span></span>
<span data-ttu-id="9cf87-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cf87-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf87-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9cf87-120">-Force</span></span>
<span data-ttu-id="9cf87-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cf87-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9cf87-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cf87-122">-InputObject</span></span>
<span data-ttu-id="9cf87-123">指定管線物件。</span><span class="sxs-lookup"><span data-stu-id="9cf87-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="9cf87-124">這個 Cmdlet 會移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="9cf87-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf87-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="9cf87-125">-Name</span></span>
<span data-ttu-id="9cf87-126">指定要移除的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="9cf87-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf87-127">-ResourceGroupName</span></span>
<span data-ttu-id="9cf87-128">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cf87-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9cf87-129">這個 Cmdlet 會從群組中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="9cf87-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9cf87-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cf87-130">-ResourceId</span></span>
<span data-ttu-id="9cf87-131">要移除之管線的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9cf87-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="9cf87-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9cf87-132">-Confirm</span></span>
<span data-ttu-id="9cf87-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9cf87-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf87-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf87-134">-WhatIf</span></span>
<span data-ttu-id="9cf87-135">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9cf87-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9cf87-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf87-136">CommonParameters</span></span>
<span data-ttu-id="9cf87-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cf87-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf87-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cf87-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf87-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9cf87-139">INPUTS</span></span>

### <span data-ttu-id="9cf87-140">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="9cf87-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="9cf87-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9cf87-141">System.String</span></span>

## <span data-ttu-id="9cf87-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9cf87-142">OUTPUTS</span></span>

### <span data-ttu-id="9cf87-143">System.object</span><span class="sxs-lookup"><span data-stu-id="9cf87-143">System.Boolean</span></span>

## <span data-ttu-id="9cf87-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9cf87-144">NOTES</span></span>
<span data-ttu-id="9cf87-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="9cf87-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9cf87-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cf87-146">RELATED LINKS</span></span>

[<span data-ttu-id="9cf87-147">AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9cf87-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="9cf87-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9cf87-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="9cf87-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9cf87-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

