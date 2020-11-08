---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135553"
---
# <span data-ttu-id="d8060-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d8060-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d8060-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8060-102">SYNOPSIS</span></span>
<span data-ttu-id="d8060-103">移除後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="d8060-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d8060-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8060-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8060-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8060-105">DESCRIPTION</span></span>
<span data-ttu-id="d8060-106">**AzApplicationGatewayUrlPathMapConfig** Cmdlet 會移除與後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="d8060-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d8060-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8060-107">EXAMPLES</span></span>

### <span data-ttu-id="d8060-108">範例1：從應用程式閘道移除 URL 路徑對應</span><span class="sxs-lookup"><span data-stu-id="d8060-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="d8060-109">第一個命令會取得名為 appGwName 的應用程式閘道，並將結果儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="d8060-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="d8060-110">第二個命令會從應用程式閘道移除名為 map01 的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="d8060-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="d8060-111">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d8060-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="d8060-112">參數</span><span class="sxs-lookup"><span data-stu-id="d8060-112">PARAMETERS</span></span>

### <span data-ttu-id="d8060-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8060-113">-ApplicationGateway</span></span>
<span data-ttu-id="d8060-114">指定此 Cmdlet 移除 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d8060-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="d8060-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8060-115">-DefaultProfile</span></span>
<span data-ttu-id="d8060-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8060-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8060-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8060-117">-Name</span></span>
<span data-ttu-id="d8060-118">指定此 Cmdlet 從後端伺服器移除的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="d8060-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="d8060-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8060-119">CommonParameters</span></span>
<span data-ttu-id="d8060-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8060-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8060-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8060-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8060-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d8060-122">INPUTS</span></span>

### <span data-ttu-id="d8060-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d8060-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8060-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d8060-124">OUTPUTS</span></span>

### <span data-ttu-id="d8060-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d8060-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8060-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d8060-126">NOTES</span></span>

## <span data-ttu-id="d8060-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8060-127">RELATED LINKS</span></span>

[<span data-ttu-id="d8060-128">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d8060-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d8060-129">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d8060-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d8060-130">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d8060-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d8060-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d8060-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

