---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 6399843edfc8ee806693e0ddfee77952438f2d35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912713"
---
# <span data-ttu-id="89038-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89038-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="89038-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89038-102">SYNOPSIS</span></span>
<span data-ttu-id="89038-103">建立應用程式閘道的 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="89038-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="89038-104">語法</span><span class="sxs-lookup"><span data-stu-id="89038-104">SYNTAX</span></span>

### <span data-ttu-id="89038-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="89038-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89038-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="89038-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89038-107">描述</span><span class="sxs-lookup"><span data-stu-id="89038-107">DESCRIPTION</span></span>
<span data-ttu-id="89038-108">**New-AzApplicationGatewayIPConfiguration** Cmdlet 會為應用程式閘道建立 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="89038-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="89038-109">IP 群組原則包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="89038-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="89038-110">例子</span><span class="sxs-lookup"><span data-stu-id="89038-110">EXAMPLES</span></span>

### <span data-ttu-id="89038-111">範例 1：建立應用程式閘道的 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="89038-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="89038-112">第一個命令會獲得名為 VNet01 的虛擬網路，該虛擬網路屬於名為 ResourceGroup01 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="89038-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="89038-113">第二個命令會獲得上一個命令中虛擬網路所屬子網的子網組$Subnet變數。</span><span class="sxs-lookup"><span data-stu-id="89038-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="89038-114">第三個命令會使用 $Subnet。</span><span class="sxs-lookup"><span data-stu-id="89038-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="89038-115">參數</span><span class="sxs-lookup"><span data-stu-id="89038-115">PARAMETERS</span></span>

### <span data-ttu-id="89038-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89038-116">-DefaultProfile</span></span>
<span data-ttu-id="89038-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="89038-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89038-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="89038-118">-Name</span></span>
<span data-ttu-id="89038-119">指定要建立之 IP 群組原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="89038-119">Specifies the name of the IP configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89038-120">-子網</span><span class="sxs-lookup"><span data-stu-id="89038-120">-Subnet</span></span>
<span data-ttu-id="89038-121">指定子網物件。</span><span class="sxs-lookup"><span data-stu-id="89038-121">Specifies the subnet object.</span></span>
<span data-ttu-id="89038-122">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="89038-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89038-123">-子網Id</span><span class="sxs-lookup"><span data-stu-id="89038-123">-SubnetId</span></span>
<span data-ttu-id="89038-124">指定子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="89038-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="89038-125">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="89038-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89038-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89038-126">CommonParameters</span></span>
<span data-ttu-id="89038-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89038-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89038-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="89038-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89038-129">輸入</span><span class="sxs-lookup"><span data-stu-id="89038-129">INPUTS</span></span>

### <span data-ttu-id="89038-130">沒有</span><span class="sxs-lookup"><span data-stu-id="89038-130">None</span></span>

## <span data-ttu-id="89038-131">輸出</span><span class="sxs-lookup"><span data-stu-id="89038-131">OUTPUTS</span></span>

### <span data-ttu-id="89038-132">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89038-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="89038-133">筆記</span><span class="sxs-lookup"><span data-stu-id="89038-133">NOTES</span></span>

## <span data-ttu-id="89038-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="89038-134">RELATED LINKS</span></span>

[<span data-ttu-id="89038-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89038-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="89038-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89038-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="89038-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89038-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="89038-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89038-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


