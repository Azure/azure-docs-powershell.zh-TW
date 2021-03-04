---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1d9caf3c95d7f8a508a41b8c047684b86c66227a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913462"
---
# <span data-ttu-id="4d486-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d486-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4d486-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4d486-102">SYNOPSIS</span></span>
<span data-ttu-id="4d486-103">移除後端伺服器資料庫的 URL 路徑映射。</span><span class="sxs-lookup"><span data-stu-id="4d486-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4d486-104">語法</span><span class="sxs-lookup"><span data-stu-id="4d486-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d486-105">描述</span><span class="sxs-lookup"><span data-stu-id="4d486-105">DESCRIPTION</span></span>
<span data-ttu-id="4d486-106">**Remove-AzApplicationGatewayUrlPathMapConfig** Cmdlet 會移除後端伺服器集區 URL 路徑的映射。</span><span class="sxs-lookup"><span data-stu-id="4d486-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4d486-107">例子</span><span class="sxs-lookup"><span data-stu-id="4d486-107">EXAMPLES</span></span>

### <span data-ttu-id="4d486-108">範例 1：移除應用程式閘道的 URL 路徑地圖</span><span class="sxs-lookup"><span data-stu-id="4d486-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="4d486-109">第一個命令會取得名為 appGwName 的應用程式閘道，並儲存在$appgw變數中。</span><span class="sxs-lookup"><span data-stu-id="4d486-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="4d486-110">第二個命令會從應用程式閘道移除名為 map01 的 URL 路徑映射。</span><span class="sxs-lookup"><span data-stu-id="4d486-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="4d486-111">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4d486-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="4d486-112">參數</span><span class="sxs-lookup"><span data-stu-id="4d486-112">PARAMETERS</span></span>

### <span data-ttu-id="4d486-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d486-113">-ApplicationGateway</span></span>
<span data-ttu-id="4d486-114">指定此 Cmdlet 會移除 URL 路徑地圖組配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4d486-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="4d486-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d486-115">-DefaultProfile</span></span>
<span data-ttu-id="4d486-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d486-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d486-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d486-117">-Name</span></span>
<span data-ttu-id="4d486-118">指定此 Cmdlet 從後端伺服器移除的 URL 路徑地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="4d486-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="4d486-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d486-119">CommonParameters</span></span>
<span data-ttu-id="4d486-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4d486-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d486-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4d486-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d486-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4d486-122">INPUTS</span></span>

### <span data-ttu-id="4d486-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d486-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d486-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4d486-124">OUTPUTS</span></span>

### <span data-ttu-id="4d486-125">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d486-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d486-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4d486-126">NOTES</span></span>

## <span data-ttu-id="4d486-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d486-127">RELATED LINKS</span></span>

[<span data-ttu-id="4d486-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d486-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d486-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d486-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d486-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d486-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d486-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d486-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


