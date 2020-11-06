---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 97c832994e39707c0d45963eda856028589d4b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451139"
---
# <span data-ttu-id="bd67a-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="bd67a-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="bd67a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd67a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd67a-103">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="bd67a-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd67a-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd67a-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd67a-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd67a-105">DESCRIPTION</span></span>
<span data-ttu-id="bd67a-106">這個 commandlet 會傳回受支援之 VPN 裝置品牌、模型及固件版本的清單。</span><span class="sxs-lookup"><span data-stu-id="bd67a-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="bd67a-107">示例</span><span class="sxs-lookup"><span data-stu-id="bd67a-107">EXAMPLES</span></span>

### <span data-ttu-id="bd67a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bd67a-108">Example 1</span></span>
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

<span data-ttu-id="bd67a-109">傳回支援之 VPN 裝置品牌、型號及固件版本的清單：</span><span class="sxs-lookup"><span data-stu-id="bd67a-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="bd67a-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd67a-110">PARAMETERS</span></span>

### <span data-ttu-id="bd67a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd67a-111">-DefaultProfile</span></span>
<span data-ttu-id="bd67a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd67a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd67a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd67a-113">-Name</span></span>
<span data-ttu-id="bd67a-114">虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="bd67a-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="bd67a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd67a-115">-ResourceGroupName</span></span>
<span data-ttu-id="bd67a-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd67a-116">The resource group name.</span></span>

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

### <span data-ttu-id="bd67a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd67a-117">CommonParameters</span></span>
<span data-ttu-id="bd67a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd67a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd67a-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd67a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd67a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bd67a-120">INPUTS</span></span>

### <span data-ttu-id="bd67a-121">System.object</span><span class="sxs-lookup"><span data-stu-id="bd67a-121">System.String</span></span>

## <span data-ttu-id="bd67a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="bd67a-122">OUTPUTS</span></span>

### <span data-ttu-id="bd67a-123">System.object</span><span class="sxs-lookup"><span data-stu-id="bd67a-123">System.String</span></span>

## <span data-ttu-id="bd67a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="bd67a-124">NOTES</span></span>

## <span data-ttu-id="bd67a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd67a-125">RELATED LINKS</span></span>
