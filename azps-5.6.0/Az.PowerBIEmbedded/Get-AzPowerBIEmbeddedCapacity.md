---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 17d7547daaffdfafc117a250d20c0af1f069b70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902290"
---
# <span data-ttu-id="02d46-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="02d46-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="02d46-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02d46-102">SYNOPSIS</span></span>
<span data-ttu-id="02d46-103">瞭解 PowerBI 內嵌容量的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="02d46-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="02d46-104">語法</span><span class="sxs-lookup"><span data-stu-id="02d46-104">SYNTAX</span></span>

### <span data-ttu-id="02d46-105">BySourceOrResourceGroupOrSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="02d46-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02d46-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02d46-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02d46-107">描述</span><span class="sxs-lookup"><span data-stu-id="02d46-107">DESCRIPTION</span></span>
<span data-ttu-id="02d46-108">此Get-AzPowerBIEmbeddedCapacity Cmdlet 會獲得 PowerBI 內嵌容量的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="02d46-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="02d46-109">例子</span><span class="sxs-lookup"><span data-stu-id="02d46-109">EXAMPLES</span></span>

### <span data-ttu-id="02d46-110">範例 1：取得資源群組容量</span><span class="sxs-lookup"><span data-stu-id="02d46-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="02d46-111">此命令會獲得名為 testRG 的資源群組中所有的 Azure PowerBI 內嵌容量</span><span class="sxs-lookup"><span data-stu-id="02d46-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="02d46-112">範例 2：取得容量</span><span class="sxs-lookup"><span data-stu-id="02d46-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="02d46-113">此命令在名為 testRG 的資源群組中，會獲得名為 test一的 Azure PowerBI 內嵌容量。</span><span class="sxs-lookup"><span data-stu-id="02d46-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="02d46-114">參數</span><span class="sxs-lookup"><span data-stu-id="02d46-114">PARAMETERS</span></span>

### <span data-ttu-id="02d46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d46-115">-DefaultProfile</span></span>
<span data-ttu-id="02d46-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="02d46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02d46-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="02d46-117">-Name</span></span>
<span data-ttu-id="02d46-118">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="02d46-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="02d46-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d46-119">-ResourceGroupName</span></span>
<span data-ttu-id="02d46-120">容量所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="02d46-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="02d46-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02d46-121">-ResourceId</span></span>
<span data-ttu-id="02d46-122">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="02d46-122">Azure resource ID</span></span>

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

### <span data-ttu-id="02d46-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d46-123">CommonParameters</span></span>
<span data-ttu-id="02d46-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02d46-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d46-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="02d46-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d46-126">輸入</span><span class="sxs-lookup"><span data-stu-id="02d46-126">INPUTS</span></span>

### <span data-ttu-id="02d46-127">System.String</span><span class="sxs-lookup"><span data-stu-id="02d46-127">System.String</span></span>

## <span data-ttu-id="02d46-128">輸出</span><span class="sxs-lookup"><span data-stu-id="02d46-128">OUTPUTS</span></span>

### <span data-ttu-id="02d46-129">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="02d46-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="02d46-130">筆記</span><span class="sxs-lookup"><span data-stu-id="02d46-130">NOTES</span></span>

## <span data-ttu-id="02d46-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="02d46-131">RELATED LINKS</span></span>

[<span data-ttu-id="02d46-132">New-AzPowerBIEmbedded一切 </span><span class="sxs-lookup"><span data-stu-id="02d46-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="02d46-133">Remove-AzPowerBIEmbedded一切 </span><span class="sxs-lookup"><span data-stu-id="02d46-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
