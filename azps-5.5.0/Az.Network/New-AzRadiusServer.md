---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132523"
---
# <span data-ttu-id="6aa9b-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="6aa9b-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="6aa9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6aa9b-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa9b-103">建立外部 radius 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="6aa9b-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="6aa9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6aa9b-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aa9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6aa9b-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa9b-106">New-AzRadiusServer Cmdlet 會建立要在虛擬網路閘道和 VPN 伺服器設定中使用的外部 radius 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="6aa9b-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="6aa9b-107">示例</span><span class="sxs-lookup"><span data-stu-id="6aa9b-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa9b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6aa9b-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="6aa9b-109">建立多個外部 radius 伺服器設定，以用於在新的虛擬網路閘道上設定 P2S。</span><span class="sxs-lookup"><span data-stu-id="6aa9b-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="6aa9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="6aa9b-110">PARAMETERS</span></span>

### <span data-ttu-id="6aa9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa9b-111">-DefaultProfile</span></span>
<span data-ttu-id="6aa9b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6aa9b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa9b-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="6aa9b-113">-RadiusServerAddress</span></span>
<span data-ttu-id="6aa9b-114">外部 radius 伺服器位址</span><span class="sxs-lookup"><span data-stu-id="6aa9b-114">External radius server address</span></span>

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

### <span data-ttu-id="6aa9b-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="6aa9b-115">-RadiusServerScore</span></span>
<span data-ttu-id="6aa9b-116">外部 radius 伺服器分數</span><span class="sxs-lookup"><span data-stu-id="6aa9b-116">External radius server score</span></span>

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

### <span data-ttu-id="6aa9b-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="6aa9b-117">-RadiusServerSecret</span></span>
<span data-ttu-id="6aa9b-118">外部 radius 伺服器密碼</span><span class="sxs-lookup"><span data-stu-id="6aa9b-118">External radius server secret</span></span>

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

### <span data-ttu-id="6aa9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa9b-119">CommonParameters</span></span>
<span data-ttu-id="6aa9b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6aa9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa9b-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6aa9b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa9b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6aa9b-122">INPUTS</span></span>

### <span data-ttu-id="6aa9b-123">System.object</span><span class="sxs-lookup"><span data-stu-id="6aa9b-123">System.String</span></span>

### <span data-ttu-id="6aa9b-124">SecureString</span><span class="sxs-lookup"><span data-stu-id="6aa9b-124">System.Security.SecureString</span></span>

### <span data-ttu-id="6aa9b-125">System.object</span><span class="sxs-lookup"><span data-stu-id="6aa9b-125">System.Int32</span></span>

## <span data-ttu-id="6aa9b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6aa9b-126">OUTPUTS</span></span>

### <span data-ttu-id="6aa9b-127">PSRadiusServer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6aa9b-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="6aa9b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6aa9b-128">NOTES</span></span>

## <span data-ttu-id="6aa9b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6aa9b-129">RELATED LINKS</span></span>
