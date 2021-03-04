---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 45cb703d6fdc87238f4d1ed35ada90aadeed501b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910997"
---
# <span data-ttu-id="f2c18-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="f2c18-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="f2c18-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2c18-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c18-103">這個命令小程式會返回支援的 VPN 裝置品牌、型號和內文版本清單。</span><span class="sxs-lookup"><span data-stu-id="f2c18-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f2c18-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2c18-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c18-105">描述</span><span class="sxs-lookup"><span data-stu-id="f2c18-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c18-106">這個命令小程式會返回支援的 VPN 裝置品牌、型號和內文版本清單。</span><span class="sxs-lookup"><span data-stu-id="f2c18-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f2c18-107">例子</span><span class="sxs-lookup"><span data-stu-id="f2c18-107">EXAMPLES</span></span>

### <span data-ttu-id="f2c18-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2c18-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="f2c18-109">會返回支援的 VPN 裝置品牌、型號和內文版本清單：</span><span class="sxs-lookup"><span data-stu-id="f2c18-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="f2c18-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2c18-110">PARAMETERS</span></span>

### <span data-ttu-id="f2c18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c18-111">-DefaultProfile</span></span>
<span data-ttu-id="f2c18-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2c18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c18-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2c18-113">-Name</span></span>
<span data-ttu-id="f2c18-114">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="f2c18-114">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c18-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c18-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2c18-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2c18-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c18-117">CommonParameters</span></span>
<span data-ttu-id="f2c18-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2c18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c18-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2c18-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c18-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f2c18-120">INPUTS</span></span>

### <span data-ttu-id="f2c18-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f2c18-121">System.String</span></span>

## <span data-ttu-id="f2c18-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f2c18-122">OUTPUTS</span></span>

### <span data-ttu-id="f2c18-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f2c18-123">System.String</span></span>

## <span data-ttu-id="f2c18-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f2c18-124">NOTES</span></span>

## <span data-ttu-id="f2c18-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2c18-125">RELATED LINKS</span></span>
