---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446311"
---
# <span data-ttu-id="f6345-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6345-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="f6345-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6345-102">SYNOPSIS</span></span>
<span data-ttu-id="f6345-103">從 Azure 資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="f6345-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6345-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6345-104">SYNTAX</span></span>

### <span data-ttu-id="f6345-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="f6345-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6345-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f6345-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6345-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6345-107">DESCRIPTION</span></span>
<span data-ttu-id="f6345-108">**AzureRmDataFactoryPipeline** Cmdlet 會從 Azure 資料工廠中移除管線。</span><span class="sxs-lookup"><span data-stu-id="f6345-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="f6345-109">示例</span><span class="sxs-lookup"><span data-stu-id="f6345-109">EXAMPLES</span></span>

### <span data-ttu-id="f6345-110">範例1：移除管線</span><span class="sxs-lookup"><span data-stu-id="f6345-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="f6345-111">這個 Cmdlet 會從資料工廠（名為 WikiADF）移除名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="f6345-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="f6345-112">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="f6345-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="f6345-113">參數</span><span class="sxs-lookup"><span data-stu-id="f6345-113">PARAMETERS</span></span>

### <span data-ttu-id="f6345-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f6345-114">-DataFactory</span></span>
<span data-ttu-id="f6345-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="f6345-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f6345-116">這個 Cmdlet 會從資料工廠中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="f6345-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f6345-117">-DataFactoryName</span></span>
<span data-ttu-id="f6345-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6345-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f6345-119">這個 Cmdlet 會從資料工廠中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="f6345-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6345-120">-DefaultProfile</span></span>
<span data-ttu-id="f6345-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f6345-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f6345-122">-Force</span></span>
<span data-ttu-id="f6345-123">表示此 Cmdlet 不會提示您確認就移除管線。</span><span class="sxs-lookup"><span data-stu-id="f6345-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6345-124">-Name</span></span>
<span data-ttu-id="f6345-125">指定要移除的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="f6345-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6345-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6345-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6345-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f6345-128">這個 Cmdlet 會從群組中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="f6345-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f6345-129">-Confirm</span></span>
<span data-ttu-id="f6345-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6345-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6345-131">-WhatIf</span></span>
<span data-ttu-id="f6345-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6345-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6345-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6345-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6345-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6345-134">CommonParameters</span></span>
<span data-ttu-id="f6345-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6345-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6345-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6345-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6345-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f6345-137">INPUTS</span></span>

### <span data-ttu-id="f6345-138">所有</span><span class="sxs-lookup"><span data-stu-id="f6345-138">None</span></span>
<span data-ttu-id="f6345-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f6345-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6345-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f6345-140">OUTPUTS</span></span>

### <span data-ttu-id="f6345-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f6345-141">System.Boolean</span></span>

## <span data-ttu-id="f6345-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f6345-142">NOTES</span></span>
* <span data-ttu-id="f6345-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="f6345-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f6345-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6345-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6345-145">AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6345-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f6345-146">新-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6345-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f6345-147">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6345-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f6345-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f6345-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="f6345-149">暫停-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f6345-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


