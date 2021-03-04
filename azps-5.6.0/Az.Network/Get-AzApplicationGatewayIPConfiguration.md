---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 367d4efc8332b862a8db276934acfa971d7c0d9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914757"
---
# <span data-ttu-id="f24ff-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f24ff-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f24ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f24ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f24ff-103">獲得應用程式閘道的 IP 組配置。</span><span class="sxs-lookup"><span data-stu-id="f24ff-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="f24ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="f24ff-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f24ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="f24ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f24ff-106">**Get-AzApplicationGatewayIPConfiguration** Cmdlet 取得應用程式閘道的 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="f24ff-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="f24ff-107">IP 群組原則包含部署應用程式閘道的子網。</span><span class="sxs-lookup"><span data-stu-id="f24ff-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="f24ff-108">例子</span><span class="sxs-lookup"><span data-stu-id="f24ff-108">EXAMPLES</span></span>

### <span data-ttu-id="f24ff-109">範例 1：取得特定的 IP 組</span><span class="sxs-lookup"><span data-stu-id="f24ff-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="f24ff-110">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。第二個命令會從儲存在 $AppGw 的閘道中，獲得名為 GateSubnet01 的 IP $AppGw。</span><span class="sxs-lookup"><span data-stu-id="f24ff-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="f24ff-111">範例 2：取得 IP 組配置清單</span><span class="sxs-lookup"><span data-stu-id="f24ff-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="f24ff-112">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。第二個命令會獲得所有 IP 組配置的清單。</span><span class="sxs-lookup"><span data-stu-id="f24ff-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="f24ff-113">參數</span><span class="sxs-lookup"><span data-stu-id="f24ff-113">PARAMETERS</span></span>

### <span data-ttu-id="f24ff-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f24ff-114">-ApplicationGateway</span></span>
<span data-ttu-id="f24ff-115">指定包含 IP 群組原則的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="f24ff-115">Specifies the application gateway object that contains IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f24ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24ff-116">-DefaultProfile</span></span>
<span data-ttu-id="f24ff-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f24ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f24ff-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f24ff-118">-Name</span></span>
<span data-ttu-id="f24ff-119">指定此 Cmdlet 會獲得之 IP 群組原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f24ff-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f24ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24ff-120">CommonParameters</span></span>
<span data-ttu-id="f24ff-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f24ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24ff-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f24ff-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24ff-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f24ff-123">INPUTS</span></span>

### <span data-ttu-id="f24ff-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f24ff-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f24ff-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f24ff-125">OUTPUTS</span></span>

### <span data-ttu-id="f24ff-126">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f24ff-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f24ff-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f24ff-127">NOTES</span></span>

## <span data-ttu-id="f24ff-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f24ff-128">RELATED LINKS</span></span>

[<span data-ttu-id="f24ff-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f24ff-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f24ff-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f24ff-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f24ff-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f24ff-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f24ff-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f24ff-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


