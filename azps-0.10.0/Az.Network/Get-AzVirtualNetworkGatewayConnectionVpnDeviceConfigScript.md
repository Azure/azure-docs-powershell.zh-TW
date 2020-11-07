---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 3d955b2133f4a262b69de1413c5a4bf4d8e719b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794348"
---
# <span data-ttu-id="1129e-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="1129e-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="1129e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1129e-102">SYNOPSIS</span></span>
<span data-ttu-id="1129e-103">這個 commandlet 會採用連線資源、VPN 裝置品牌、模型、固件版本，並傳回客戶可以直接在其內部部署 VPN 裝置上套用的對應配置腳本。</span><span class="sxs-lookup"><span data-stu-id="1129e-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="1129e-104">此腳本將遵循所選裝置的語法，並填入 Azure 閘道公用 IP 位址、虛擬網路位址首碼、VPN 隧道預共用金鑰等所需的參數。客戶只需複製並貼上到其 VPN 裝置設定。</span><span class="sxs-lookup"><span data-stu-id="1129e-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="1129e-105">句法</span><span class="sxs-lookup"><span data-stu-id="1129e-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1129e-106">說明</span><span class="sxs-lookup"><span data-stu-id="1129e-106">DESCRIPTION</span></span>
<span data-ttu-id="1129e-107">這個 commandlet 會採用連線資源、VPN 裝置品牌、模型、固件版本，並傳回客戶可以直接在其內部部署 VPN 裝置上套用的對應配置腳本。</span><span class="sxs-lookup"><span data-stu-id="1129e-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="1129e-108">此腳本將遵循所選裝置的語法，並填入 Azure 閘道公用 IP 位址、虛擬網路位址首碼、VPN 隧道預共用金鑰等所需的參數。客戶只需複製並貼上到其 VPN 裝置設定。</span><span class="sxs-lookup"><span data-stu-id="1129e-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="1129e-109">示例</span><span class="sxs-lookup"><span data-stu-id="1129e-109">EXAMPLES</span></span>

### <span data-ttu-id="1129e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1129e-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="1129e-111">上述範例使用 Get-AzVirtualNetworkGatewaySupportedVpnDevice 來取得支援的 VPN 裝置品牌、模型及固件版本。</span><span class="sxs-lookup"><span data-stu-id="1129e-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="1129e-112">然後使用傳回的其中一個模型資訊，為 VirtualNetworkGatewayConnection "TestConnection" 產生 VPN 裝置配置腳本。</span><span class="sxs-lookup"><span data-stu-id="1129e-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="1129e-113">這個範例中所用的裝置已 DeviceFamily 「IOS-Test」、DeviceVendor 「Cisco-Test」和 FirmwareVersion 20。</span><span class="sxs-lookup"><span data-stu-id="1129e-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="1129e-114">參數</span><span class="sxs-lookup"><span data-stu-id="1129e-114">PARAMETERS</span></span>

### <span data-ttu-id="1129e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1129e-115">-DefaultProfile</span></span>
<span data-ttu-id="1129e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1129e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1129e-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="1129e-117">-DeviceFamily</span></span>
<span data-ttu-id="1129e-118">VPN 裝置模型/系列的名稱。</span><span class="sxs-lookup"><span data-stu-id="1129e-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="1129e-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="1129e-119">-DeviceVendor</span></span>
<span data-ttu-id="1129e-120">VPN 裝置廠商的名稱。</span><span class="sxs-lookup"><span data-stu-id="1129e-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="1129e-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="1129e-121">-FirmwareVersion</span></span>
<span data-ttu-id="1129e-122">VPN 裝置的固件版本。</span><span class="sxs-lookup"><span data-stu-id="1129e-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="1129e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1129e-123">-Name</span></span>
<span data-ttu-id="1129e-124">要產生設定之連接的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1129e-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="1129e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1129e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1129e-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1129e-126">The resource group name.</span></span>

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

### <span data-ttu-id="1129e-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1129e-127">-Confirm</span></span>
<span data-ttu-id="1129e-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1129e-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1129e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1129e-129">-WhatIf</span></span>
<span data-ttu-id="1129e-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1129e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1129e-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1129e-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1129e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1129e-132">CommonParameters</span></span>
<span data-ttu-id="1129e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1129e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1129e-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1129e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1129e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1129e-135">INPUTS</span></span>

### <span data-ttu-id="1129e-136">System.object</span><span class="sxs-lookup"><span data-stu-id="1129e-136">System.String</span></span>

## <span data-ttu-id="1129e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1129e-137">OUTPUTS</span></span>

### <span data-ttu-id="1129e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1129e-138">System.String</span></span>

## <span data-ttu-id="1129e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1129e-139">NOTES</span></span>

## <span data-ttu-id="1129e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1129e-140">RELATED LINKS</span></span>

