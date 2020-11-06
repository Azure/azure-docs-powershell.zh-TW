---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
ms.openlocfilehash: cba3540f47d2ce53b11a11f237adb28aa0bec6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446865"
---
# <span data-ttu-id="eae9c-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eae9c-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="eae9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eae9c-102">SYNOPSIS</span></span>
<span data-ttu-id="eae9c-103">取得資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eae9c-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eae9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="eae9c-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eae9c-105">說明</span><span class="sxs-lookup"><span data-stu-id="eae9c-105">DESCRIPTION</span></span>
<span data-ttu-id="eae9c-106">Get-AzureRmDataFactoryV2 Cmdlet 會取得 Azure 資源群組中資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eae9c-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="eae9c-107">如果您指定資料工廠的名稱，此 Cmdlet 會取得該資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eae9c-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="eae9c-108">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資源群組中所有資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eae9c-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="eae9c-109">示例</span><span class="sxs-lookup"><span data-stu-id="eae9c-109">EXAMPLES</span></span>

### <span data-ttu-id="eae9c-110">範例1：取得所有資料工廠</span><span class="sxs-lookup"><span data-stu-id="eae9c-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="eae9c-111">顯示有關 Azure 訂閱中所有資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="eae9c-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="eae9c-112">範例2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="eae9c-112">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="eae9c-113">這個命令會在名為「ADF」的資源群組的訂閱中，顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="eae9c-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="eae9c-114">在後續的 Cmdlet 中指定 DataFactory 參數，以使用 $DataFactory 中儲存的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="eae9c-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="eae9c-115">參數</span><span class="sxs-lookup"><span data-stu-id="eae9c-115">PARAMETERS</span></span>

### <span data-ttu-id="eae9c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="eae9c-116">-Name</span></span>
<span data-ttu-id="eae9c-117">指定要取得資訊之資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="eae9c-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eae9c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eae9c-118">-ResourceGroupName</span></span>
<span data-ttu-id="eae9c-119">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eae9c-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eae9c-120">這個 Cmdlet 會取得屬於此參數指定之群組之資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eae9c-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="eae9c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae9c-121">-DefaultProfile</span></span>
<span data-ttu-id="eae9c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eae9c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eae9c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae9c-123">CommonParameters</span></span>
<span data-ttu-id="eae9c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eae9c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae9c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eae9c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae9c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="eae9c-126">INPUTS</span></span>

### <span data-ttu-id="eae9c-127">System.object</span><span class="sxs-lookup"><span data-stu-id="eae9c-127">System.String</span></span>

## <span data-ttu-id="eae9c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="eae9c-128">OUTPUTS</span></span>

### <span data-ttu-id="eae9c-129">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null）]</span><span class="sxs-lookup"><span data-stu-id="eae9c-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="eae9c-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eae9c-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="eae9c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="eae9c-131">NOTES</span></span>
<span data-ttu-id="eae9c-132">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="eae9c-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eae9c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="eae9c-133">RELATED LINKS</span></span>

[<span data-ttu-id="eae9c-134">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eae9c-134">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="eae9c-135">移除-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eae9c-135">Remove-AzureRmDataFactoryV2</span></span>]()

