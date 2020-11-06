---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 9ec81a9cf82851905d308fa0e0dd1fa45aeb7af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447745"
---
# <span data-ttu-id="b1eb7-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="b1eb7-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="b1eb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="b1eb7-103">為虛擬網路閘道設定 VPN 用戶端位址集區。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1eb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1eb7-104">SYNTAX</span></span>

### <span data-ttu-id="b1eb7-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b1eb7-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1eb7-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1eb7-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1eb7-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1eb7-107">DESCRIPTION</span></span>
<span data-ttu-id="b1eb7-108">AzureRmVirtualNetworkVpnClientConfig Cmdlet 會為虛擬網路閘道 **設定** 用戶端位址集區。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="b1eb7-109">虛擬私人網路絡 (VPN) 連線至此閘道的用戶端，都會從該位址集區中指派 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="b1eb7-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1eb7-110">EXAMPLES</span></span>

### <span data-ttu-id="b1eb7-111">範例1：將 VPN 用戶端位址集區指派給虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="b1eb7-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="b1eb7-112">這個範例會將 VPN 用戶端位址集區指派給名為 ContosoVirtualGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="b1eb7-113">第一個命令會建立閘道的物件參照，而物件會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="b1eb7-114">接著，這個範例中的第二個命令會使用 **AzureRmVirtualNetworkGatewayVpnClientConfig** Cmdlet 來指派位址集區 10.0.0.0/16 到 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="b1eb7-115">範例2：在現有閘道設定外部 radius 驗證</span><span class="sxs-lookup"><span data-stu-id="b1eb7-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="b1eb7-116">這個範例會將 VPN 用戶端位址集區指派給名為 ContosoVirtualGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="b1eb7-117">第一個命令會建立閘道的物件參照，而物件會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="b1eb7-118">接著，這個範例中的第二個命令會使用 **AzureRmVirtualNetworkGatewayVpnClientConfig** Cmdlet 來指派位址集區 10.0.0.0/16 到 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="b1eb7-119">它也會將外部 radius 伺服器「TestRadiusServer」設定為用於 vpn 用戶端的驗證。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="b1eb7-120">參數</span><span class="sxs-lookup"><span data-stu-id="b1eb7-120">PARAMETERS</span></span>

### <span data-ttu-id="b1eb7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1eb7-121">-DefaultProfile</span></span>
<span data-ttu-id="b1eb7-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1eb7-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b1eb7-123">-RadiusServerAddress</span></span>
<span data-ttu-id="b1eb7-124">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-124">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb7-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b1eb7-125">-RadiusServerSecret</span></span>
<span data-ttu-id="b1eb7-126">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-126">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb7-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1eb7-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b1eb7-128">指定包含此 Cmdlet 所修改之 VPN 用戶端配置設定的虛擬網路閘道物件參照。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="b1eb7-129">您可以使用 Get-AzureRmVirtualNetworkGateway 並指定閘道的名稱，以建立虛擬閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb7-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="b1eb7-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="b1eb7-131">指定要指派給連接至此閘道之用戶端的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="b1eb7-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb7-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b1eb7-132">-Confirm</span></span>
<span data-ttu-id="b1eb7-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1eb7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1eb7-134">-WhatIf</span></span>
<span data-ttu-id="b1eb7-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1eb7-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1eb7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1eb7-137">CommonParameters</span></span>
<span data-ttu-id="b1eb7-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1eb7-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1eb7-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b1eb7-140">INPUTS</span></span>

###  
<span data-ttu-id="b1eb7-141">這個 Cmdlet 會接受 PSVirtualNetworkGateway 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b1eb7-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b1eb7-142">OUTPUTS</span></span>

###  
<span data-ttu-id="b1eb7-143">這個 Cmdlet 會修改 PSVirtualNetworkGateway 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。</span><span class="sxs-lookup"><span data-stu-id="b1eb7-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b1eb7-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b1eb7-144">NOTES</span></span>

## <span data-ttu-id="b1eb7-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1eb7-145">RELATED LINKS</span></span>

[<span data-ttu-id="b1eb7-146">AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="b1eb7-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="b1eb7-147">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1eb7-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b1eb7-148">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1eb7-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


