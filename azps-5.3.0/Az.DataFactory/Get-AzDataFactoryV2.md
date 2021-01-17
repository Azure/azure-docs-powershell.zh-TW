---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449428"
---
# <span data-ttu-id="067e8-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="067e8-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="067e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="067e8-102">SYNOPSIS</span></span>
<span data-ttu-id="067e8-103">取得資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="067e8-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="067e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="067e8-104">SYNTAX</span></span>

### <span data-ttu-id="067e8-105">BySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="067e8-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="067e8-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="067e8-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="067e8-107">說明</span><span class="sxs-lookup"><span data-stu-id="067e8-107">DESCRIPTION</span></span>
<span data-ttu-id="067e8-108">Get-AzDataFactoryV2 Cmdlet 會取得 Azure 資源群組中資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="067e8-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="067e8-109">如果您指定資料工廠的名稱，此 Cmdlet 會取得該資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="067e8-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="067e8-110">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資源群組中所有資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="067e8-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="067e8-111">示例</span><span class="sxs-lookup"><span data-stu-id="067e8-111">EXAMPLES</span></span>

### <span data-ttu-id="067e8-112">範例1：取得所有資料工廠</span><span class="sxs-lookup"><span data-stu-id="067e8-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="067e8-113">顯示有關 Azure 訂閱中所有資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="067e8-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="067e8-114">範例2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="067e8-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="067e8-115">這個命令會在名為「ADF」的資源群組的訂閱中，顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="067e8-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="067e8-116">在後續的 Cmdlet 中指定 DataFactory 參數，以使用 $DataFactory 中儲存的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="067e8-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="067e8-117">參數</span><span class="sxs-lookup"><span data-stu-id="067e8-117">PARAMETERS</span></span>

### <span data-ttu-id="067e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067e8-118">-DefaultProfile</span></span>
<span data-ttu-id="067e8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="067e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="067e8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="067e8-120">-Name</span></span>
<span data-ttu-id="067e8-121">指定要取得資訊之資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="067e8-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="067e8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="067e8-122">-ResourceGroupName</span></span>
<span data-ttu-id="067e8-123">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="067e8-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="067e8-124">這個 Cmdlet 會取得屬於此參數指定之群組之資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="067e8-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="067e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067e8-125">CommonParameters</span></span>
<span data-ttu-id="067e8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="067e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067e8-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="067e8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067e8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="067e8-128">INPUTS</span></span>

### <span data-ttu-id="067e8-129">System.object</span><span class="sxs-lookup"><span data-stu-id="067e8-129">System.String</span></span>

## <span data-ttu-id="067e8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="067e8-130">OUTPUTS</span></span>

### <span data-ttu-id="067e8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="067e8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="067e8-132">筆記</span><span class="sxs-lookup"><span data-stu-id="067e8-132">NOTES</span></span>
<span data-ttu-id="067e8-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="067e8-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="067e8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="067e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="067e8-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="067e8-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="067e8-136">移除-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="067e8-136">Remove-AzDataFactoryV2</span></span>]()

