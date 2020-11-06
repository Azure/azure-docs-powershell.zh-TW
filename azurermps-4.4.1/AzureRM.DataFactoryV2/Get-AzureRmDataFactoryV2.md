---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450784"
---
# <span data-ttu-id="8ff7d-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ff7d-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="8ff7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ff7d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff7d-103">取得資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ff7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ff7d-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="8ff7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ff7d-105">DESCRIPTION</span></span>
<span data-ttu-id="8ff7d-106">Get-AzureRmDataFactoryV2 Cmdlet 會取得 Azure 資源群組中資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="8ff7d-107">如果您指定資料工廠的名稱，此 Cmdlet 會取得該資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="8ff7d-108">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資源群組中所有資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="8ff7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="8ff7d-109">EXAMPLES</span></span>

### <span data-ttu-id="8ff7d-110">範例1：取得所有資料工廠</span><span class="sxs-lookup"><span data-stu-id="8ff7d-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

<span data-ttu-id="8ff7d-111">顯示有關 Azure 訂閱中所有資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="8ff7d-112">範例2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="8ff7d-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="8ff7d-113">這個命令會在名為「ADF」的資源群組的訂閱中，顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="8ff7d-114">在後續的 Cmdlet 中指定 DataFactory 參數，以使用 $DataFactory 中儲存的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="8ff7d-115">參數</span><span class="sxs-lookup"><span data-stu-id="8ff7d-115">PARAMETERS</span></span>

### <span data-ttu-id="8ff7d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ff7d-116">-Name</span></span>
<span data-ttu-id="8ff7d-117">指定要取得資訊之資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff7d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff7d-118">-ResourceGroupName</span></span>
<span data-ttu-id="8ff7d-119">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8ff7d-120">這個 Cmdlet 會取得屬於此參數指定之群組之資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ff7d-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

## <span data-ttu-id="8ff7d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="8ff7d-121">INPUTS</span></span>

### <span data-ttu-id="8ff7d-122">System.object</span><span class="sxs-lookup"><span data-stu-id="8ff7d-122">System.String</span></span>


## <span data-ttu-id="8ff7d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8ff7d-123">OUTPUTS</span></span>

### <span data-ttu-id="8ff7d-124">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null）]</span><span class="sxs-lookup"><span data-stu-id="8ff7d-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8ff7d-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8ff7d-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="8ff7d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8ff7d-126">NOTES</span></span>
<span data-ttu-id="8ff7d-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="8ff7d-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8ff7d-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ff7d-128">RELATED LINKS</span></span>
[<span data-ttu-id="8ff7d-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ff7d-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="8ff7d-130">移除-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ff7d-130">Remove-AzureRmDataFactoryV2</span></span>]()
