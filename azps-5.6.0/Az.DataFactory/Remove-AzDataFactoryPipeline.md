---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 25653cb7423803f2722a87e218c4ee4b3d73be86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907137"
---
# <span data-ttu-id="f07d5-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f07d5-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="f07d5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f07d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f07d5-103">從 Azure Data Factory 移除管線。</span><span class="sxs-lookup"><span data-stu-id="f07d5-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="f07d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="f07d5-104">SYNTAX</span></span>

### <span data-ttu-id="f07d5-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="f07d5-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f07d5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f07d5-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f07d5-107">描述</span><span class="sxs-lookup"><span data-stu-id="f07d5-107">DESCRIPTION</span></span>
<span data-ttu-id="f07d5-108">**Remove-AzDataFactoryPipeline** Cmdlet 會從 Azure Data Factory 移除管線。</span><span class="sxs-lookup"><span data-stu-id="f07d5-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="f07d5-109">例子</span><span class="sxs-lookup"><span data-stu-id="f07d5-109">EXAMPLES</span></span>

### <span data-ttu-id="f07d5-110">範例 1：移除管線</span><span class="sxs-lookup"><span data-stu-id="f07d5-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="f07d5-111">此 Cmdlet 會從名為 WikiADF 的資料工廠移除名為DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="f07d5-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="f07d5-112">命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="f07d5-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="f07d5-113">參數</span><span class="sxs-lookup"><span data-stu-id="f07d5-113">PARAMETERS</span></span>

### <span data-ttu-id="f07d5-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f07d5-114">-DataFactory</span></span>
<span data-ttu-id="f07d5-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="f07d5-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f07d5-116">此 Cmdlet 會從此參數指定的資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="f07d5-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f07d5-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f07d5-117">-DataFactoryName</span></span>
<span data-ttu-id="f07d5-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="f07d5-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f07d5-119">此 Cmdlet 會從此參數指定的資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="f07d5-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f07d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07d5-120">-DefaultProfile</span></span>
<span data-ttu-id="f07d5-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f07d5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f07d5-122">-強制</span><span class="sxs-lookup"><span data-stu-id="f07d5-122">-Force</span></span>
<span data-ttu-id="f07d5-123">表示此 Cmdlet 會移除管線，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f07d5-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f07d5-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f07d5-124">-Name</span></span>
<span data-ttu-id="f07d5-125">指定要移除的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="f07d5-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="f07d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f07d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="f07d5-127">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f07d5-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f07d5-128">此 Cmdlet 會從此參數指定的群組移除管線。</span><span class="sxs-lookup"><span data-stu-id="f07d5-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f07d5-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f07d5-129">-Confirm</span></span>
<span data-ttu-id="f07d5-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f07d5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f07d5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07d5-131">-WhatIf</span></span>
<span data-ttu-id="f07d5-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f07d5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f07d5-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f07d5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f07d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07d5-134">CommonParameters</span></span>
<span data-ttu-id="f07d5-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f07d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07d5-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f07d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07d5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f07d5-137">INPUTS</span></span>

### <span data-ttu-id="f07d5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f07d5-138">System.String</span></span>

### <span data-ttu-id="f07d5-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f07d5-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f07d5-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f07d5-140">OUTPUTS</span></span>

### <span data-ttu-id="f07d5-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="f07d5-141">System.Void</span></span>

## <span data-ttu-id="f07d5-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f07d5-142">NOTES</span></span>
* <span data-ttu-id="f07d5-143">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="f07d5-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f07d5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f07d5-144">RELATED LINKS</span></span>

[<span data-ttu-id="f07d5-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f07d5-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="f07d5-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f07d5-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="f07d5-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f07d5-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="f07d5-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f07d5-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="f07d5-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f07d5-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


