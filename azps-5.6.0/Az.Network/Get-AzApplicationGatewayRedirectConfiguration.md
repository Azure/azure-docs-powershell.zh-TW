---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b2e62b0785cc01dfc9b26aeac7b267c06a4d24b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912790"
---
# <span data-ttu-id="49578-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="49578-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="49578-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49578-102">SYNOPSIS</span></span>
<span data-ttu-id="49578-103">從應用程式閘道獲得現有的重新導向組。</span><span class="sxs-lookup"><span data-stu-id="49578-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="49578-104">語法</span><span class="sxs-lookup"><span data-stu-id="49578-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49578-105">描述</span><span class="sxs-lookup"><span data-stu-id="49578-105">DESCRIPTION</span></span>
<span data-ttu-id="49578-106">**Get-AzApplicationGatewayRedirectConfiguration** Cmdlet 會從應用程式閘道取得現有的重新導向組式。</span><span class="sxs-lookup"><span data-stu-id="49578-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="49578-107">例子</span><span class="sxs-lookup"><span data-stu-id="49578-107">EXAMPLES</span></span>

### <span data-ttu-id="49578-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="49578-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="49578-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="49578-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="49578-110">第二個命令會從儲存在名為 $AppGW 之變數的應用程式閘道中，獲得名為 Redirect01 的重新導向$AppGW。</span><span class="sxs-lookup"><span data-stu-id="49578-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="49578-111">參數</span><span class="sxs-lookup"><span data-stu-id="49578-111">PARAMETERS</span></span>

### <span data-ttu-id="49578-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49578-112">-ApplicationGateway</span></span>
<span data-ttu-id="49578-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="49578-113">The applicationGateway</span></span>

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

### <span data-ttu-id="49578-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49578-114">-DefaultProfile</span></span>
<span data-ttu-id="49578-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49578-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49578-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="49578-116">-Name</span></span>
<span data-ttu-id="49578-117">要求路由規則的名稱</span><span class="sxs-lookup"><span data-stu-id="49578-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="49578-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49578-118">CommonParameters</span></span>
<span data-ttu-id="49578-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49578-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49578-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49578-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49578-121">輸入</span><span class="sxs-lookup"><span data-stu-id="49578-121">INPUTS</span></span>

### <span data-ttu-id="49578-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49578-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49578-123">輸出</span><span class="sxs-lookup"><span data-stu-id="49578-123">OUTPUTS</span></span>

### <span data-ttu-id="49578-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="49578-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="49578-125">筆記</span><span class="sxs-lookup"><span data-stu-id="49578-125">NOTES</span></span>

## <span data-ttu-id="49578-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="49578-126">RELATED LINKS</span></span>

[<span data-ttu-id="49578-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="49578-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="49578-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="49578-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="49578-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="49578-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="49578-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="49578-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
