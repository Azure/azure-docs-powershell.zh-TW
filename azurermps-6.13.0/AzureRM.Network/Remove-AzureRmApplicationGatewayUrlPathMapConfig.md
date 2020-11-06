---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 68676c05757a58f2c1094e36338d17a52de6b040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446935"
---
# <span data-ttu-id="1325a-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1325a-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="1325a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1325a-102">SYNOPSIS</span></span>
<span data-ttu-id="1325a-103">移除後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="1325a-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1325a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1325a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1325a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1325a-105">DESCRIPTION</span></span>
<span data-ttu-id="1325a-106">**AzureRmApplicationGatewayUrlPathMapConfig** Cmdlet 會移除與後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="1325a-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1325a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1325a-107">EXAMPLES</span></span>

## <span data-ttu-id="1325a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1325a-108">PARAMETERS</span></span>

### <span data-ttu-id="1325a-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1325a-109">-ApplicationGateway</span></span>
<span data-ttu-id="1325a-110">指定此 Cmdlet 移除 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1325a-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="1325a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1325a-111">-DefaultProfile</span></span>
<span data-ttu-id="1325a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1325a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1325a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1325a-113">-Name</span></span>
<span data-ttu-id="1325a-114">指定此 Cmdlet 從後端伺服器移除的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="1325a-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="1325a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1325a-115">CommonParameters</span></span>
<span data-ttu-id="1325a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1325a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1325a-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1325a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1325a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="1325a-118">INPUTS</span></span>

### <span data-ttu-id="1325a-119">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1325a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="1325a-120">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1325a-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="1325a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="1325a-121">OUTPUTS</span></span>

### <span data-ttu-id="1325a-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1325a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1325a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="1325a-123">NOTES</span></span>

## <span data-ttu-id="1325a-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="1325a-124">RELATED LINKS</span></span>

[<span data-ttu-id="1325a-125">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1325a-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1325a-126">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1325a-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1325a-127">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1325a-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1325a-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1325a-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


