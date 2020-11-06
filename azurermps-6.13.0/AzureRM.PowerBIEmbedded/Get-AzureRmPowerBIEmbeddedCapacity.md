---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447297"
---
# <span data-ttu-id="cf01a-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cf01a-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cf01a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf01a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf01a-103">取得 PowerBI 內嵌容量的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cf01a-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf01a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf01a-104">SYNTAX</span></span>

### <span data-ttu-id="cf01a-105">ByCapacityOrResourceGroupOrSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="cf01a-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf01a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf01a-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf01a-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf01a-107">DESCRIPTION</span></span>
<span data-ttu-id="cf01a-108">Get-AzureRmPowerBIEmbeddedCapacity Cmdlet 會取得 PowerBI 內嵌容量的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cf01a-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="cf01a-109">示例</span><span class="sxs-lookup"><span data-stu-id="cf01a-109">EXAMPLES</span></span>

### <span data-ttu-id="cf01a-110">範例1：取得資源群組容量</span><span class="sxs-lookup"><span data-stu-id="cf01a-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="cf01a-111">這個命令會在名為 testRG 的資源群組中取得所有的 Azure PowerBI 內嵌容量</span><span class="sxs-lookup"><span data-stu-id="cf01a-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="cf01a-112">範例2：取得容量</span><span class="sxs-lookup"><span data-stu-id="cf01a-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="cf01a-113">這個命令會在名為 testRG 的資源群組中，取得名為 testcapacity 的 Azure PowerBI 內嵌的容量。</span><span class="sxs-lookup"><span data-stu-id="cf01a-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="cf01a-114">參數</span><span class="sxs-lookup"><span data-stu-id="cf01a-114">PARAMETERS</span></span>

### <span data-ttu-id="cf01a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf01a-115">-DefaultProfile</span></span>
<span data-ttu-id="cf01a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf01a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf01a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf01a-117">-Name</span></span>
<span data-ttu-id="cf01a-118">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="cf01a-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf01a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf01a-119">-ResourceGroupName</span></span>
<span data-ttu-id="cf01a-120">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="cf01a-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf01a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf01a-121">-ResourceId</span></span>
<span data-ttu-id="cf01a-122">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cf01a-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf01a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf01a-123">CommonParameters</span></span>
<span data-ttu-id="cf01a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf01a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf01a-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf01a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf01a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="cf01a-126">INPUTS</span></span>

### <span data-ttu-id="cf01a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="cf01a-127">System.String</span></span>

## <span data-ttu-id="cf01a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="cf01a-128">OUTPUTS</span></span>

### <span data-ttu-id="cf01a-129">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="cf01a-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cf01a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="cf01a-130">NOTES</span></span>

## <span data-ttu-id="cf01a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf01a-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf01a-132">新-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="cf01a-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="cf01a-133">移除-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="cf01a-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
