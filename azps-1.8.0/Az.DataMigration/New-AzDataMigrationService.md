---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: b3978bcc0e3b883d95c5161ca1b24f9cd6c6c1f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787874"
---
# <span data-ttu-id="f18d2-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f18d2-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="f18d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f18d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f18d2-103">建立 Azure Database 遷移服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="f18d2-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="f18d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f18d2-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f18d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="f18d2-105">DESCRIPTION</span></span>
<span data-ttu-id="f18d2-106">New-AzDataMigrationService Cmdlet 會建立 Azure Database 遷移服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="f18d2-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="f18d2-107">這個 Cmdlet 會採用現有 Azure 資源群組的名稱、要建立的 Azure 資料庫移轉服務新實例的唯一名稱、該實例的提供區域、DMS Worker SKU 的名稱，以及該服務要駐留的 Azure 虛擬子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="f18d2-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="f18d2-108">訂閱名稱不提供任何參數，因為使用者需要指定 Azure 登入會話或執行 Get-AzSubscription 的預設訂閱 SubscriptionName "MySubscription" |Select-AzSubscription 選取另一個訂閱。</span><span class="sxs-lookup"><span data-stu-id="f18d2-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="f18d2-109">示例</span><span class="sxs-lookup"><span data-stu-id="f18d2-109">EXAMPLES</span></span>

### <span data-ttu-id="f18d2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f18d2-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="f18d2-111">上述範例示範如何在美國中北部地方建立名為 TestService 的 Azure 資料庫移轉服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="f18d2-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="f18d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="f18d2-112">PARAMETERS</span></span>

### <span data-ttu-id="f18d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f18d2-113">-DefaultProfile</span></span>
<span data-ttu-id="f18d2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f18d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f18d2-115">-位置</span><span class="sxs-lookup"><span data-stu-id="f18d2-115">-Location</span></span>
<span data-ttu-id="f18d2-116">要建立之 Azure 資料庫移轉服務實例的位置，對應至 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="f18d2-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="f18d2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f18d2-117">-Name</span></span>
<span data-ttu-id="f18d2-118">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f18d2-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="f18d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f18d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="f18d2-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f18d2-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f18d2-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="f18d2-121">-Sku</span></span>
<span data-ttu-id="f18d2-122">Azure 資料庫移轉服務實例的 sku。</span><span class="sxs-lookup"><span data-stu-id="f18d2-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="f18d2-123">可能的值目前 Basic_1vCore、Basic_2vCores、GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="f18d2-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="f18d2-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="f18d2-124">-VirtualSubnetId</span></span>
<span data-ttu-id="f18d2-125">指定虛擬網路下要用於 Azure 資料庫移轉服務實例之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="f18d2-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="f18d2-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f18d2-126">-Confirm</span></span>
<span data-ttu-id="f18d2-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f18d2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f18d2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f18d2-128">-WhatIf</span></span>
<span data-ttu-id="f18d2-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f18d2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f18d2-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f18d2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f18d2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f18d2-131">CommonParameters</span></span>
<span data-ttu-id="f18d2-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f18d2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f18d2-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f18d2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f18d2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f18d2-134">INPUTS</span></span>

### <span data-ttu-id="f18d2-135">所有</span><span class="sxs-lookup"><span data-stu-id="f18d2-135">None</span></span>

## <span data-ttu-id="f18d2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f18d2-136">OUTPUTS</span></span>

### <span data-ttu-id="f18d2-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f18d2-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="f18d2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f18d2-138">NOTES</span></span>

## <span data-ttu-id="f18d2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f18d2-139">RELATED LINKS</span></span>
