---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: d739741333f0c50da237fc29d96ac2dd02435280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903474"
---
# <span data-ttu-id="56deb-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="56deb-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="56deb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56deb-102">SYNOPSIS</span></span>
<span data-ttu-id="56deb-103">建立外部弧線伺服器組</span><span class="sxs-lookup"><span data-stu-id="56deb-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="56deb-104">語法</span><span class="sxs-lookup"><span data-stu-id="56deb-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56deb-105">描述</span><span class="sxs-lookup"><span data-stu-id="56deb-105">DESCRIPTION</span></span>
<span data-ttu-id="56deb-106">Cmdlet New-AzRadiusServer建立外部弧線伺服器組配置，以用於虛擬網路閘道和 VPN 伺服器組配置。</span><span class="sxs-lookup"><span data-stu-id="56deb-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="56deb-107">例子</span><span class="sxs-lookup"><span data-stu-id="56deb-107">EXAMPLES</span></span>

### <span data-ttu-id="56deb-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="56deb-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="56deb-109">建立多個外部弧線伺服器組配置，以用於新虛擬網路閘道上的 P2S。</span><span class="sxs-lookup"><span data-stu-id="56deb-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="56deb-110">參數</span><span class="sxs-lookup"><span data-stu-id="56deb-110">PARAMETERS</span></span>

### <span data-ttu-id="56deb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56deb-111">-DefaultProfile</span></span>
<span data-ttu-id="56deb-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56deb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56deb-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="56deb-113">-RadiusServerAddress</span></span>
<span data-ttu-id="56deb-114">外部弧線伺服器位址</span><span class="sxs-lookup"><span data-stu-id="56deb-114">External radius server address</span></span>

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

### <span data-ttu-id="56deb-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="56deb-115">-RadiusServerScore</span></span>
<span data-ttu-id="56deb-116">外部弧線伺服器分數</span><span class="sxs-lookup"><span data-stu-id="56deb-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56deb-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="56deb-117">-RadiusServerSecret</span></span>
<span data-ttu-id="56deb-118">外部弧線伺服器機密</span><span class="sxs-lookup"><span data-stu-id="56deb-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56deb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56deb-119">CommonParameters</span></span>
<span data-ttu-id="56deb-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56deb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56deb-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56deb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56deb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="56deb-122">INPUTS</span></span>

### <span data-ttu-id="56deb-123">System.String</span><span class="sxs-lookup"><span data-stu-id="56deb-123">System.String</span></span>

### <span data-ttu-id="56deb-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="56deb-124">System.Security.SecureString</span></span>

### <span data-ttu-id="56deb-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="56deb-125">System.Int32</span></span>

## <span data-ttu-id="56deb-126">輸出</span><span class="sxs-lookup"><span data-stu-id="56deb-126">OUTPUTS</span></span>

### <span data-ttu-id="56deb-127">Microsoft.Azure.Commands.Network.models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="56deb-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="56deb-128">筆記</span><span class="sxs-lookup"><span data-stu-id="56deb-128">NOTES</span></span>

## <span data-ttu-id="56deb-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="56deb-129">RELATED LINKS</span></span>
