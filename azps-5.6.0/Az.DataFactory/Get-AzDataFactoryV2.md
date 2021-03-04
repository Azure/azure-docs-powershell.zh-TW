---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: 05fad970f92d871dafdb7f712eb4227f7ed06eaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907749"
---
# <span data-ttu-id="68cae-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="68cae-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="68cae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="68cae-102">SYNOPSIS</span></span>
<span data-ttu-id="68cae-103">獲得 Data Factory 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68cae-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="68cae-104">語法</span><span class="sxs-lookup"><span data-stu-id="68cae-104">SYNTAX</span></span>

### <span data-ttu-id="68cae-105">BySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="68cae-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68cae-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="68cae-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68cae-107">描述</span><span class="sxs-lookup"><span data-stu-id="68cae-107">DESCRIPTION</span></span>
<span data-ttu-id="68cae-108">Cmdlet Get-AzDataFactoryV2 Azure 資源群組中資料需求的資訊。</span><span class="sxs-lookup"><span data-stu-id="68cae-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="68cae-109">如果您指定資料工廠的名稱，此 Cmdlet 會獲得該資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="68cae-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="68cae-110">如果您未指定名稱，此 Cmdlet 會獲得 Azure 資源群組中所有資料工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="68cae-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="68cae-111">例子</span><span class="sxs-lookup"><span data-stu-id="68cae-111">EXAMPLES</span></span>

### <span data-ttu-id="68cae-112">範例 1：取得所有資料</span><span class="sxs-lookup"><span data-stu-id="68cae-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="68cae-113">顯示 Azure 訂閱中所有資料預訂的資訊。</span><span class="sxs-lookup"><span data-stu-id="68cae-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="68cae-114">範例 2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="68cae-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="68cae-115">此命令會在名為 ADF 的資源群組訂閱中顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="68cae-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="68cae-116">在後續的 Cmdlet 中指定 DataFactory 參數，以使用儲存在 $DataFactory。</span><span class="sxs-lookup"><span data-stu-id="68cae-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="68cae-117">參數</span><span class="sxs-lookup"><span data-stu-id="68cae-117">PARAMETERS</span></span>

### <span data-ttu-id="68cae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cae-118">-DefaultProfile</span></span>
<span data-ttu-id="68cae-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="68cae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="68cae-120">-Name</span></span>
<span data-ttu-id="68cae-121">指定要取得資訊的資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="68cae-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cae-122">-ResourceGroupName</span></span>
<span data-ttu-id="68cae-123">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68cae-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="68cae-124">此 Cmdlet 會獲得屬於此參數指定群組之資料轉場的資訊。</span><span class="sxs-lookup"><span data-stu-id="68cae-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="68cae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cae-125">CommonParameters</span></span>
<span data-ttu-id="68cae-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="68cae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cae-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68cae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cae-128">輸入</span><span class="sxs-lookup"><span data-stu-id="68cae-128">INPUTS</span></span>

### <span data-ttu-id="68cae-129">System.String</span><span class="sxs-lookup"><span data-stu-id="68cae-129">System.String</span></span>

## <span data-ttu-id="68cae-130">輸出</span><span class="sxs-lookup"><span data-stu-id="68cae-130">OUTPUTS</span></span>

### <span data-ttu-id="68cae-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="68cae-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="68cae-132">筆記</span><span class="sxs-lookup"><span data-stu-id="68cae-132">NOTES</span></span>
<span data-ttu-id="68cae-133">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="68cae-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="68cae-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="68cae-134">RELATED LINKS</span></span>

[<span data-ttu-id="68cae-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="68cae-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="68cae-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="68cae-136">Remove-AzDataFactoryV2</span></span>]()

