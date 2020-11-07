---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623697"
---
# <span data-ttu-id="d1a1c-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d1a1c-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d1a1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a1c-103">取得 PowerBI 內嵌容量的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1a1c-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1a1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1a1c-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="d1a1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a1c-106">Get-AzureRmPowerBIEmbeddedCapacity Cmdlet 會取得 PowerBI 內嵌容量的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1a1c-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d1a1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="d1a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="d1a1c-108">範例1：取得資源群組容量</span><span class="sxs-lookup"><span data-stu-id="d1a1c-108">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="d1a1c-109">這個命令會在名為 testRG 的資源群組中取得所有的 Azure PowerBI 內嵌容量</span><span class="sxs-lookup"><span data-stu-id="d1a1c-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="d1a1c-110">範例2：取得容量</span><span class="sxs-lookup"><span data-stu-id="d1a1c-110">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="d1a1c-111">這個命令會在名為 testRG 的資源群組中，取得名為 testcapacity 的 Azure PowerBI 內嵌的容量。</span><span class="sxs-lookup"><span data-stu-id="d1a1c-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="d1a1c-112">參數</span><span class="sxs-lookup"><span data-stu-id="d1a1c-112">PARAMETERS</span></span>

### <span data-ttu-id="d1a1c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a1c-113">-ResourceGroupName</span></span>
<span data-ttu-id="d1a1c-114">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d1a1c-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1a1c-115">-Name</span></span>
<span data-ttu-id="d1a1c-116">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="d1a1c-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1a1c-117">-ResourceId</span></span>
<span data-ttu-id="d1a1c-118">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d1a1c-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a1c-119">CommonParameters</span></span>
<span data-ttu-id="d1a1c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1a1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a1c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1a1c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a1c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d1a1c-122">INPUTS</span></span>

### <span data-ttu-id="d1a1c-123">所有</span><span class="sxs-lookup"><span data-stu-id="d1a1c-123">None</span></span>
<span data-ttu-id="d1a1c-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d1a1c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1a1c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="d1a1c-125">OUTPUTS</span></span>

### <span data-ttu-id="d1a1c-126">PSPowerBIEmbeddedCapacity><的 [清單]</span><span class="sxs-lookup"><span data-stu-id="d1a1c-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="d1a1c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="d1a1c-127">NOTES</span></span>

## <span data-ttu-id="d1a1c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1a1c-128">RELATED LINKS</span></span>

[<span data-ttu-id="d1a1c-129">新-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="d1a1c-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d1a1c-130">移除-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="d1a1c-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
