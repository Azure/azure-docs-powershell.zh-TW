---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908494"
---
# <span data-ttu-id="a9c80-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="a9c80-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="a9c80-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9c80-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c80-103">這個命令小程式會採用連接資源、VPN 裝置品牌、型號、硬體版本，並退回客戶可直接在內部部署 VPN 裝置上所對應的組程腳本。</span><span class="sxs-lookup"><span data-stu-id="a9c80-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="a9c80-104">腳本會遵循所選裝置語法，並填入必要的參數，例如 Azure 閘道公用 IP 位址、虛擬網路位址首碼、VPN 內建預先共用金鑰等，讓客戶只要複製貼上到他們的 VPN 裝置設定。</span><span class="sxs-lookup"><span data-stu-id="a9c80-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="a9c80-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9c80-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c80-106">描述</span><span class="sxs-lookup"><span data-stu-id="a9c80-106">DESCRIPTION</span></span>
<span data-ttu-id="a9c80-107">這個命令小程式會採用連接資源、VPN 裝置品牌、型號、硬體版本，並退回客戶可直接在內部部署 VPN 裝置上所對應的組程腳本。</span><span class="sxs-lookup"><span data-stu-id="a9c80-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="a9c80-108">腳本會遵循所選裝置語法，並填入必要的參數，例如 Azure 閘道公用 IP 位址、虛擬網路位址首碼、VPN 內建預先共用金鑰等，讓客戶只要複製貼上到他們的 VPN 裝置設定。</span><span class="sxs-lookup"><span data-stu-id="a9c80-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="a9c80-109">例子</span><span class="sxs-lookup"><span data-stu-id="a9c80-109">EXAMPLES</span></span>

### <span data-ttu-id="a9c80-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9c80-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="a9c80-111">上述範例使用Get-AzVirtualNetworkGatewaySupportedVpnDevice取得支援的 VPN 裝置品牌、型號和內文版本。</span><span class="sxs-lookup"><span data-stu-id="a9c80-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="a9c80-112">然後使用其中一個返回的模型資訊，為 VirtualNetworkGatewayConnection"TestConnection"產生 VPN 裝置組組腳本。</span><span class="sxs-lookup"><span data-stu-id="a9c80-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="a9c80-113">此範例中使用的裝置有 DeviceFamily "IOS-Test"、DeviceVendor "Cisco-Test" 和 FirmwareVersion 20。</span><span class="sxs-lookup"><span data-stu-id="a9c80-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="a9c80-114">參數</span><span class="sxs-lookup"><span data-stu-id="a9c80-114">PARAMETERS</span></span>

### <span data-ttu-id="a9c80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c80-115">-DefaultProfile</span></span>
<span data-ttu-id="a9c80-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9c80-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9c80-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="a9c80-117">-DeviceFamily</span></span>
<span data-ttu-id="a9c80-118">VPN 裝置型號/系列的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c80-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="a9c80-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="a9c80-119">-DeviceVendor</span></span>
<span data-ttu-id="a9c80-120">VPN 裝置廠商的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c80-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="a9c80-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="a9c80-121">-FirmwareVersion</span></span>
<span data-ttu-id="a9c80-122">VPN 裝置之內文的內文版本。</span><span class="sxs-lookup"><span data-stu-id="a9c80-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="a9c80-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9c80-123">-Name</span></span>
<span data-ttu-id="a9c80-124">要產生組配置的連接資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c80-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="a9c80-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c80-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9c80-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a9c80-126">The resource group name.</span></span>

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

### <span data-ttu-id="a9c80-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a9c80-127">-Confirm</span></span>
<span data-ttu-id="a9c80-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a9c80-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c80-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c80-129">-WhatIf</span></span>
<span data-ttu-id="a9c80-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9c80-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c80-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9c80-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c80-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c80-132">CommonParameters</span></span>
<span data-ttu-id="a9c80-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9c80-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c80-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9c80-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c80-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a9c80-135">INPUTS</span></span>

### <span data-ttu-id="a9c80-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a9c80-136">System.String</span></span>

## <span data-ttu-id="a9c80-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a9c80-137">OUTPUTS</span></span>

### <span data-ttu-id="a9c80-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a9c80-138">System.String</span></span>

## <span data-ttu-id="a9c80-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a9c80-139">NOTES</span></span>

## <span data-ttu-id="a9c80-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9c80-140">RELATED LINKS</span></span>
