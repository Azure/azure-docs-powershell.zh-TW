---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e134fafb8f7089b803b09a0202d3c43b0948f7ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903113"
---
# <span data-ttu-id="279fb-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="279fb-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="279fb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="279fb-102">SYNOPSIS</span></span>
<span data-ttu-id="279fb-103">修改應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="279fb-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="279fb-104">語法</span><span class="sxs-lookup"><span data-stu-id="279fb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="279fb-105">描述</span><span class="sxs-lookup"><span data-stu-id="279fb-105">DESCRIPTION</span></span>
<span data-ttu-id="279fb-106">**Set-AzApplicationGatewayFrontendPort** Cmdlet 會修改應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="279fb-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="279fb-107">例子</span><span class="sxs-lookup"><span data-stu-id="279fb-107">EXAMPLES</span></span>

### <span data-ttu-id="279fb-108">範例 1：將應用程式閘道前端埠設定為 80</span><span class="sxs-lookup"><span data-stu-id="279fb-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="279fb-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="279fb-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="279fb-110">第二個命令會修改 $AppGw 中的閘道，為名為 FrontEndPort01 的前端埠使用埠 80。</span><span class="sxs-lookup"><span data-stu-id="279fb-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="279fb-111">參數</span><span class="sxs-lookup"><span data-stu-id="279fb-111">PARAMETERS</span></span>

### <span data-ttu-id="279fb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="279fb-112">-ApplicationGateway</span></span>
<span data-ttu-id="279fb-113">指定此 Cmdlet 與前端埠關聯的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="279fb-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="279fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279fb-114">-DefaultProfile</span></span>
<span data-ttu-id="279fb-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="279fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="279fb-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="279fb-116">-Name</span></span>
<span data-ttu-id="279fb-117">指定要修改的前端埠名稱。</span><span class="sxs-lookup"><span data-stu-id="279fb-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="279fb-118">-埠</span><span class="sxs-lookup"><span data-stu-id="279fb-118">-Port</span></span>
<span data-ttu-id="279fb-119">指定要用於前端埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="279fb-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279fb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279fb-120">CommonParameters</span></span>
<span data-ttu-id="279fb-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="279fb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279fb-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="279fb-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279fb-123">輸入</span><span class="sxs-lookup"><span data-stu-id="279fb-123">INPUTS</span></span>

### <span data-ttu-id="279fb-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="279fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="279fb-125">輸出</span><span class="sxs-lookup"><span data-stu-id="279fb-125">OUTPUTS</span></span>

### <span data-ttu-id="279fb-126">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="279fb-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="279fb-127">筆記</span><span class="sxs-lookup"><span data-stu-id="279fb-127">NOTES</span></span>

## <span data-ttu-id="279fb-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="279fb-128">RELATED LINKS</span></span>

[<span data-ttu-id="279fb-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="279fb-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="279fb-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="279fb-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="279fb-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="279fb-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="279fb-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="279fb-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
