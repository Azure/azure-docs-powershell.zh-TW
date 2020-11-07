---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
ms.openlocfilehash: 46eccff9ad7b4fc525a864eab4c4477df4503dc2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800841"
---
# <span data-ttu-id="077e9-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="077e9-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="077e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="077e9-102">SYNOPSIS</span></span>
<span data-ttu-id="077e9-103">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="077e9-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="077e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="077e9-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="077e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="077e9-105">DESCRIPTION</span></span>
<span data-ttu-id="077e9-106">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="077e9-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="077e9-107">示例</span><span class="sxs-lookup"><span data-stu-id="077e9-107">EXAMPLES</span></span>

### <span data-ttu-id="077e9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="077e9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="077e9-109">傳回支援之 VPN 裝置品牌、型號及固件版本的清單：</span><span class="sxs-lookup"><span data-stu-id="077e9-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="077e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="077e9-110">PARAMETERS</span></span>

### <span data-ttu-id="077e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077e9-111">-DefaultProfile</span></span>
<span data-ttu-id="077e9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="077e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="077e9-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="077e9-113">-Name</span></span>
<span data-ttu-id="077e9-114">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="077e9-114">The virtual network gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077e9-115">-ResourceGroupName</span></span>
<span data-ttu-id="077e9-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="077e9-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077e9-117">CommonParameters</span></span>
<span data-ttu-id="077e9-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="077e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077e9-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="077e9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077e9-120">輸入</span><span class="sxs-lookup"><span data-stu-id="077e9-120">INPUTS</span></span>

### <span data-ttu-id="077e9-121">System.object</span><span class="sxs-lookup"><span data-stu-id="077e9-121">System.String</span></span>

## <span data-ttu-id="077e9-122">輸出</span><span class="sxs-lookup"><span data-stu-id="077e9-122">OUTPUTS</span></span>

### <span data-ttu-id="077e9-123">System.object</span><span class="sxs-lookup"><span data-stu-id="077e9-123">System.String</span></span>

## <span data-ttu-id="077e9-124">筆記</span><span class="sxs-lookup"><span data-stu-id="077e9-124">NOTES</span></span>

## <span data-ttu-id="077e9-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="077e9-125">RELATED LINKS</span></span>

