---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 86330711dc9b35c85d87543d2b2ee55e9b1d4a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443904"
---
# <span data-ttu-id="4b9ca-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b9ca-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="4b9ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9ca-103">從資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b9ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b9ca-104">SYNTAX</span></span>

### <span data-ttu-id="4b9ca-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="4b9ca-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b9ca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b9ca-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b9ca-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b9ca-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b9ca-108">說明</span><span class="sxs-lookup"><span data-stu-id="4b9ca-108">DESCRIPTION</span></span>
<span data-ttu-id="4b9ca-109">Remove-AzureRmDataFactoryV2Dataset Cmdlet 會從 Azure 資料工廠中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="4b9ca-110">示例</span><span class="sxs-lookup"><span data-stu-id="4b9ca-110">EXAMPLES</span></span>

### <span data-ttu-id="4b9ca-111">範例1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="4b9ca-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="4b9ca-112">這個命令會從名為 WikiADF 的資料工廠中移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="4b9ca-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="4b9ca-114">參數</span><span class="sxs-lookup"><span data-stu-id="4b9ca-114">PARAMETERS</span></span>

### <span data-ttu-id="4b9ca-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4b9ca-115">-DataFactoryName</span></span>
<span data-ttu-id="4b9ca-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4b9ca-117">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b9ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9ca-118">-DefaultProfile</span></span>
<span data-ttu-id="4b9ca-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b9ca-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4b9ca-120">-Force</span></span>
<span data-ttu-id="4b9ca-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4b9ca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b9ca-122">-InputObject</span></span>
<span data-ttu-id="4b9ca-123">指定要移除的資料集物件。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="4b9ca-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b9ca-124">-Name</span></span>
<span data-ttu-id="4b9ca-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b9ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b9ca-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4b9ca-128">這個 Cmdlet 會從這個參數指定的群組中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b9ca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b9ca-129">-ResourceId</span></span>
<span data-ttu-id="4b9ca-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4b9ca-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4b9ca-131">-Confirm</span></span>
<span data-ttu-id="4b9ca-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b9ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b9ca-133">-WhatIf</span></span>
<span data-ttu-id="4b9ca-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4b9ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9ca-135">CommonParameters</span></span>
<span data-ttu-id="4b9ca-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9ca-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b9ca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9ca-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4b9ca-138">INPUTS</span></span>

### <span data-ttu-id="4b9ca-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="4b9ca-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="4b9ca-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4b9ca-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4b9ca-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4b9ca-141">System.String</span></span>

## <span data-ttu-id="4b9ca-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4b9ca-142">OUTPUTS</span></span>

### <span data-ttu-id="4b9ca-143">System.void</span><span class="sxs-lookup"><span data-stu-id="4b9ca-143">System.Void</span></span>

## <span data-ttu-id="4b9ca-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4b9ca-144">NOTES</span></span>
<span data-ttu-id="4b9ca-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="4b9ca-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4b9ca-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b9ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="4b9ca-147">AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b9ca-147">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="4b9ca-148">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b9ca-148">Set-AzureRmDataFactoryV2Dataset</span></span>]()
