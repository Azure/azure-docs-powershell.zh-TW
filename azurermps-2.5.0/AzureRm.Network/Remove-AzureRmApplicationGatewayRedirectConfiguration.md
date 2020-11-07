---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: ba979a12584d526ba7e3a36d13c44b51704b44f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800406"
---
# <span data-ttu-id="1abda-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1abda-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1abda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1abda-102">SYNOPSIS</span></span>
<span data-ttu-id="1abda-103">從現有的應用程式閘道移除重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="1abda-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1abda-104">句法</span><span class="sxs-lookup"><span data-stu-id="1abda-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1abda-105">說明</span><span class="sxs-lookup"><span data-stu-id="1abda-105">DESCRIPTION</span></span>
<span data-ttu-id="1abda-106">**AzureRmApplicationGatewayRedirectConfiguration** Cmdlet 會從現有的應用程式閘道中移除重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="1abda-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="1abda-107">示例</span><span class="sxs-lookup"><span data-stu-id="1abda-107">EXAMPLES</span></span>

### <span data-ttu-id="1abda-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1abda-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="1abda-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1abda-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1abda-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Redirect01 的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="1abda-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1abda-111">參數</span><span class="sxs-lookup"><span data-stu-id="1abda-111">PARAMETERS</span></span>

### <span data-ttu-id="1abda-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1abda-112">-ApplicationGateway</span></span>
<span data-ttu-id="1abda-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1abda-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1abda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abda-114">-DefaultProfile</span></span>
<span data-ttu-id="1abda-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1abda-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1abda-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1abda-116">-Name</span></span>
<span data-ttu-id="1abda-117">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="1abda-117">The name of the redirect configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1abda-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abda-118">CommonParameters</span></span>
<span data-ttu-id="1abda-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1abda-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abda-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1abda-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abda-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1abda-121">INPUTS</span></span>

### <span data-ttu-id="1abda-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1abda-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1abda-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1abda-123">OUTPUTS</span></span>

### <span data-ttu-id="1abda-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1abda-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1abda-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1abda-125">NOTES</span></span>

## <span data-ttu-id="1abda-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1abda-126">RELATED LINKS</span></span>

