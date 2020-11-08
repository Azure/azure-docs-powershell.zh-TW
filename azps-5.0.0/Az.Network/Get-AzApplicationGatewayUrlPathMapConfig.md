---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141421"
---
# <span data-ttu-id="3b92d-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3b92d-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="3b92d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b92d-102">SYNOPSIS</span></span>
<span data-ttu-id="3b92d-103">取得與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="3b92d-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3b92d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b92d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b92d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b92d-105">DESCRIPTION</span></span>
<span data-ttu-id="3b92d-106">**AzApplicationGatewayURLPathMapConfig** Cmdlet 會取得 URL 路徑對應至後端伺服器池的陣列。</span><span class="sxs-lookup"><span data-stu-id="3b92d-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3b92d-107">示例</span><span class="sxs-lookup"><span data-stu-id="3b92d-107">EXAMPLES</span></span>

### <span data-ttu-id="3b92d-108">範例1：取得 URL 路徑對應配置</span><span class="sxs-lookup"><span data-stu-id="3b92d-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="3b92d-109">這個命令會從位於名為「閘道」的應用程式閘道上的後端伺服器上，取得 URL 路徑對應配置。</span><span class="sxs-lookup"><span data-stu-id="3b92d-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="3b92d-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b92d-110">PARAMETERS</span></span>

### <span data-ttu-id="3b92d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b92d-111">-ApplicationGateway</span></span>
<span data-ttu-id="3b92d-112">指定此 Cmdlet 取得 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3b92d-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="3b92d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b92d-113">-DefaultProfile</span></span>
<span data-ttu-id="3b92d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b92d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b92d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b92d-115">-Name</span></span>
<span data-ttu-id="3b92d-116">指定此 Cmdlet 取得路徑對應配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="3b92d-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="3b92d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b92d-117">CommonParameters</span></span>
<span data-ttu-id="3b92d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b92d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b92d-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3b92d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b92d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="3b92d-120">INPUTS</span></span>

### <span data-ttu-id="3b92d-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3b92d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3b92d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="3b92d-122">OUTPUTS</span></span>

### <span data-ttu-id="3b92d-123">PSApplicationGatewayUrlPathMap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3b92d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="3b92d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3b92d-124">NOTES</span></span>

## <span data-ttu-id="3b92d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b92d-125">RELATED LINKS</span></span>

[<span data-ttu-id="3b92d-126">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3b92d-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3b92d-127">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3b92d-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3b92d-128">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3b92d-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3b92d-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3b92d-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


