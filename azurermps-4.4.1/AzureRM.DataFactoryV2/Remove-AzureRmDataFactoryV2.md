---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625516"
---
# <span data-ttu-id="b52b1-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b52b1-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="b52b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b52b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b52b1-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b52b1-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b52b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b52b1-104">SYNTAX</span></span>

### <span data-ttu-id="b52b1-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b52b1-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b52b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b52b1-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b52b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b52b1-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b52b1-108">說明</span><span class="sxs-lookup"><span data-stu-id="b52b1-108">DESCRIPTION</span></span>
<span data-ttu-id="b52b1-109">Remove-AzureRmDataFactoryV2 Cmdlet 會移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b52b1-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="b52b1-110">示例</span><span class="sxs-lookup"><span data-stu-id="b52b1-110">EXAMPLES</span></span>

### <span data-ttu-id="b52b1-111">範例1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="b52b1-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="b52b1-112">這個命令會從名為 [ADF] 的資源群組中移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b52b1-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="b52b1-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="b52b1-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="b52b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="b52b1-114">PARAMETERS</span></span>

### <span data-ttu-id="b52b1-115">-確認</span><span class="sxs-lookup"><span data-stu-id="b52b1-115">-Confirm</span></span>
<span data-ttu-id="b52b1-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b52b1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b52b1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b52b1-117">-InputObject</span></span>
<span data-ttu-id="b52b1-118">指定要移除的 DataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="b52b1-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b52b1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b52b1-119">-Force</span></span>
<span data-ttu-id="b52b1-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b52b1-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b52b1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b52b1-121">-Name</span></span>
<span data-ttu-id="b52b1-122">指定要移除的資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b52b1-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b52b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b52b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="b52b1-124">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b52b1-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b52b1-125">這個 Cmdlet 會從此參數指定的群組中移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b52b1-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b52b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b52b1-126">-ResourceId</span></span>
<span data-ttu-id="b52b1-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b52b1-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b52b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b52b1-128">-WhatIf</span></span>
<span data-ttu-id="b52b1-129">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b52b1-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="b52b1-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b52b1-130">INPUTS</span></span>

### <span data-ttu-id="b52b1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b52b1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="b52b1-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b52b1-132">System.String</span></span>


## <span data-ttu-id="b52b1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b52b1-133">OUTPUTS</span></span>

### <span data-ttu-id="b52b1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b52b1-134">System.Object</span></span>

## <span data-ttu-id="b52b1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b52b1-135">NOTES</span></span>
<span data-ttu-id="b52b1-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="b52b1-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b52b1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b52b1-137">RELATED LINKS</span></span>
[<span data-ttu-id="b52b1-138">AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b52b1-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="b52b1-139">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b52b1-139">Set-AzureRmDataFactoryV2</span></span>]()
