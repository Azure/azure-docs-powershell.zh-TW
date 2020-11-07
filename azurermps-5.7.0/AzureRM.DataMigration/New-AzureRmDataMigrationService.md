---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625903"
---
# <span data-ttu-id="cfd8b-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cfd8b-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="cfd8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfd8b-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd8b-103">建立 Azure Database 遷移服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfd8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfd8b-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="cfd8b-105">說明</span><span class="sxs-lookup"><span data-stu-id="cfd8b-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd8b-106">New-AzureRmDataMigrationService Cmdlet 會建立 Azure Database 遷移服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="cfd8b-107">這個 Cmdlet 會採用現有 Azure 資源群組的名稱、要建立的 Azure 資料庫移轉服務新實例的唯一名稱、該實例的提供區域、DMS Worker SKU 的名稱，以及該服務要駐留的 Azure 虛擬子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="cfd8b-108">訂閱名稱不提供任何參數，因為使用者需要指定 Azure 登入會話或執行 Get-AzureRmSubscription 的預設訂閱– SubscriptionName "MySubscription" |Select-AzureRmSubscription 選取另一個訂閱。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="cfd8b-109">示例</span><span class="sxs-lookup"><span data-stu-id="cfd8b-109">EXAMPLES</span></span>

### <span data-ttu-id="cfd8b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cfd8b-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="cfd8b-111">上述範例示範如何在美國中北部地方建立名為 TestService 的 Azure 資料庫移轉服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="cfd8b-112">參數</span><span class="sxs-lookup"><span data-stu-id="cfd8b-112">PARAMETERS</span></span>

### <span data-ttu-id="cfd8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd8b-113">-DefaultProfile</span></span>
<span data-ttu-id="cfd8b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd8b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="cfd8b-115">-Location</span></span>
<span data-ttu-id="cfd8b-116">要建立之 Azure 資料庫移轉服務實例的位置，對應至 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd8b-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfd8b-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd8b-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cfd8b-119">-ServiceName</span></span>
<span data-ttu-id="cfd8b-120">Azure 資料庫移轉服務實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-120">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd8b-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="cfd8b-121">-Sku</span></span>
<span data-ttu-id="cfd8b-122">Azure 資料庫移轉服務實例的 sku。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="cfd8b-123">可能的值目前 Basic_1vCore、Basic_2vCores、GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="cfd8b-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd8b-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="cfd8b-124">-VirtualSubnetId</span></span>
<span data-ttu-id="cfd8b-125">指定虛擬網路下要用於 Azure 資料庫移轉服務實例之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd8b-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="cfd8b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="cfd8b-126">OUTPUTS</span></span>

### <span data-ttu-id="cfd8b-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cfd8b-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="cfd8b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="cfd8b-128">NOTES</span></span>

## <span data-ttu-id="cfd8b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfd8b-129">RELATED LINKS</span></span>

