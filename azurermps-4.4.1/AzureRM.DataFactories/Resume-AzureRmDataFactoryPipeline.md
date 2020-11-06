---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 63bb7337e7473d27838b08763ebe2a7de14514a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446855"
---
# <span data-ttu-id="372fb-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="372fb-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="372fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="372fb-102">SYNOPSIS</span></span>
<span data-ttu-id="372fb-103">在資料工廠中繼續執行暫停的管線。</span><span class="sxs-lookup"><span data-stu-id="372fb-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="372fb-104">SYNTAX</span></span>

### <span data-ttu-id="372fb-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="372fb-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372fb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="372fb-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372fb-107">說明</span><span class="sxs-lookup"><span data-stu-id="372fb-107">DESCRIPTION</span></span>
<span data-ttu-id="372fb-108">**Resume AzureRmDataFactoryPipeline** Cmdlet 會在 Azure 資料工廠中繼續暫停的管線。</span><span class="sxs-lookup"><span data-stu-id="372fb-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="372fb-109">示例</span><span class="sxs-lookup"><span data-stu-id="372fb-109">EXAMPLES</span></span>

### <span data-ttu-id="372fb-110">範例1：繼續管線</span><span class="sxs-lookup"><span data-stu-id="372fb-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="372fb-111">這個命令會在名為 WikiADF 的資料工廠中，恢復名為 DPWikisample 的管道。</span><span class="sxs-lookup"><span data-stu-id="372fb-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="372fb-112">使用 **AzureRmDataFactoryPipeline** Cmdlet 來暫停管線。</span><span class="sxs-lookup"><span data-stu-id="372fb-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="372fb-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="372fb-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="372fb-114">參數</span><span class="sxs-lookup"><span data-stu-id="372fb-114">PARAMETERS</span></span>

### <span data-ttu-id="372fb-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="372fb-115">-DataFactory</span></span>
<span data-ttu-id="372fb-116">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="372fb-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="372fb-117">這個 Cmdlet 會繼續屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="372fb-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="372fb-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="372fb-118">-DataFactoryName</span></span>
<span data-ttu-id="372fb-119">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="372fb-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="372fb-120">這個 Cmdlet 會繼續屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="372fb-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="372fb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="372fb-121">-Name</span></span>
<span data-ttu-id="372fb-122">指定要繼續的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="372fb-122">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="372fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="372fb-124">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="372fb-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="372fb-125">這個 Cmdlet 會繼續屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="372fb-125">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="372fb-126">-確認</span><span class="sxs-lookup"><span data-stu-id="372fb-126">-Confirm</span></span>
<span data-ttu-id="372fb-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="372fb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372fb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372fb-128">-WhatIf</span></span>
<span data-ttu-id="372fb-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="372fb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372fb-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="372fb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372fb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372fb-131">-DefaultProfile</span></span>
<span data-ttu-id="372fb-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="372fb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="372fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372fb-133">CommonParameters</span></span>
<span data-ttu-id="372fb-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="372fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372fb-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="372fb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372fb-136">輸入</span><span class="sxs-lookup"><span data-stu-id="372fb-136">INPUTS</span></span>

## <span data-ttu-id="372fb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="372fb-137">OUTPUTS</span></span>

### <span data-ttu-id="372fb-138">System.object</span><span class="sxs-lookup"><span data-stu-id="372fb-138">System.Boolean</span></span>

## <span data-ttu-id="372fb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="372fb-139">NOTES</span></span>
* <span data-ttu-id="372fb-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="372fb-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="372fb-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="372fb-141">RELATED LINKS</span></span>

[<span data-ttu-id="372fb-142">AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="372fb-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="372fb-143">新-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="372fb-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="372fb-144">移除-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="372fb-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="372fb-145">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="372fb-145">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="372fb-146">暫停-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="372fb-146">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


