---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c7912f1a5d0539a0c81aff930cd94cb944e45bb7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794465"
---
# <span data-ttu-id="b566c-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b566c-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b566c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b566c-102">SYNOPSIS</span></span>
<span data-ttu-id="b566c-103">取得應用程式閘道的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="b566c-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="b566c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b566c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b566c-105">說明</span><span class="sxs-lookup"><span data-stu-id="b566c-105">DESCRIPTION</span></span>
<span data-ttu-id="b566c-106">**AzApplicationGatewayIPConfiguration** Cmdlet 會取得應用程式閘道的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="b566c-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="b566c-107">[IP 設定] 包含部署應用程式閘道所用的子網。</span><span class="sxs-lookup"><span data-stu-id="b566c-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="b566c-108">示例</span><span class="sxs-lookup"><span data-stu-id="b566c-108">EXAMPLES</span></span>

### <span data-ttu-id="b566c-109">範例1：取得特定的 IP 配置</span><span class="sxs-lookup"><span data-stu-id="b566c-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="b566c-110">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會從儲存在 $AppGw 中的閘道取得名為 GateSubnet01 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="b566c-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="b566c-111">範例2：取得 IP 配置清單</span><span class="sxs-lookup"><span data-stu-id="b566c-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="b566c-112">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會取得所有 IP 配置的清單。</span><span class="sxs-lookup"><span data-stu-id="b566c-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="b566c-113">參數</span><span class="sxs-lookup"><span data-stu-id="b566c-113">PARAMETERS</span></span>

### <span data-ttu-id="b566c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b566c-114">-ApplicationGateway</span></span>
<span data-ttu-id="b566c-115">指定包含 IP 配置的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="b566c-115">Specifies the application gateway object that contains IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b566c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b566c-116">-DefaultProfile</span></span>
<span data-ttu-id="b566c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b566c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b566c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b566c-118">-Name</span></span>
<span data-ttu-id="b566c-119">指定此 Cmdlet 取得的 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b566c-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b566c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b566c-120">CommonParameters</span></span>
<span data-ttu-id="b566c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b566c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b566c-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b566c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b566c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b566c-123">INPUTS</span></span>

### <span data-ttu-id="b566c-124">System.object</span><span class="sxs-lookup"><span data-stu-id="b566c-124">System.String</span></span>

## <span data-ttu-id="b566c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b566c-125">OUTPUTS</span></span>

### <span data-ttu-id="b566c-126">PSApplicationGatewayIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b566c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b566c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b566c-127">NOTES</span></span>

## <span data-ttu-id="b566c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b566c-128">RELATED LINKS</span></span>

[<span data-ttu-id="b566c-129">附加 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b566c-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b566c-130">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b566c-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b566c-131">移除-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b566c-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b566c-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b566c-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

