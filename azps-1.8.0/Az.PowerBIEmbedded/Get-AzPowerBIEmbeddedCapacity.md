---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 68d9e388238f9054ce56592186f686728e378000
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621265"
---
# <span data-ttu-id="89318-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="89318-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="89318-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89318-102">SYNOPSIS</span></span>
<span data-ttu-id="89318-103">取得 PowerBI 內嵌容量的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89318-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="89318-104">句法</span><span class="sxs-lookup"><span data-stu-id="89318-104">SYNTAX</span></span>

### <span data-ttu-id="89318-105">ByCapacityOrResourceGroupOrSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="89318-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89318-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="89318-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89318-107">說明</span><span class="sxs-lookup"><span data-stu-id="89318-107">DESCRIPTION</span></span>
<span data-ttu-id="89318-108">Get-AzPowerBIEmbeddedCapacity Cmdlet 會取得 PowerBI 內嵌容量的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89318-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="89318-109">示例</span><span class="sxs-lookup"><span data-stu-id="89318-109">EXAMPLES</span></span>

### <span data-ttu-id="89318-110">範例1：取得資源群組容量</span><span class="sxs-lookup"><span data-stu-id="89318-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="89318-111">這個命令會在名為 testRG 的資源群組中取得所有的 Azure PowerBI 內嵌容量</span><span class="sxs-lookup"><span data-stu-id="89318-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="89318-112">範例2：取得容量</span><span class="sxs-lookup"><span data-stu-id="89318-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="89318-113">這個命令會在名為 testRG 的資源群組中，取得名為 testcapacity 的 Azure PowerBI 內嵌的容量。</span><span class="sxs-lookup"><span data-stu-id="89318-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="89318-114">參數</span><span class="sxs-lookup"><span data-stu-id="89318-114">PARAMETERS</span></span>

### <span data-ttu-id="89318-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89318-115">-DefaultProfile</span></span>
<span data-ttu-id="89318-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89318-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89318-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="89318-117">-Name</span></span>
<span data-ttu-id="89318-118">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="89318-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="89318-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89318-119">-ResourceGroupName</span></span>
<span data-ttu-id="89318-120">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="89318-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="89318-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89318-121">-ResourceId</span></span>
<span data-ttu-id="89318-122">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="89318-122">Azure resource ID</span></span>

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

### <span data-ttu-id="89318-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89318-123">CommonParameters</span></span>
<span data-ttu-id="89318-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89318-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89318-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89318-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89318-126">輸入</span><span class="sxs-lookup"><span data-stu-id="89318-126">INPUTS</span></span>

### <span data-ttu-id="89318-127">System.object</span><span class="sxs-lookup"><span data-stu-id="89318-127">System.String</span></span>

## <span data-ttu-id="89318-128">輸出</span><span class="sxs-lookup"><span data-stu-id="89318-128">OUTPUTS</span></span>

### <span data-ttu-id="89318-129">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="89318-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="89318-130">筆記</span><span class="sxs-lookup"><span data-stu-id="89318-130">NOTES</span></span>

## <span data-ttu-id="89318-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="89318-131">RELATED LINKS</span></span>

[<span data-ttu-id="89318-132">新-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="89318-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="89318-133">移除-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="89318-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)