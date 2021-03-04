---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: 7d36860991d5b6b12fb23044cc607044fb87bfa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916753"
---
# <span data-ttu-id="f2ade-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f2ade-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="f2ade-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2ade-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ade-103">建立 Azure 資料庫移移服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="f2ade-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="f2ade-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2ade-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2ade-105">描述</span><span class="sxs-lookup"><span data-stu-id="f2ade-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ade-106">此New-AzDataMigrationService Cmdlet 會建立 Azure 資料庫移轉服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="f2ade-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="f2ade-107">此 Cmdlet 會取用現有 Azure 資源群組的名稱、要建立之 Azure 資料庫移轉服務新實例的唯一名稱、實例的所在地區、DMS 員工 SKU 的名稱，以及服務所在的 Azure 虛擬子網名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ade-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="f2ade-108">訂閱名稱沒有參數，因為使用者預期會指定 Azure 登入會話的預設訂閱，或執行 Get-AzSubscription -SubscriptionName "MySubscription" |Select-AzSubscription選取另一個訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2ade-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="f2ade-109">例子</span><span class="sxs-lookup"><span data-stu-id="f2ade-109">EXAMPLES</span></span>

### <span data-ttu-id="f2ade-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2ade-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="f2ade-111">上述範例顯示如何在美國中地區建立名為 TestService 的 Azure 資料庫移移服務新實例。</span><span class="sxs-lookup"><span data-stu-id="f2ade-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="f2ade-112">參數</span><span class="sxs-lookup"><span data-stu-id="f2ade-112">PARAMETERS</span></span>

### <span data-ttu-id="f2ade-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ade-113">-DefaultProfile</span></span>
<span data-ttu-id="f2ade-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2ade-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2ade-115">-位置</span><span class="sxs-lookup"><span data-stu-id="f2ade-115">-Location</span></span>
<span data-ttu-id="f2ade-116">要建立 Azure 資料庫移移服務實例的位置，對應到 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="f2ade-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ade-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2ade-117">-Name</span></span>
<span data-ttu-id="f2ade-118">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ade-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ade-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ade-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2ade-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ade-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ade-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="f2ade-121">-Sku</span></span>
<span data-ttu-id="f2ade-122">Azure 資料庫移移服務實例的 SKU。</span><span class="sxs-lookup"><span data-stu-id="f2ade-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="f2ade-123">目前可能的值Basic_1vCore，Basic_2vCores，GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="f2ade-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ade-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="f2ade-124">-VirtualSubnetId</span></span>
<span data-ttu-id="f2ade-125">指定虛擬網路下要用於 Azure 資料庫移移服務實例的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ade-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ade-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f2ade-126">-Confirm</span></span>
<span data-ttu-id="f2ade-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f2ade-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2ade-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2ade-128">-WhatIf</span></span>
<span data-ttu-id="f2ade-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2ade-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2ade-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2ade-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2ade-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ade-131">CommonParameters</span></span>
<span data-ttu-id="f2ade-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2ade-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ade-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f2ade-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ade-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f2ade-134">INPUTS</span></span>

### <span data-ttu-id="f2ade-135">沒有</span><span class="sxs-lookup"><span data-stu-id="f2ade-135">None</span></span>

## <span data-ttu-id="f2ade-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f2ade-136">OUTPUTS</span></span>

### <span data-ttu-id="f2ade-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f2ade-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="f2ade-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f2ade-138">NOTES</span></span>

## <span data-ttu-id="f2ade-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2ade-139">RELATED LINKS</span></span>
