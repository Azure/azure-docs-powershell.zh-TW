---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 0ff95b3e212e61b3d8c9d01b0ad745963d7b24e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621914"
---
# <span data-ttu-id="054de-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="054de-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="054de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="054de-102">SYNOPSIS</span></span>
<span data-ttu-id="054de-103">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="054de-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="054de-104">句法</span><span class="sxs-lookup"><span data-stu-id="054de-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="054de-105">說明</span><span class="sxs-lookup"><span data-stu-id="054de-105">DESCRIPTION</span></span>
<span data-ttu-id="054de-106">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="054de-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="054de-107">示例</span><span class="sxs-lookup"><span data-stu-id="054de-107">EXAMPLES</span></span>

### <span data-ttu-id="054de-108">範例1</span><span class="sxs-lookup"><span data-stu-id="054de-108">Example 1</span></span>
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

<span data-ttu-id="054de-109">傳回支援之 VPN 裝置品牌、型號及固件版本的清單：</span><span class="sxs-lookup"><span data-stu-id="054de-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="054de-110">參數</span><span class="sxs-lookup"><span data-stu-id="054de-110">PARAMETERS</span></span>

### <span data-ttu-id="054de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="054de-111">-DefaultProfile</span></span>
<span data-ttu-id="054de-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="054de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="054de-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="054de-113">-Name</span></span>
<span data-ttu-id="054de-114">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="054de-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="054de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="054de-115">-ResourceGroupName</span></span>
<span data-ttu-id="054de-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="054de-116">The resource group name.</span></span>

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

### <span data-ttu-id="054de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054de-117">CommonParameters</span></span>
<span data-ttu-id="054de-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="054de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="054de-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="054de-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054de-120">輸入</span><span class="sxs-lookup"><span data-stu-id="054de-120">INPUTS</span></span>

### <span data-ttu-id="054de-121">System.object</span><span class="sxs-lookup"><span data-stu-id="054de-121">System.String</span></span>

## <span data-ttu-id="054de-122">輸出</span><span class="sxs-lookup"><span data-stu-id="054de-122">OUTPUTS</span></span>

### <span data-ttu-id="054de-123">System.object</span><span class="sxs-lookup"><span data-stu-id="054de-123">System.String</span></span>

## <span data-ttu-id="054de-124">筆記</span><span class="sxs-lookup"><span data-stu-id="054de-124">NOTES</span></span>

## <span data-ttu-id="054de-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="054de-125">RELATED LINKS</span></span>
