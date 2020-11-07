---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794191"
---
# <span data-ttu-id="5fa64-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5fa64-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5fa64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5fa64-102">SYNOPSIS</span></span>
<span data-ttu-id="5fa64-103">移除後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="5fa64-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5fa64-104">句法</span><span class="sxs-lookup"><span data-stu-id="5fa64-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fa64-105">說明</span><span class="sxs-lookup"><span data-stu-id="5fa64-105">DESCRIPTION</span></span>
<span data-ttu-id="5fa64-106">**AzApplicationGatewayUrlPathMapConfig** Cmdlet 會移除與後端伺服器池的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="5fa64-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5fa64-107">示例</span><span class="sxs-lookup"><span data-stu-id="5fa64-107">EXAMPLES</span></span>

### <span data-ttu-id="5fa64-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="5fa64-108">1:</span></span>
```

```

## <span data-ttu-id="5fa64-109">參數</span><span class="sxs-lookup"><span data-stu-id="5fa64-109">PARAMETERS</span></span>

### <span data-ttu-id="5fa64-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5fa64-110">-ApplicationGateway</span></span>
<span data-ttu-id="5fa64-111">指定此 Cmdlet 移除 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5fa64-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="5fa64-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fa64-112">-DefaultProfile</span></span>
<span data-ttu-id="5fa64-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5fa64-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fa64-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fa64-114">-Name</span></span>
<span data-ttu-id="5fa64-115">指定此 Cmdlet 從後端伺服器移除的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="5fa64-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="5fa64-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fa64-116">CommonParameters</span></span>
<span data-ttu-id="5fa64-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5fa64-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fa64-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5fa64-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fa64-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5fa64-119">INPUTS</span></span>

### <span data-ttu-id="5fa64-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5fa64-120">PSApplicationGateway</span></span>
<span data-ttu-id="5fa64-121">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5fa64-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5fa64-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5fa64-122">OUTPUTS</span></span>

### <span data-ttu-id="5fa64-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5fa64-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5fa64-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5fa64-124">NOTES</span></span>

## <span data-ttu-id="5fa64-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fa64-125">RELATED LINKS</span></span>

[<span data-ttu-id="5fa64-126">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5fa64-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5fa64-127">AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5fa64-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5fa64-128">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5fa64-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5fa64-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5fa64-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


