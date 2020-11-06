---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
ms.openlocfilehash: be781e1679a5338cbc80312bbcfed01aa087a1b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454620"
---
# <span data-ttu-id="71536-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="71536-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="71536-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71536-102">SYNOPSIS</span></span>
<span data-ttu-id="71536-103">取得資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71536-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71536-104">句法</span><span class="sxs-lookup"><span data-stu-id="71536-104">SYNTAX</span></span>

### <span data-ttu-id="71536-105">BySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="71536-105">BySubscriptionId (Default)</span></span>
```
Get-AzureRmDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71536-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="71536-106">ByFactoryName</span></span>
```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71536-107">說明</span><span class="sxs-lookup"><span data-stu-id="71536-107">DESCRIPTION</span></span>
<span data-ttu-id="71536-108">Get-AzureRmDataFactoryV2 Cmdlet 會取得 Azure 資源群組中資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71536-108">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="71536-109">如果您指定資料工廠的名稱，此 Cmdlet 會取得該資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71536-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="71536-110">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資源群組中所有資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71536-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="71536-111">示例</span><span class="sxs-lookup"><span data-stu-id="71536-111">EXAMPLES</span></span>

### <span data-ttu-id="71536-112">範例1：取得所有資料工廠</span><span class="sxs-lookup"><span data-stu-id="71536-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="71536-113">顯示有關 Azure 訂閱中所有資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="71536-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="71536-114">範例2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="71536-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="71536-115">這個命令會在名為「ADF」的資源群組的訂閱中，顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="71536-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="71536-116">在後續的 Cmdlet 中指定 DataFactory 參數，以使用 $DataFactory 中儲存的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="71536-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="71536-117">參數</span><span class="sxs-lookup"><span data-stu-id="71536-117">PARAMETERS</span></span>

### <span data-ttu-id="71536-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71536-118">-DefaultProfile</span></span>
<span data-ttu-id="71536-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71536-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71536-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="71536-120">-Name</span></span>
<span data-ttu-id="71536-121">指定要取得資訊之資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="71536-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="71536-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71536-122">-ResourceGroupName</span></span>
<span data-ttu-id="71536-123">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71536-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="71536-124">這個 Cmdlet 會取得屬於此參數指定之群組之資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71536-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="71536-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71536-125">CommonParameters</span></span>
<span data-ttu-id="71536-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71536-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71536-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71536-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71536-128">輸入</span><span class="sxs-lookup"><span data-stu-id="71536-128">INPUTS</span></span>

### <span data-ttu-id="71536-129">System.object</span><span class="sxs-lookup"><span data-stu-id="71536-129">System.String</span></span>

## <span data-ttu-id="71536-130">輸出</span><span class="sxs-lookup"><span data-stu-id="71536-130">OUTPUTS</span></span>

### <span data-ttu-id="71536-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="71536-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="71536-132">筆記</span><span class="sxs-lookup"><span data-stu-id="71536-132">NOTES</span></span>
<span data-ttu-id="71536-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="71536-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="71536-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="71536-134">RELATED LINKS</span></span>

[<span data-ttu-id="71536-135">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="71536-135">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="71536-136">移除-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="71536-136">Remove-AzureRmDataFactoryV2</span></span>]()

