---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128449"
---
# <span data-ttu-id="93a86-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a86-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="93a86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93a86-102">SYNOPSIS</span></span>
<span data-ttu-id="93a86-103">從應用程式閘道取得現有的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="93a86-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="93a86-104">句法</span><span class="sxs-lookup"><span data-stu-id="93a86-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93a86-105">說明</span><span class="sxs-lookup"><span data-stu-id="93a86-105">DESCRIPTION</span></span>
<span data-ttu-id="93a86-106">**AzApplicationGatewayRedirectConfiguration** Cmdlet 會從應用程式閘道取得現有的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="93a86-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="93a86-107">示例</span><span class="sxs-lookup"><span data-stu-id="93a86-107">EXAMPLES</span></span>

### <span data-ttu-id="93a86-108">範例1</span><span class="sxs-lookup"><span data-stu-id="93a86-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="93a86-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="93a86-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="93a86-110">第二個命令會從儲存在名為 $AppGW 的變數中，從應用程式閘道取得名為 Redirect01 的重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="93a86-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="93a86-111">參數</span><span class="sxs-lookup"><span data-stu-id="93a86-111">PARAMETERS</span></span>

### <span data-ttu-id="93a86-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93a86-112">-ApplicationGateway</span></span>
<span data-ttu-id="93a86-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93a86-113">The applicationGateway</span></span>

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

### <span data-ttu-id="93a86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a86-114">-DefaultProfile</span></span>
<span data-ttu-id="93a86-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93a86-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93a86-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="93a86-116">-Name</span></span>
<span data-ttu-id="93a86-117">要求路由規則的名稱</span><span class="sxs-lookup"><span data-stu-id="93a86-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="93a86-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a86-118">CommonParameters</span></span>
<span data-ttu-id="93a86-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93a86-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a86-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93a86-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a86-121">輸入</span><span class="sxs-lookup"><span data-stu-id="93a86-121">INPUTS</span></span>

### <span data-ttu-id="93a86-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="93a86-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93a86-123">輸出</span><span class="sxs-lookup"><span data-stu-id="93a86-123">OUTPUTS</span></span>

### <span data-ttu-id="93a86-124">PSApplicationGatewayRedirectConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="93a86-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="93a86-125">筆記</span><span class="sxs-lookup"><span data-stu-id="93a86-125">NOTES</span></span>

## <span data-ttu-id="93a86-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="93a86-126">RELATED LINKS</span></span>

[<span data-ttu-id="93a86-127">附加 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a86-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="93a86-128">新-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a86-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="93a86-129">移除-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a86-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="93a86-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="93a86-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)