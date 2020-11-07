---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 794f432b06c693d6758603975a98ca6b2f5e3511
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794346"
---
# <span data-ttu-id="930f3-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="930f3-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="930f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="930f3-102">SYNOPSIS</span></span>
<span data-ttu-id="930f3-103">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="930f3-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="930f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="930f3-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="930f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="930f3-105">DESCRIPTION</span></span>
<span data-ttu-id="930f3-106">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="930f3-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="930f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="930f3-107">EXAMPLES</span></span>

### <span data-ttu-id="930f3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="930f3-108">Example 1</span></span>
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

<span data-ttu-id="930f3-109">傳回支援之 VPN 裝置品牌、型號及固件版本的清單：</span><span class="sxs-lookup"><span data-stu-id="930f3-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="930f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="930f3-110">PARAMETERS</span></span>

### <span data-ttu-id="930f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930f3-111">-DefaultProfile</span></span>
<span data-ttu-id="930f3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="930f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="930f3-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="930f3-113">-Name</span></span>
<span data-ttu-id="930f3-114">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="930f3-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="930f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="930f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="930f3-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="930f3-116">The resource group name.</span></span>

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

### <span data-ttu-id="930f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930f3-117">CommonParameters</span></span>
<span data-ttu-id="930f3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="930f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930f3-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="930f3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930f3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="930f3-120">INPUTS</span></span>

### <span data-ttu-id="930f3-121">System.object</span><span class="sxs-lookup"><span data-stu-id="930f3-121">System.String</span></span>

## <span data-ttu-id="930f3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="930f3-122">OUTPUTS</span></span>

### <span data-ttu-id="930f3-123">System.object</span><span class="sxs-lookup"><span data-stu-id="930f3-123">System.String</span></span>

## <span data-ttu-id="930f3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="930f3-124">NOTES</span></span>

## <span data-ttu-id="930f3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="930f3-125">RELATED LINKS</span></span>

