---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286995"
---
# <span data-ttu-id="bd379-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd379-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="bd379-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd379-102">SYNOPSIS</span></span>
<span data-ttu-id="bd379-103">建立應用程式閘道的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="bd379-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="bd379-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd379-104">SYNTAX</span></span>

### <span data-ttu-id="bd379-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd379-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd379-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bd379-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd379-107">說明</span><span class="sxs-lookup"><span data-stu-id="bd379-107">DESCRIPTION</span></span>
<span data-ttu-id="bd379-108">**新的-AzApplicationGatewayIPConfiguration** Cmdlet 會為應用程式閘道建立 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="bd379-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="bd379-109">[IP 設定] 包含部署應用程式閘道所用的子網。</span><span class="sxs-lookup"><span data-stu-id="bd379-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="bd379-110">示例</span><span class="sxs-lookup"><span data-stu-id="bd379-110">EXAMPLES</span></span>

### <span data-ttu-id="bd379-111">範例1：建立應用程式閘道的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="bd379-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="bd379-112">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bd379-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="bd379-113">第二個命令會針對前一個命令中的虛擬網路，取得子網的子網設定，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="bd379-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="bd379-114">第三個命令會使用 $Subnet 建立 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="bd379-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="bd379-115">參數</span><span class="sxs-lookup"><span data-stu-id="bd379-115">PARAMETERS</span></span>

### <span data-ttu-id="bd379-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd379-116">-DefaultProfile</span></span>
<span data-ttu-id="bd379-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd379-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd379-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd379-118">-Name</span></span>
<span data-ttu-id="bd379-119">指定要建立的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="bd379-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="bd379-120">-子網</span><span class="sxs-lookup"><span data-stu-id="bd379-120">-Subnet</span></span>
<span data-ttu-id="bd379-121">指定子網物件。</span><span class="sxs-lookup"><span data-stu-id="bd379-121">Specifies the subnet object.</span></span>
<span data-ttu-id="bd379-122">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="bd379-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="bd379-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bd379-123">-SubnetId</span></span>
<span data-ttu-id="bd379-124">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="bd379-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="bd379-125">這是要部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="bd379-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="bd379-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd379-126">CommonParameters</span></span>
<span data-ttu-id="bd379-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd379-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd379-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd379-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd379-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bd379-129">INPUTS</span></span>

### <span data-ttu-id="bd379-130">所有</span><span class="sxs-lookup"><span data-stu-id="bd379-130">None</span></span>

## <span data-ttu-id="bd379-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bd379-131">OUTPUTS</span></span>

### <span data-ttu-id="bd379-132">PSApplicationGatewayIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bd379-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="bd379-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bd379-133">NOTES</span></span>

## <span data-ttu-id="bd379-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd379-134">RELATED LINKS</span></span>

[<span data-ttu-id="bd379-135">附加 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd379-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bd379-136">AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd379-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bd379-137">移除-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd379-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="bd379-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd379-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


