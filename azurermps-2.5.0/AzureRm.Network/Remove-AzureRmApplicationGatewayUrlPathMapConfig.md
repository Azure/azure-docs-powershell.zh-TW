---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800389"
---
# <span data-ttu-id="c3e51-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c3e51-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="c3e51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3e51-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e51-103">移除後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="c3e51-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e51-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3e51-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e51-105">說明</span><span class="sxs-lookup"><span data-stu-id="c3e51-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e51-106">**AzureRmApplicationGatewayUrlPathMapConfig** Cmdlet 會移除與後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="c3e51-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c3e51-107">示例</span><span class="sxs-lookup"><span data-stu-id="c3e51-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e51-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="c3e51-108">1:</span></span>
```

```

## <span data-ttu-id="c3e51-109">參數</span><span class="sxs-lookup"><span data-stu-id="c3e51-109">PARAMETERS</span></span>

### <span data-ttu-id="c3e51-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3e51-110">-ApplicationGateway</span></span>
<span data-ttu-id="c3e51-111">指定此 Cmdlet 移除 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c3e51-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="c3e51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e51-112">-DefaultProfile</span></span>
<span data-ttu-id="c3e51-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3e51-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3e51-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3e51-114">-Name</span></span>
<span data-ttu-id="c3e51-115">指定此 Cmdlet 從後端伺服器移除的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="c3e51-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="c3e51-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e51-116">CommonParameters</span></span>
<span data-ttu-id="c3e51-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3e51-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e51-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3e51-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e51-119">輸入</span><span class="sxs-lookup"><span data-stu-id="c3e51-119">INPUTS</span></span>

### <span data-ttu-id="c3e51-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3e51-120">PSApplicationGateway</span></span>
<span data-ttu-id="c3e51-121">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c3e51-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="c3e51-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c3e51-122">OUTPUTS</span></span>

### <span data-ttu-id="c3e51-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c3e51-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3e51-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c3e51-124">NOTES</span></span>

## <span data-ttu-id="c3e51-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3e51-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3e51-126">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c3e51-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c3e51-127">AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c3e51-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c3e51-128">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c3e51-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c3e51-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c3e51-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


