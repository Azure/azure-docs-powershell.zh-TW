---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448292"
---
# <span data-ttu-id="334f9-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="334f9-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="334f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="334f9-102">SYNOPSIS</span></span>
<span data-ttu-id="334f9-103">為虛擬網路閘道設定 VPN 用戶端位址集區。</span><span class="sxs-lookup"><span data-stu-id="334f9-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="334f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="334f9-104">SYNTAX</span></span>

### <span data-ttu-id="334f9-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="334f9-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334f9-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="334f9-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="334f9-107">說明</span><span class="sxs-lookup"><span data-stu-id="334f9-107">DESCRIPTION</span></span>
<span data-ttu-id="334f9-108">AzureRmVirtualNetworkVpnClientConfig Cmdlet 會為虛擬網路閘道 **設定** 用戶端位址集區。</span><span class="sxs-lookup"><span data-stu-id="334f9-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="334f9-109">虛擬私人網路絡 (VPN) 連線至此閘道的用戶端，都會從該位址集區中指派 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="334f9-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="334f9-110">示例</span><span class="sxs-lookup"><span data-stu-id="334f9-110">EXAMPLES</span></span>

### <span data-ttu-id="334f9-111">範例1：將 VPN 用戶端位址集區指派給虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="334f9-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="334f9-112">這個範例會將 VPN 用戶端位址集區指派給名為 ContosoVirtualGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="334f9-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="334f9-113">第一個命令會建立閘道的物件參照，而物件會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="334f9-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="334f9-114">接著，這個範例中的第二個命令會使用 **AzureRmVirtualNetworkGatewayVpnClientConfig** Cmdlet 來指派位址集區 10.0.0.0/16 到 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="334f9-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="334f9-115">範例2：在現有閘道設定外部 radius 驗證</span><span class="sxs-lookup"><span data-stu-id="334f9-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="334f9-116">這個範例會將 VPN 用戶端位址集區指派給名為 ContosoVirtualGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="334f9-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="334f9-117">第一個命令會建立閘道的物件參照，而物件會儲存在名為 $Gateway 的變數中。</span><span class="sxs-lookup"><span data-stu-id="334f9-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="334f9-118">接著，這個範例中的第二個命令會使用 **AzureRmVirtualNetworkGatewayVpnClientConfig** Cmdlet 來指派位址集區 10.0.0.0/16 到 ContosoVirtualGateway。</span><span class="sxs-lookup"><span data-stu-id="334f9-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="334f9-119">它也會將外部 radius 伺服器「TestRadiusServer」設定為用於 vpn 用戶端的驗證。</span><span class="sxs-lookup"><span data-stu-id="334f9-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="334f9-120">參數</span><span class="sxs-lookup"><span data-stu-id="334f9-120">PARAMETERS</span></span>

### <span data-ttu-id="334f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334f9-121">-DefaultProfile</span></span>
<span data-ttu-id="334f9-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="334f9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="334f9-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="334f9-123">-RadiusServerAddress</span></span>
<span data-ttu-id="334f9-124">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="334f9-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334f9-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="334f9-125">-RadiusServerSecret</span></span>
<span data-ttu-id="334f9-126">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="334f9-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334f9-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="334f9-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="334f9-128">指定包含此 Cmdlet 所修改之 VPN 用戶端配置設定的虛擬網路閘道物件參照。</span><span class="sxs-lookup"><span data-stu-id="334f9-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="334f9-129">您可以使用 Get-AzureRmVirtualNetworkGateway 並指定閘道的名稱，以建立虛擬閘道的物件參考。</span><span class="sxs-lookup"><span data-stu-id="334f9-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="334f9-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="334f9-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="334f9-131">指定要指派給連接至此閘道之用戶端的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="334f9-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="334f9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="334f9-132">-Confirm</span></span>
<span data-ttu-id="334f9-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="334f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="334f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="334f9-134">-WhatIf</span></span>
<span data-ttu-id="334f9-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="334f9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="334f9-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="334f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="334f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334f9-137">CommonParameters</span></span>
<span data-ttu-id="334f9-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="334f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334f9-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="334f9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334f9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="334f9-140">INPUTS</span></span>

### <span data-ttu-id="334f9-141">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="334f9-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="334f9-142">參數： VirtualNetworkGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="334f9-142">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="334f9-143">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="334f9-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="334f9-144">System.object</span><span class="sxs-lookup"><span data-stu-id="334f9-144">System.String</span></span>

### <span data-ttu-id="334f9-145">SecureString</span><span class="sxs-lookup"><span data-stu-id="334f9-145">System.Security.SecureString</span></span>

## <span data-ttu-id="334f9-146">輸出</span><span class="sxs-lookup"><span data-stu-id="334f9-146">OUTPUTS</span></span>

### <span data-ttu-id="334f9-147">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="334f9-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="334f9-148">筆記</span><span class="sxs-lookup"><span data-stu-id="334f9-148">NOTES</span></span>

## <span data-ttu-id="334f9-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="334f9-149">RELATED LINKS</span></span>

[<span data-ttu-id="334f9-150">AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="334f9-150">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="334f9-151">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="334f9-151">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="334f9-152">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="334f9-152">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


