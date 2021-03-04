---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e165b481b1321f5ddd81766452120f55f6f0e153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902554"
---
# <span data-ttu-id="10714-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="10714-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="10714-102">簡介</span><span class="sxs-lookup"><span data-stu-id="10714-102">SYNOPSIS</span></span>
<span data-ttu-id="10714-103">取得或列出庫存中可用的網路虛擬裝置 SKU。</span><span class="sxs-lookup"><span data-stu-id="10714-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="10714-104">語法</span><span class="sxs-lookup"><span data-stu-id="10714-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10714-105">描述</span><span class="sxs-lookup"><span data-stu-id="10714-105">DESCRIPTION</span></span>
<span data-ttu-id="10714-106">此Get-AzNetworkVirtualApplianceSku Microsoft Azure 庫存中可或列出可用的網路虛擬裝置 SKU。</span><span class="sxs-lookup"><span data-stu-id="10714-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="10714-107">例子</span><span class="sxs-lookup"><span data-stu-id="10714-107">EXAMPLES</span></span>

### <span data-ttu-id="10714-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="10714-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="10714-109">按名稱取得 SKU。</span><span class="sxs-lookup"><span data-stu-id="10714-109">Get a sku by name.</span></span>

### <span data-ttu-id="10714-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="10714-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="10714-111">列出所有可用的網路虛擬裝置 SKU。</span><span class="sxs-lookup"><span data-stu-id="10714-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="10714-112">參數</span><span class="sxs-lookup"><span data-stu-id="10714-112">PARAMETERS</span></span>

### <span data-ttu-id="10714-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10714-113">-DefaultProfile</span></span>
<span data-ttu-id="10714-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="10714-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10714-115">-SKUName</span><span class="sxs-lookup"><span data-stu-id="10714-115">-SkuName</span></span>
<span data-ttu-id="10714-116">SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="10714-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10714-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10714-117">CommonParameters</span></span>
<span data-ttu-id="10714-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="10714-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10714-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10714-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10714-120">輸入</span><span class="sxs-lookup"><span data-stu-id="10714-120">INPUTS</span></span>

### <span data-ttu-id="10714-121">沒有</span><span class="sxs-lookup"><span data-stu-id="10714-121">None</span></span>

## <span data-ttu-id="10714-122">輸出</span><span class="sxs-lookup"><span data-stu-id="10714-122">OUTPUTS</span></span>

### <span data-ttu-id="10714-123">Microsoft.Azure.Commands.Network.models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="10714-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="10714-124">筆記</span><span class="sxs-lookup"><span data-stu-id="10714-124">NOTES</span></span>

## <span data-ttu-id="10714-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="10714-125">RELATED LINKS</span></span>
