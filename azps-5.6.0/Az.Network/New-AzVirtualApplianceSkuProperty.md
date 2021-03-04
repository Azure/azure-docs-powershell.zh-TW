---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915998"
---
# <span data-ttu-id="a9f08-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="a9f08-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="a9f08-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9f08-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f08-103">定義資源的網路虛擬裝置 SKU。</span><span class="sxs-lookup"><span data-stu-id="a9f08-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="a9f08-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9f08-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f08-105">描述</span><span class="sxs-lookup"><span data-stu-id="a9f08-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f08-106">命令New-AzVirtualApplianceSkuProperties定義網路虛擬裝置資源的 SKU。</span><span class="sxs-lookup"><span data-stu-id="a9f08-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a9f08-107">例子</span><span class="sxs-lookup"><span data-stu-id="a9f08-107">EXAMPLES</span></span>

### <span data-ttu-id="a9f08-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9f08-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="a9f08-109">建立虛擬裝置 SKU 屬性物件，以用於New-AzNetworkVirtualAppliance命令。</span><span class="sxs-lookup"><span data-stu-id="a9f08-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="a9f08-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9f08-110">PARAMETERS</span></span>

### <span data-ttu-id="a9f08-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a9f08-111">-BundledScaleUnit</span></span>
<span data-ttu-id="a9f08-112">已組合的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="a9f08-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="a9f08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f08-113">-DefaultProfile</span></span>
<span data-ttu-id="a9f08-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9f08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f08-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="a9f08-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="a9f08-116">市場位置版本。</span><span class="sxs-lookup"><span data-stu-id="a9f08-116">The market place version.</span></span>

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

### <span data-ttu-id="a9f08-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="a9f08-117">-VendorName</span></span>
<span data-ttu-id="a9f08-118">廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f08-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f08-119">CommonParameters</span></span>
<span data-ttu-id="a9f08-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9f08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f08-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9f08-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f08-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a9f08-122">INPUTS</span></span>

### <span data-ttu-id="a9f08-123">沒有</span><span class="sxs-lookup"><span data-stu-id="a9f08-123">None</span></span>

## <span data-ttu-id="a9f08-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a9f08-124">OUTPUTS</span></span>

### <span data-ttu-id="a9f08-125">Microsoft.Azure.Commands.Network.models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="a9f08-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="a9f08-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a9f08-126">NOTES</span></span>

## <span data-ttu-id="a9f08-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9f08-127">RELATED LINKS</span></span>
