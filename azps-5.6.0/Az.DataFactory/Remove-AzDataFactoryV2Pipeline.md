---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: eb832037080550a1a22c3cacce2386eba7c4e6f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906706"
---
# <span data-ttu-id="b35b9-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b35b9-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="b35b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b35b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b35b9-103">從 Data Factory 移除管線。</span><span class="sxs-lookup"><span data-stu-id="b35b9-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="b35b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="b35b9-104">SYNTAX</span></span>

### <span data-ttu-id="b35b9-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b35b9-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b35b9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b35b9-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b35b9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b35b9-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b35b9-108">描述</span><span class="sxs-lookup"><span data-stu-id="b35b9-108">DESCRIPTION</span></span>
<span data-ttu-id="b35b9-109">Cmdlet Remove-AzDataFactoryV2Pipeline Azure Data Factory 移除管線。</span><span class="sxs-lookup"><span data-stu-id="b35b9-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="b35b9-110">例子</span><span class="sxs-lookup"><span data-stu-id="b35b9-110">EXAMPLES</span></span>

### <span data-ttu-id="b35b9-111">範例 1：移除管線</span><span class="sxs-lookup"><span data-stu-id="b35b9-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="b35b9-112">此 Cmdlet 會從名為 WikiADF 的資料工廠移除名為DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="b35b9-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="b35b9-113">命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="b35b9-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="b35b9-114">參數</span><span class="sxs-lookup"><span data-stu-id="b35b9-114">PARAMETERS</span></span>

### <span data-ttu-id="b35b9-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b35b9-115">-DataFactoryName</span></span>
<span data-ttu-id="b35b9-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b35b9-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b35b9-117">此 Cmdlet 會從此參數指定的資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="b35b9-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b35b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35b9-118">-DefaultProfile</span></span>
<span data-ttu-id="b35b9-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b35b9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b35b9-120">-強制</span><span class="sxs-lookup"><span data-stu-id="b35b9-120">-Force</span></span>
<span data-ttu-id="b35b9-121">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="b35b9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b35b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b35b9-122">-InputObject</span></span>
<span data-ttu-id="b35b9-123">指定管線物件。</span><span class="sxs-lookup"><span data-stu-id="b35b9-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="b35b9-124">此 Cmdlet 會移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="b35b9-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="b35b9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b35b9-125">-Name</span></span>
<span data-ttu-id="b35b9-126">指定要移除的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="b35b9-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="b35b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="b35b9-128">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b35b9-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b35b9-129">此 Cmdlet 會從此參數指定的群組移除管線。</span><span class="sxs-lookup"><span data-stu-id="b35b9-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b35b9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b35b9-130">-ResourceId</span></span>
<span data-ttu-id="b35b9-131">要移除之管線的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b35b9-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="b35b9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b35b9-132">-Confirm</span></span>
<span data-ttu-id="b35b9-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b35b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b35b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35b9-134">-WhatIf</span></span>
<span data-ttu-id="b35b9-135">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b35b9-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b35b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35b9-136">CommonParameters</span></span>
<span data-ttu-id="b35b9-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b35b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35b9-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b35b9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35b9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b35b9-139">INPUTS</span></span>

### <span data-ttu-id="b35b9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b35b9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="b35b9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b35b9-141">System.String</span></span>

## <span data-ttu-id="b35b9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b35b9-142">OUTPUTS</span></span>

### <span data-ttu-id="b35b9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b35b9-143">System.Boolean</span></span>

## <span data-ttu-id="b35b9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b35b9-144">NOTES</span></span>
<span data-ttu-id="b35b9-145">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="b35b9-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b35b9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b35b9-146">RELATED LINKS</span></span>

[<span data-ttu-id="b35b9-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b35b9-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b35b9-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b35b9-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b35b9-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b35b9-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

