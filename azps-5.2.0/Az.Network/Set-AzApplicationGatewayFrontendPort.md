---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 08637412afafe9220107e95dd3cb7dcc5154ba26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274787"
---
# <span data-ttu-id="23d91-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="23d91-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="23d91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23d91-102">SYNOPSIS</span></span>
<span data-ttu-id="23d91-103">修改應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="23d91-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="23d91-104">句法</span><span class="sxs-lookup"><span data-stu-id="23d91-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d91-105">說明</span><span class="sxs-lookup"><span data-stu-id="23d91-105">DESCRIPTION</span></span>
<span data-ttu-id="23d91-106">**AzApplicationGatewayFrontendPort** Cmdlet 會修改應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="23d91-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="23d91-107">示例</span><span class="sxs-lookup"><span data-stu-id="23d91-107">EXAMPLES</span></span>

### <span data-ttu-id="23d91-108">範例1：將應用程式閘道前端埠設定為80</span><span class="sxs-lookup"><span data-stu-id="23d91-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="23d91-109">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="23d91-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="23d91-110">第二個命令會在 $AppGw 中修改閘道，以將埠80用於名為 FrontEndPort01 的前端埠。</span><span class="sxs-lookup"><span data-stu-id="23d91-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="23d91-111">參數</span><span class="sxs-lookup"><span data-stu-id="23d91-111">PARAMETERS</span></span>

### <span data-ttu-id="23d91-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23d91-112">-ApplicationGateway</span></span>
<span data-ttu-id="23d91-113">指定此 Cmdlet 將前端埠關聯的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="23d91-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="23d91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d91-114">-DefaultProfile</span></span>
<span data-ttu-id="23d91-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23d91-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23d91-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="23d91-116">-Name</span></span>
<span data-ttu-id="23d91-117">指定要修改的前端埠名稱。</span><span class="sxs-lookup"><span data-stu-id="23d91-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="23d91-118">-埠</span><span class="sxs-lookup"><span data-stu-id="23d91-118">-Port</span></span>
<span data-ttu-id="23d91-119">指定要用於前端埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="23d91-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="23d91-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d91-120">CommonParameters</span></span>
<span data-ttu-id="23d91-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23d91-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d91-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23d91-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d91-123">輸入</span><span class="sxs-lookup"><span data-stu-id="23d91-123">INPUTS</span></span>

### <span data-ttu-id="23d91-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23d91-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="23d91-125">輸出</span><span class="sxs-lookup"><span data-stu-id="23d91-125">OUTPUTS</span></span>

### <span data-ttu-id="23d91-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23d91-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="23d91-127">筆記</span><span class="sxs-lookup"><span data-stu-id="23d91-127">NOTES</span></span>

## <span data-ttu-id="23d91-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="23d91-128">RELATED LINKS</span></span>

[<span data-ttu-id="23d91-129">附加 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="23d91-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="23d91-130">AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="23d91-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="23d91-131">新-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="23d91-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="23d91-132">移除-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="23d91-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
