---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 298a86c05cc318fbe360cddd2341901070601d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445627"
---
# <span data-ttu-id="40d13-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40d13-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="40d13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40d13-102">SYNOPSIS</span></span>
<span data-ttu-id="40d13-103">在資料工廠中繼續執行暫停的管線。</span><span class="sxs-lookup"><span data-stu-id="40d13-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40d13-104">句法</span><span class="sxs-lookup"><span data-stu-id="40d13-104">SYNTAX</span></span>

### <span data-ttu-id="40d13-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="40d13-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d13-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="40d13-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d13-107">說明</span><span class="sxs-lookup"><span data-stu-id="40d13-107">DESCRIPTION</span></span>
<span data-ttu-id="40d13-108">**Resume AzureRmDataFactoryPipeline** Cmdlet 會在 Azure 資料工廠中繼續暫停的管線。</span><span class="sxs-lookup"><span data-stu-id="40d13-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="40d13-109">示例</span><span class="sxs-lookup"><span data-stu-id="40d13-109">EXAMPLES</span></span>

### <span data-ttu-id="40d13-110">範例1：繼續管線</span><span class="sxs-lookup"><span data-stu-id="40d13-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="40d13-111">這個命令會在名為 WikiADF 的資料工廠中，恢復名為 DPWikisample 的管道。</span><span class="sxs-lookup"><span data-stu-id="40d13-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="40d13-112">使用 **AzureRmDataFactoryPipeline** Cmdlet 來暫停管線。</span><span class="sxs-lookup"><span data-stu-id="40d13-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="40d13-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="40d13-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="40d13-114">參數</span><span class="sxs-lookup"><span data-stu-id="40d13-114">PARAMETERS</span></span>

### <span data-ttu-id="40d13-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="40d13-115">-DataFactory</span></span>
<span data-ttu-id="40d13-116">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="40d13-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="40d13-117">這個 Cmdlet 會繼續屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="40d13-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40d13-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="40d13-118">-DataFactoryName</span></span>
<span data-ttu-id="40d13-119">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="40d13-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="40d13-120">這個 Cmdlet 會繼續屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="40d13-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40d13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d13-121">-DefaultProfile</span></span>
<span data-ttu-id="40d13-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="40d13-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d13-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="40d13-123">-Name</span></span>
<span data-ttu-id="40d13-124">指定要繼續的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="40d13-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="40d13-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d13-125">-ResourceGroupName</span></span>
<span data-ttu-id="40d13-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40d13-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="40d13-127">這個 Cmdlet 會繼續屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="40d13-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="40d13-128">-確認</span><span class="sxs-lookup"><span data-stu-id="40d13-128">-Confirm</span></span>
<span data-ttu-id="40d13-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40d13-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d13-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d13-130">-WhatIf</span></span>
<span data-ttu-id="40d13-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40d13-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d13-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40d13-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d13-133">CommonParameters</span></span>
<span data-ttu-id="40d13-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40d13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d13-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40d13-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d13-136">輸入</span><span class="sxs-lookup"><span data-stu-id="40d13-136">INPUTS</span></span>

### <span data-ttu-id="40d13-137">System.object</span><span class="sxs-lookup"><span data-stu-id="40d13-137">System.String</span></span>

### <span data-ttu-id="40d13-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="40d13-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="40d13-139">輸出</span><span class="sxs-lookup"><span data-stu-id="40d13-139">OUTPUTS</span></span>

### <span data-ttu-id="40d13-140">System.object</span><span class="sxs-lookup"><span data-stu-id="40d13-140">System.Boolean</span></span>

## <span data-ttu-id="40d13-141">筆記</span><span class="sxs-lookup"><span data-stu-id="40d13-141">NOTES</span></span>
* <span data-ttu-id="40d13-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="40d13-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="40d13-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="40d13-143">RELATED LINKS</span></span>

[<span data-ttu-id="40d13-144">AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40d13-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40d13-145">新-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40d13-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40d13-146">移除-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40d13-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="40d13-147">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="40d13-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="40d13-148">暫停-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="40d13-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


