---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969172"
---
# <span data-ttu-id="7199e-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7199e-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7199e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7199e-102">SYNOPSIS</span></span>
<span data-ttu-id="7199e-103">將前端埠新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7199e-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="7199e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7199e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7199e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7199e-105">DESCRIPTION</span></span>
<span data-ttu-id="7199e-106">**AzApplicationGatewayFrontendPort** Cmdlet 會將前端埠新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7199e-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="7199e-107">示例</span><span class="sxs-lookup"><span data-stu-id="7199e-107">EXAMPLES</span></span>

### <span data-ttu-id="7199e-108">範例1：將前端埠新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="7199e-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="7199e-109">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7199e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7199e-110">第二個命令會將埠80新增為儲存在 $AppGw 中之應用程式閘道的前端埠，並將埠 FrontEndPort01 命名為。</span><span class="sxs-lookup"><span data-stu-id="7199e-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="7199e-111">參數</span><span class="sxs-lookup"><span data-stu-id="7199e-111">PARAMETERS</span></span>

### <span data-ttu-id="7199e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7199e-112">-ApplicationGateway</span></span>
<span data-ttu-id="7199e-113">指定此 Cmdlet 新增前端埠的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7199e-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="7199e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7199e-114">-DefaultProfile</span></span>
<span data-ttu-id="7199e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7199e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7199e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7199e-116">-Name</span></span>
<span data-ttu-id="7199e-117">指定前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="7199e-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="7199e-118">-埠</span><span class="sxs-lookup"><span data-stu-id="7199e-118">-Port</span></span>
<span data-ttu-id="7199e-119">指定埠號碼。</span><span class="sxs-lookup"><span data-stu-id="7199e-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="7199e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7199e-120">CommonParameters</span></span>
<span data-ttu-id="7199e-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7199e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7199e-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7199e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7199e-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7199e-123">INPUTS</span></span>

### <span data-ttu-id="7199e-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7199e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7199e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7199e-125">OUTPUTS</span></span>

### <span data-ttu-id="7199e-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7199e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7199e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7199e-127">NOTES</span></span>

## <span data-ttu-id="7199e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7199e-128">RELATED LINKS</span></span>

[<span data-ttu-id="7199e-129">AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7199e-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7199e-130">新-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7199e-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7199e-131">移除-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7199e-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7199e-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7199e-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


