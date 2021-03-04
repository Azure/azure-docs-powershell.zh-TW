---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: f82882a4975c2f873362ece62f6eac9e6b7a53a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912749"
---
# <span data-ttu-id="985ff-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="985ff-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="985ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="985ff-102">SYNOPSIS</span></span>
<span data-ttu-id="985ff-103">獲得後端伺服器資料庫 URL 路徑的陣列。</span><span class="sxs-lookup"><span data-stu-id="985ff-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="985ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="985ff-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="985ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="985ff-105">DESCRIPTION</span></span>
<span data-ttu-id="985ff-106">**Get-AzApplicationGatewayURLPathMapConfig** Cmdlet 會取得後端伺服器集區 URL 路徑的陣列。</span><span class="sxs-lookup"><span data-stu-id="985ff-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="985ff-107">例子</span><span class="sxs-lookup"><span data-stu-id="985ff-107">EXAMPLES</span></span>

### <span data-ttu-id="985ff-108">範例 1：取得 URL 路徑映射組</span><span class="sxs-lookup"><span data-stu-id="985ff-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="985ff-109">此命令會從名為閘道的應用程式閘道上的後端伺服器，獲得 URL 路徑地圖組配置。</span><span class="sxs-lookup"><span data-stu-id="985ff-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="985ff-110">參數</span><span class="sxs-lookup"><span data-stu-id="985ff-110">PARAMETERS</span></span>

### <span data-ttu-id="985ff-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="985ff-111">-ApplicationGateway</span></span>
<span data-ttu-id="985ff-112">指定此 Cmdlet 會獲得 URL 路徑地圖配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="985ff-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="985ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985ff-113">-DefaultProfile</span></span>
<span data-ttu-id="985ff-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="985ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="985ff-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="985ff-115">-Name</span></span>
<span data-ttu-id="985ff-116">指定此 Cmdlet 取得路徑地圖配置的 URL 路徑地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="985ff-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="985ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985ff-117">CommonParameters</span></span>
<span data-ttu-id="985ff-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="985ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985ff-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="985ff-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985ff-120">輸入</span><span class="sxs-lookup"><span data-stu-id="985ff-120">INPUTS</span></span>

### <span data-ttu-id="985ff-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="985ff-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="985ff-122">輸出</span><span class="sxs-lookup"><span data-stu-id="985ff-122">OUTPUTS</span></span>

### <span data-ttu-id="985ff-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="985ff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="985ff-124">筆記</span><span class="sxs-lookup"><span data-stu-id="985ff-124">NOTES</span></span>

## <span data-ttu-id="985ff-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="985ff-125">RELATED LINKS</span></span>

[<span data-ttu-id="985ff-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="985ff-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="985ff-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="985ff-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="985ff-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="985ff-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="985ff-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="985ff-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


