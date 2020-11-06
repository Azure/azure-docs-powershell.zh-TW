---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ac85a308b73d822846a2f2a0a7b9ddf9ccc05cbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622069"
---
# <span data-ttu-id="cdf31-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cdf31-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="cdf31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdf31-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf31-103">取得與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="cdf31-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cdf31-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdf31-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdf31-105">說明</span><span class="sxs-lookup"><span data-stu-id="cdf31-105">DESCRIPTION</span></span>
<span data-ttu-id="cdf31-106">**AzApplicationGatewayURLPathMapConfig** Cmdlet 會取得 URL 路徑對應至後端伺服器池的陣列。</span><span class="sxs-lookup"><span data-stu-id="cdf31-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="cdf31-107">示例</span><span class="sxs-lookup"><span data-stu-id="cdf31-107">EXAMPLES</span></span>

### <span data-ttu-id="cdf31-108">範例1：取得 URL 路徑對應配置</span><span class="sxs-lookup"><span data-stu-id="cdf31-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="cdf31-109">這個命令會從位於名為「閘道」的應用程式閘道上的後端伺服器上，取得 URL 路徑對應配置。</span><span class="sxs-lookup"><span data-stu-id="cdf31-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="cdf31-110">參數</span><span class="sxs-lookup"><span data-stu-id="cdf31-110">PARAMETERS</span></span>

### <span data-ttu-id="cdf31-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cdf31-111">-ApplicationGateway</span></span>
<span data-ttu-id="cdf31-112">指定此 Cmdlet 取得 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="cdf31-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="cdf31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf31-113">-DefaultProfile</span></span>
<span data-ttu-id="cdf31-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdf31-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdf31-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdf31-115">-Name</span></span>
<span data-ttu-id="cdf31-116">指定此 Cmdlet 取得路徑對應配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="cdf31-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="cdf31-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf31-117">CommonParameters</span></span>
<span data-ttu-id="cdf31-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdf31-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf31-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cdf31-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf31-120">輸入</span><span class="sxs-lookup"><span data-stu-id="cdf31-120">INPUTS</span></span>

### <span data-ttu-id="cdf31-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cdf31-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cdf31-122">輸出</span><span class="sxs-lookup"><span data-stu-id="cdf31-122">OUTPUTS</span></span>

### <span data-ttu-id="cdf31-123">PSApplicationGatewayUrlPathMap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cdf31-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="cdf31-124">筆記</span><span class="sxs-lookup"><span data-stu-id="cdf31-124">NOTES</span></span>

## <span data-ttu-id="cdf31-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdf31-125">RELATED LINKS</span></span>

[<span data-ttu-id="cdf31-126">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cdf31-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cdf31-127">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cdf31-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cdf31-128">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cdf31-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="cdf31-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cdf31-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

