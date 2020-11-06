---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 612e6b0cb5438dbb37a2e9d1c77da151c852fac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448633"
---
# <span data-ttu-id="3ac7c-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3ac7c-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="3ac7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ac7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac7c-103">移除後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="3ac7c-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ac7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ac7c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ac7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ac7c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac7c-106">**AzureRmApplicationGatewayUrlPathMapConfig** Cmdlet 會移除與後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="3ac7c-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3ac7c-107">示例</span><span class="sxs-lookup"><span data-stu-id="3ac7c-107">EXAMPLES</span></span>

## <span data-ttu-id="3ac7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ac7c-108">PARAMETERS</span></span>

### <span data-ttu-id="3ac7c-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ac7c-109">-ApplicationGateway</span></span>
<span data-ttu-id="3ac7c-110">指定此 Cmdlet 移除 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3ac7c-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="3ac7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac7c-111">-DefaultProfile</span></span>
<span data-ttu-id="3ac7c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ac7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ac7c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ac7c-113">-Name</span></span>
<span data-ttu-id="3ac7c-114">指定此 Cmdlet 從後端伺服器移除的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac7c-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="3ac7c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac7c-115">CommonParameters</span></span>
<span data-ttu-id="3ac7c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ac7c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac7c-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ac7c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac7c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="3ac7c-118">INPUTS</span></span>

### <span data-ttu-id="3ac7c-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ac7c-119">PSApplicationGateway</span></span>
<span data-ttu-id="3ac7c-120">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3ac7c-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="3ac7c-121">輸出</span><span class="sxs-lookup"><span data-stu-id="3ac7c-121">OUTPUTS</span></span>

### <span data-ttu-id="3ac7c-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3ac7c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ac7c-123">筆記</span><span class="sxs-lookup"><span data-stu-id="3ac7c-123">NOTES</span></span>

## <span data-ttu-id="3ac7c-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ac7c-124">RELATED LINKS</span></span>

[<span data-ttu-id="3ac7c-125">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3ac7c-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3ac7c-126">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3ac7c-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3ac7c-127">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3ac7c-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3ac7c-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3ac7c-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)

