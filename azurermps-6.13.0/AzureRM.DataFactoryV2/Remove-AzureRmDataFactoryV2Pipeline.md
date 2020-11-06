---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: ed3284445121bf2ab6ecdd9aef2d8abe6d1351f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443899"
---
# <span data-ttu-id="65922-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="65922-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="65922-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65922-102">SYNOPSIS</span></span>
<span data-ttu-id="65922-103">從資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="65922-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65922-104">句法</span><span class="sxs-lookup"><span data-stu-id="65922-104">SYNTAX</span></span>

### <span data-ttu-id="65922-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="65922-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65922-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65922-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65922-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65922-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65922-108">說明</span><span class="sxs-lookup"><span data-stu-id="65922-108">DESCRIPTION</span></span>
<span data-ttu-id="65922-109">Remove-AzureRmDataFactoryV2Pipeline Cmdlet 會從 Azure 資料工廠中移除管線。</span><span class="sxs-lookup"><span data-stu-id="65922-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="65922-110">示例</span><span class="sxs-lookup"><span data-stu-id="65922-110">EXAMPLES</span></span>

### <span data-ttu-id="65922-111">範例1：移除管線</span><span class="sxs-lookup"><span data-stu-id="65922-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="65922-112">這個 Cmdlet 會從資料工廠（名為 WikiADF）移除名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="65922-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="65922-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="65922-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="65922-114">參數</span><span class="sxs-lookup"><span data-stu-id="65922-114">PARAMETERS</span></span>

### <span data-ttu-id="65922-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="65922-115">-DataFactoryName</span></span>
<span data-ttu-id="65922-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="65922-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="65922-117">這個 Cmdlet 會從資料工廠中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="65922-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="65922-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65922-118">-DefaultProfile</span></span>
<span data-ttu-id="65922-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65922-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65922-120">-Force</span><span class="sxs-lookup"><span data-stu-id="65922-120">-Force</span></span>
<span data-ttu-id="65922-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65922-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="65922-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65922-122">-InputObject</span></span>
<span data-ttu-id="65922-123">指定管線物件。</span><span class="sxs-lookup"><span data-stu-id="65922-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="65922-124">這個 Cmdlet 會移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="65922-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="65922-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="65922-125">-Name</span></span>
<span data-ttu-id="65922-126">指定要移除的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="65922-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="65922-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65922-127">-ResourceGroupName</span></span>
<span data-ttu-id="65922-128">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="65922-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="65922-129">這個 Cmdlet 會從群組中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="65922-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="65922-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65922-130">-ResourceId</span></span>
<span data-ttu-id="65922-131">要移除之管線的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="65922-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="65922-132">-確認</span><span class="sxs-lookup"><span data-stu-id="65922-132">-Confirm</span></span>
<span data-ttu-id="65922-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65922-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65922-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65922-134">-WhatIf</span></span>
<span data-ttu-id="65922-135">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65922-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="65922-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65922-136">CommonParameters</span></span>
<span data-ttu-id="65922-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65922-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65922-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65922-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65922-139">輸入</span><span class="sxs-lookup"><span data-stu-id="65922-139">INPUTS</span></span>

### <span data-ttu-id="65922-140">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="65922-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="65922-141">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="65922-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="65922-142">System.object</span><span class="sxs-lookup"><span data-stu-id="65922-142">System.String</span></span>

## <span data-ttu-id="65922-143">輸出</span><span class="sxs-lookup"><span data-stu-id="65922-143">OUTPUTS</span></span>

### <span data-ttu-id="65922-144">System.object</span><span class="sxs-lookup"><span data-stu-id="65922-144">System.Boolean</span></span>

## <span data-ttu-id="65922-145">筆記</span><span class="sxs-lookup"><span data-stu-id="65922-145">NOTES</span></span>
<span data-ttu-id="65922-146">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="65922-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="65922-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="65922-147">RELATED LINKS</span></span>

[<span data-ttu-id="65922-148">AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="65922-148">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="65922-149">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="65922-149">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="65922-150">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="65922-150">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

