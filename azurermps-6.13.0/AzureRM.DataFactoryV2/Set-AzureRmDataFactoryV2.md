---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449210"
---
# <span data-ttu-id="b2a97-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b2a97-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="b2a97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2a97-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a97-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b2a97-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2a97-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2a97-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2a97-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2a97-105">DESCRIPTION</span></span>
<span data-ttu-id="b2a97-106">**AzureRmDataFactoryV2** Cmdlet 會建立具有指定資源群組名稱和位置的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b2a97-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="b2a97-107">依下列循序執行這些作業：--建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b2a97-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="b2a97-108">--建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="b2a97-108">-- Create linked services.</span></span>
<span data-ttu-id="b2a97-109">--建立資料集。</span><span class="sxs-lookup"><span data-stu-id="b2a97-109">-- Create datasets.</span></span>
<span data-ttu-id="b2a97-110">--建立管線。</span><span class="sxs-lookup"><span data-stu-id="b2a97-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="b2a97-111">示例</span><span class="sxs-lookup"><span data-stu-id="b2a97-111">EXAMPLES</span></span>

### <span data-ttu-id="b2a97-112">範例1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="b2a97-112">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="b2a97-113">這個命令會在 WestUS 位置中，在名為 [ADF] 的資源群組中，建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b2a97-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="b2a97-114">參數</span><span class="sxs-lookup"><span data-stu-id="b2a97-114">PARAMETERS</span></span>

### <span data-ttu-id="b2a97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a97-115">-DefaultProfile</span></span>
<span data-ttu-id="b2a97-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2a97-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2a97-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b2a97-117">-Force</span></span>
<span data-ttu-id="b2a97-118">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2a97-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b2a97-119">-位置</span><span class="sxs-lookup"><span data-stu-id="b2a97-119">-Location</span></span>
<span data-ttu-id="b2a97-120">此區域會建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b2a97-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="b2a97-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2a97-121">-Name</span></span>
<span data-ttu-id="b2a97-122">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="b2a97-122">The data factory name.</span></span>

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

### <span data-ttu-id="b2a97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2a97-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2a97-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2a97-124">The resource group name.</span></span>

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

### <span data-ttu-id="b2a97-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2a97-125">-Tag</span></span>
<span data-ttu-id="b2a97-126">資料工廠的標籤。</span><span class="sxs-lookup"><span data-stu-id="b2a97-126">The tags of the data factory.</span></span>

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

### <span data-ttu-id="b2a97-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b2a97-127">-Confirm</span></span>
<span data-ttu-id="b2a97-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2a97-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2a97-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2a97-129">-WhatIf</span></span>
<span data-ttu-id="b2a97-130">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2a97-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b2a97-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a97-131">CommonParameters</span></span>
<span data-ttu-id="b2a97-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2a97-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a97-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2a97-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a97-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b2a97-134">INPUTS</span></span>

### <span data-ttu-id="b2a97-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b2a97-135">System.String</span></span>

### <span data-ttu-id="b2a97-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2a97-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b2a97-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b2a97-137">OUTPUTS</span></span>

### <span data-ttu-id="b2a97-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b2a97-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b2a97-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b2a97-139">NOTES</span></span>
<span data-ttu-id="b2a97-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="b2a97-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b2a97-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2a97-141">RELATED LINKS</span></span>

[<span data-ttu-id="b2a97-142">AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b2a97-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="b2a97-143">移除-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b2a97-143">Remove-AzureRmDataFactoryV2</span></span>]()
