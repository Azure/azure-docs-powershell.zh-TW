---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: a0e8cbdb9ec64d4f65b859f70c1a1bb7f843132b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913493"
---
# <span data-ttu-id="61921-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="61921-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="61921-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61921-102">SYNOPSIS</span></span>
<span data-ttu-id="61921-103">獲得應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="61921-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="61921-104">語法</span><span class="sxs-lookup"><span data-stu-id="61921-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61921-105">描述</span><span class="sxs-lookup"><span data-stu-id="61921-105">DESCRIPTION</span></span>
<span data-ttu-id="61921-106">**Get-AzApplicationGatewayFrontendPort** Cmdlet 取得應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="61921-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="61921-107">例子</span><span class="sxs-lookup"><span data-stu-id="61921-107">EXAMPLES</span></span>

### <span data-ttu-id="61921-108">範例 1：取得指定的前端埠</span><span class="sxs-lookup"><span data-stu-id="61921-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="61921-109">第一個命令會從名為 ResourceGroup01 的資源群組中，獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="61921-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="61921-110">第二個命令會從 $AppGw 取名為 FrontEndPort01 的前端埠，並儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="61921-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="61921-111">範例 2：取得前端埠的清單</span><span class="sxs-lookup"><span data-stu-id="61921-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="61921-112">第一個命令會從名為 ResourceGroup01 的資源群組中，獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="61921-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="61921-113">第二個命令會從命令中$AppGw前端埠清單，並儲存在$FrontEndPorts變數。</span><span class="sxs-lookup"><span data-stu-id="61921-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="61921-114">參數</span><span class="sxs-lookup"><span data-stu-id="61921-114">PARAMETERS</span></span>

### <span data-ttu-id="61921-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61921-115">-ApplicationGateway</span></span>
<span data-ttu-id="61921-116">指定包含前端埠的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="61921-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="61921-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61921-117">-DefaultProfile</span></span>
<span data-ttu-id="61921-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61921-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61921-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="61921-119">-Name</span></span>
<span data-ttu-id="61921-120">指定要取得前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="61921-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="61921-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61921-121">CommonParameters</span></span>
<span data-ttu-id="61921-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61921-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61921-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61921-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61921-124">輸入</span><span class="sxs-lookup"><span data-stu-id="61921-124">INPUTS</span></span>

### <span data-ttu-id="61921-125">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61921-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61921-126">輸出</span><span class="sxs-lookup"><span data-stu-id="61921-126">OUTPUTS</span></span>

### <span data-ttu-id="61921-127">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="61921-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="61921-128">筆記</span><span class="sxs-lookup"><span data-stu-id="61921-128">NOTES</span></span>

## <span data-ttu-id="61921-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="61921-129">RELATED LINKS</span></span>

[<span data-ttu-id="61921-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="61921-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="61921-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="61921-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="61921-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="61921-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="61921-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="61921-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


