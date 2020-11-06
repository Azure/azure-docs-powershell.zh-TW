---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457640"
---
# <span data-ttu-id="83ac0-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="83ac0-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="83ac0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="83ac0-103">從資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="83ac0-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83ac0-104">句法</span><span class="sxs-lookup"><span data-stu-id="83ac0-104">SYNTAX</span></span>

### <span data-ttu-id="83ac0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="83ac0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="83ac0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83ac0-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="83ac0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83ac0-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="83ac0-108">說明</span><span class="sxs-lookup"><span data-stu-id="83ac0-108">DESCRIPTION</span></span>
<span data-ttu-id="83ac0-109">Remove-AzureRmDataFactoryV2LinkedService Cmdlet 會從 Azure 資料工廠中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="83ac0-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="83ac0-110">示例</span><span class="sxs-lookup"><span data-stu-id="83ac0-110">EXAMPLES</span></span>

### <span data-ttu-id="83ac0-111">範例1：移除連結的服務</span><span class="sxs-lookup"><span data-stu-id="83ac0-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="83ac0-112">這個命令會從名為 WikiADF 的資料工廠中移除名為 LinkedServiceTest 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="83ac0-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="83ac0-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="83ac0-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="83ac0-114">參數</span><span class="sxs-lookup"><span data-stu-id="83ac0-114">PARAMETERS</span></span>

### <span data-ttu-id="83ac0-115">-確認</span><span class="sxs-lookup"><span data-stu-id="83ac0-115">-Confirm</span></span>
<span data-ttu-id="83ac0-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83ac0-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ac0-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="83ac0-117">-DataFactoryName</span></span>
<span data-ttu-id="83ac0-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="83ac0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="83ac0-119">這個 Cmdlet 會從此參數指定的資料工廠移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="83ac0-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="83ac0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="83ac0-120">-Force</span></span>
<span data-ttu-id="83ac0-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83ac0-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="83ac0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83ac0-122">-InputObject</span></span>
<span data-ttu-id="83ac0-123">指定要移除的 LinkedService 物件。</span><span class="sxs-lookup"><span data-stu-id="83ac0-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83ac0-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="83ac0-124">-Name</span></span>
<span data-ttu-id="83ac0-125">指定要移除之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="83ac0-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="83ac0-126">連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="83ac0-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ac0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ac0-127">-ResourceGroupName</span></span>
<span data-ttu-id="83ac0-128">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83ac0-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="83ac0-129">這個 Cmdlet 會從此參數指定的群組中移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="83ac0-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="83ac0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83ac0-130">-ResourceId</span></span>
<span data-ttu-id="83ac0-131">要移除之連結服務的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="83ac0-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83ac0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ac0-132">-WhatIf</span></span>
<span data-ttu-id="83ac0-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83ac0-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="83ac0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="83ac0-134">INPUTS</span></span>

### <span data-ttu-id="83ac0-135">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="83ac0-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="83ac0-136">System.object</span><span class="sxs-lookup"><span data-stu-id="83ac0-136">System.String</span></span>


## <span data-ttu-id="83ac0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="83ac0-137">OUTPUTS</span></span>

### <span data-ttu-id="83ac0-138">System.object</span><span class="sxs-lookup"><span data-stu-id="83ac0-138">System.Object</span></span>

## <span data-ttu-id="83ac0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="83ac0-139">NOTES</span></span>
<span data-ttu-id="83ac0-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="83ac0-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="83ac0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="83ac0-141">RELATED LINKS</span></span>
[<span data-ttu-id="83ac0-142">AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="83ac0-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="83ac0-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="83ac0-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

