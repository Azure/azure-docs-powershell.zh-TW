---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 8b550d0ba38036b527a1082f4ce48f40913a54e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452160"
---
# <span data-ttu-id="9ce4c-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ce4c-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9ce4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ce4c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce4c-103">建立應用程式閘道的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ce4c-104">SYNTAX</span></span>

### <span data-ttu-id="9ce4c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ce4c-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ce4c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9ce4c-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ce4c-107">說明</span><span class="sxs-lookup"><span data-stu-id="9ce4c-107">DESCRIPTION</span></span>
<span data-ttu-id="9ce4c-108">**新的-AzureRmApplicationGatewayIPConfiguration** Cmdlet 會為應用程式閘道建立 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="9ce4c-109">[IP 設定] 包含部署應用程式閘道所用的子網。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="9ce4c-110">示例</span><span class="sxs-lookup"><span data-stu-id="9ce4c-110">EXAMPLES</span></span>

### <span data-ttu-id="9ce4c-111">範例1：建立應用程式閘道的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="9ce4c-112">第一個命令會取得一個名為 VNet01 的虛擬網路，該網路網路屬於名為 ResourceGroup01 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="9ce4c-113">第二個命令會針對前一個命令中的虛擬網路，取得子網的子網設定，並將它儲存在 $Subnet 變數中。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="9ce4c-114">第三個命令會使用 $Subnet 建立 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="9ce4c-115">參數</span><span class="sxs-lookup"><span data-stu-id="9ce4c-115">PARAMETERS</span></span>

### <span data-ttu-id="9ce4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce4c-116">-DefaultProfile</span></span>
<span data-ttu-id="9ce4c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ce4c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ce4c-118">-Name</span></span>
<span data-ttu-id="9ce4c-119">指定要建立的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-119">Specifies the name of the IP configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce4c-120">-子網</span><span class="sxs-lookup"><span data-stu-id="9ce4c-120">-Subnet</span></span>
<span data-ttu-id="9ce4c-121">指定子網物件。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-121">Specifies the subnet object.</span></span>
<span data-ttu-id="9ce4c-122">這是部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce4c-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9ce4c-123">-SubnetId</span></span>
<span data-ttu-id="9ce4c-124">指定子網 ID。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="9ce4c-125">這是要部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce4c-126">CommonParameters</span></span>
<span data-ttu-id="9ce4c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce4c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ce4c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce4c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9ce4c-129">INPUTS</span></span>

### <span data-ttu-id="9ce4c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="9ce4c-130">System.String</span></span>

## <span data-ttu-id="9ce4c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9ce4c-131">OUTPUTS</span></span>

### <span data-ttu-id="9ce4c-132">PSApplicationGatewayIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9ce4c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="9ce4c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9ce4c-133">NOTES</span></span>

## <span data-ttu-id="9ce4c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ce4c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9ce4c-135">附加 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ce4c-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9ce4c-136">AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ce4c-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9ce4c-137">移除-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ce4c-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="9ce4c-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ce4c-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


