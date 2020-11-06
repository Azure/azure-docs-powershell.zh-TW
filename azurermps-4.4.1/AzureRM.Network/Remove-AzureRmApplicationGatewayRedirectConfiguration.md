---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bd9ab62406d033eefe3fb3723d2a2ebf2f9dbb8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449614"
---
# <span data-ttu-id="7b975-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b975-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7b975-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b975-102">SYNOPSIS</span></span>
<span data-ttu-id="7b975-103">從現有的應用程式閘道移除重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="7b975-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b975-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b975-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b975-105">說明</span><span class="sxs-lookup"><span data-stu-id="7b975-105">DESCRIPTION</span></span>
<span data-ttu-id="7b975-106">**AzureRmApplicationGatewayRedirectConfiguration** Cmdlet 會從現有的應用程式閘道中移除重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="7b975-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="7b975-107">示例</span><span class="sxs-lookup"><span data-stu-id="7b975-107">EXAMPLES</span></span>

### <span data-ttu-id="7b975-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7b975-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="7b975-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b975-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="7b975-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Redirect01 的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="7b975-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7b975-111">參數</span><span class="sxs-lookup"><span data-stu-id="7b975-111">PARAMETERS</span></span>

### <span data-ttu-id="7b975-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b975-112">-ApplicationGateway</span></span>
<span data-ttu-id="7b975-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b975-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7b975-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b975-114">-Name</span></span>
<span data-ttu-id="7b975-115">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="7b975-115">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="7b975-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b975-116">-DefaultProfile</span></span>
<span data-ttu-id="7b975-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b975-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b975-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b975-118">CommonParameters</span></span>
<span data-ttu-id="7b975-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b975-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b975-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b975-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b975-121">輸入</span><span class="sxs-lookup"><span data-stu-id="7b975-121">INPUTS</span></span>

### <span data-ttu-id="7b975-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7b975-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7b975-123">輸出</span><span class="sxs-lookup"><span data-stu-id="7b975-123">OUTPUTS</span></span>

### <span data-ttu-id="7b975-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7b975-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7b975-125">筆記</span><span class="sxs-lookup"><span data-stu-id="7b975-125">NOTES</span></span>

## <span data-ttu-id="7b975-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b975-126">RELATED LINKS</span></span>

