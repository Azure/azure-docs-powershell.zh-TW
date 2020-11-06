---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444939"
---
# <span data-ttu-id="61e5a-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="61e5a-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="61e5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="61e5a-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="61e5a-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61e5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="61e5a-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61e5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="61e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="61e5a-106">**AzureRmDataFactoryV2** Cmdlet 會建立具有指定資源群組名稱和位置的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="61e5a-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="61e5a-107">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="61e5a-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="61e5a-108">示例</span><span class="sxs-lookup"><span data-stu-id="61e5a-108">EXAMPLES</span></span>

### <span data-ttu-id="61e5a-109">範例1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="61e5a-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="61e5a-110">這個命令會在 WestUS 位置中，在名為 [ADF] 的資源群組中，建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="61e5a-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="61e5a-111">參數</span><span class="sxs-lookup"><span data-stu-id="61e5a-111">PARAMETERS</span></span>

### <span data-ttu-id="61e5a-112">-確認</span><span class="sxs-lookup"><span data-stu-id="61e5a-112">-Confirm</span></span>
<span data-ttu-id="61e5a-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61e5a-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e5a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="61e5a-114">-Force</span></span>
<span data-ttu-id="61e5a-115">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61e5a-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="61e5a-116">-位置</span><span class="sxs-lookup"><span data-stu-id="61e5a-116">-Location</span></span>
<span data-ttu-id="61e5a-117">此區域會建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="61e5a-117">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e5a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="61e5a-118">-Name</span></span>
<span data-ttu-id="61e5a-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="61e5a-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e5a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e5a-120">-ResourceGroupName</span></span>
<span data-ttu-id="61e5a-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61e5a-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e5a-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="61e5a-122">-Tag</span></span>
<span data-ttu-id="61e5a-123">資料工廠的標籤。</span><span class="sxs-lookup"><span data-stu-id="61e5a-123">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e5a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e5a-124">-WhatIf</span></span>
<span data-ttu-id="61e5a-125">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61e5a-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="61e5a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e5a-126">-DefaultProfile</span></span>
<span data-ttu-id="61e5a-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61e5a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61e5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e5a-128">CommonParameters</span></span>
<span data-ttu-id="61e5a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61e5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e5a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61e5a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e5a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="61e5a-131">INPUTS</span></span>

### <span data-ttu-id="61e5a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="61e5a-132">System.String</span></span>
<span data-ttu-id="61e5a-133">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="61e5a-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="61e5a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="61e5a-134">OUTPUTS</span></span>

### <span data-ttu-id="61e5a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="61e5a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="61e5a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="61e5a-136">NOTES</span></span>
<span data-ttu-id="61e5a-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="61e5a-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="61e5a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="61e5a-138">RELATED LINKS</span></span>

[<span data-ttu-id="61e5a-139">AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="61e5a-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="61e5a-140">移除-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="61e5a-140">Remove-AzureRmDataFactoryV2</span></span>]()
