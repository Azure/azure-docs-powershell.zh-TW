---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8dc191223d5ec17856605c7640d324cc2ee3794e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457632"
---
# <span data-ttu-id="f98f5-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f98f5-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="f98f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f98f5-102">SYNOPSIS</span></span>
<span data-ttu-id="f98f5-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="f98f5-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f98f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f98f5-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
[[-Tag] <Hashtable>] [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f98f5-105">說明</span><span class="sxs-lookup"><span data-stu-id="f98f5-105">DESCRIPTION</span></span>
<span data-ttu-id="f98f5-106">**AzureRmDataFactoryV2** Cmdlet 會建立具有指定資源群組名稱和位置的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="f98f5-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="f98f5-107">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="f98f5-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="f98f5-108">示例</span><span class="sxs-lookup"><span data-stu-id="f98f5-108">EXAMPLES</span></span>

### <span data-ttu-id="f98f5-109">範例1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="f98f5-109">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="f98f5-110">這個命令會在 WestUS 位置中，在名為 [ADF] 的資源群組中，建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="f98f5-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="f98f5-111">參數</span><span class="sxs-lookup"><span data-stu-id="f98f5-111">PARAMETERS</span></span>

### <span data-ttu-id="f98f5-112">-確認</span><span class="sxs-lookup"><span data-stu-id="f98f5-112">-Confirm</span></span>
<span data-ttu-id="f98f5-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f98f5-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98f5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f98f5-114">-Force</span></span>
<span data-ttu-id="f98f5-115">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f98f5-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f98f5-116">-位置</span><span class="sxs-lookup"><span data-stu-id="f98f5-116">-Location</span></span>
<span data-ttu-id="f98f5-117">此區域會建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="f98f5-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98f5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f98f5-118">-Name</span></span>
<span data-ttu-id="f98f5-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="f98f5-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="f98f5-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f98f5-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98f5-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="f98f5-122">-Tag</span></span>
<span data-ttu-id="f98f5-123">資料工廠的標籤。</span><span class="sxs-lookup"><span data-stu-id="f98f5-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f98f5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98f5-124">-WhatIf</span></span>
<span data-ttu-id="f98f5-125">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f98f5-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f98f5-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f98f5-126">INPUTS</span></span>

### <span data-ttu-id="f98f5-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f98f5-127">System.String</span></span>
<span data-ttu-id="f98f5-128">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f98f5-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f98f5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f98f5-129">OUTPUTS</span></span>

### <span data-ttu-id="f98f5-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f98f5-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f98f5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f98f5-131">NOTES</span></span>
<span data-ttu-id="f98f5-132">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="f98f5-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f98f5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f98f5-133">RELATED LINKS</span></span>
[<span data-ttu-id="f98f5-134">AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f98f5-134">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="f98f5-135">移除-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f98f5-135">Remove-AzureRmDataFactoryV2</span></span>]()
