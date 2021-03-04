---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d1364bd101a5963dfa33927ad12c43f116dd2c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911910"
---
# <span data-ttu-id="8f76f-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f76f-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8f76f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f76f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f76f-103">移除現有應用程式閘道的重新導向組配置。</span><span class="sxs-lookup"><span data-stu-id="8f76f-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="8f76f-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f76f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f76f-105">描述</span><span class="sxs-lookup"><span data-stu-id="8f76f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f76f-106">**Remove-AzApplicationGatewayRedirectConfiguration** Cmdlet 會移除現有應用程式閘道的重新導向組式。</span><span class="sxs-lookup"><span data-stu-id="8f76f-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="8f76f-107">例子</span><span class="sxs-lookup"><span data-stu-id="8f76f-107">EXAMPLES</span></span>

### <span data-ttu-id="8f76f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8f76f-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="8f76f-109">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="8f76f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8f76f-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 Redirect01 的重新導向$AppGw。</span><span class="sxs-lookup"><span data-stu-id="8f76f-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8f76f-111">參數</span><span class="sxs-lookup"><span data-stu-id="8f76f-111">PARAMETERS</span></span>

### <span data-ttu-id="8f76f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f76f-112">-ApplicationGateway</span></span>
<span data-ttu-id="8f76f-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="8f76f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8f76f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f76f-114">-DefaultProfile</span></span>
<span data-ttu-id="8f76f-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f76f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f76f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f76f-116">-Name</span></span>
<span data-ttu-id="8f76f-117">重新導向組名</span><span class="sxs-lookup"><span data-stu-id="8f76f-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="8f76f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f76f-118">CommonParameters</span></span>
<span data-ttu-id="8f76f-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f76f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f76f-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8f76f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f76f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="8f76f-121">INPUTS</span></span>

### <span data-ttu-id="8f76f-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f76f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f76f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8f76f-123">OUTPUTS</span></span>

### <span data-ttu-id="8f76f-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f76f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f76f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8f76f-125">NOTES</span></span>

## <span data-ttu-id="8f76f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f76f-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f76f-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f76f-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="8f76f-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f76f-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="8f76f-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f76f-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="8f76f-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f76f-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
