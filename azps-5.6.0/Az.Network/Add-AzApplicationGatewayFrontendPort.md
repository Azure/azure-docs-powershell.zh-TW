---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 5926b2fb4b97d42ff8743ad227fdfb1b32326a20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905914"
---
# <span data-ttu-id="5ccc1-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5ccc1-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5ccc1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ccc1-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccc1-103">新增前端埠至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="5ccc1-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ccc1-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ccc1-105">描述</span><span class="sxs-lookup"><span data-stu-id="5ccc1-105">DESCRIPTION</span></span>
<span data-ttu-id="5ccc1-106">**Add-AzApplicationGatewayFrontendPort** Cmdlet 會新增前端埠至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="5ccc1-107">例子</span><span class="sxs-lookup"><span data-stu-id="5ccc1-107">EXAMPLES</span></span>

### <span data-ttu-id="5ccc1-108">範例 1：新增前端埠至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="5ccc1-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="5ccc1-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5ccc1-110">第二個命令會將埠 80 新增為儲存在 $AppGw 之應用程式閘道的前端埠，並命名埠 FrontEndPort01。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="5ccc1-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ccc1-111">PARAMETERS</span></span>

### <span data-ttu-id="5ccc1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ccc1-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ccc1-113">指定此 Cmdlet 新增前端埠的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="5ccc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccc1-114">-DefaultProfile</span></span>
<span data-ttu-id="5ccc1-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ccc1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ccc1-116">-Name</span></span>
<span data-ttu-id="5ccc1-117">指定前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="5ccc1-118">-埠</span><span class="sxs-lookup"><span data-stu-id="5ccc1-118">-Port</span></span>
<span data-ttu-id="5ccc1-119">指定埠號碼。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="5ccc1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccc1-120">CommonParameters</span></span>
<span data-ttu-id="5ccc1-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccc1-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5ccc1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccc1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5ccc1-123">INPUTS</span></span>

### <span data-ttu-id="5ccc1-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ccc1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ccc1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="5ccc1-125">OUTPUTS</span></span>

### <span data-ttu-id="5ccc1-126">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ccc1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ccc1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5ccc1-127">NOTES</span></span>

## <span data-ttu-id="5ccc1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ccc1-128">RELATED LINKS</span></span>

[<span data-ttu-id="5ccc1-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5ccc1-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5ccc1-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5ccc1-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5ccc1-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5ccc1-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5ccc1-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5ccc1-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


