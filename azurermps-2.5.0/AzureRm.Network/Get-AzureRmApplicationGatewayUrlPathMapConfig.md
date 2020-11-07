---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800117"
---
# <span data-ttu-id="ac047-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ac047-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="ac047-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac047-102">SYNOPSIS</span></span>
<span data-ttu-id="ac047-103">取得與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="ac047-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac047-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac047-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac047-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac047-105">DESCRIPTION</span></span>
<span data-ttu-id="ac047-106">**AzureRmApplicationGatewayURLPathMapConfig** Cmdlet 會取得 URL 路徑對應至後端伺服器池的陣列。</span><span class="sxs-lookup"><span data-stu-id="ac047-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ac047-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac047-107">EXAMPLES</span></span>

### <span data-ttu-id="ac047-108">範例1：取得 URL 路徑對應配置</span><span class="sxs-lookup"><span data-stu-id="ac047-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="ac047-109">這個命令會從位於名為「閘道」的應用程式閘道上的後端伺服器上，取得 URL 路徑對應配置。</span><span class="sxs-lookup"><span data-stu-id="ac047-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="ac047-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac047-110">PARAMETERS</span></span>

### <span data-ttu-id="ac047-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac047-111">-ApplicationGateway</span></span>
<span data-ttu-id="ac047-112">指定此 Cmdlet 取得 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ac047-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="ac047-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac047-113">-DefaultProfile</span></span>
<span data-ttu-id="ac047-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac047-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac047-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac047-115">-Name</span></span>
<span data-ttu-id="ac047-116">指定此 Cmdlet 取得路徑對應配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="ac047-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac047-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac047-117">CommonParameters</span></span>
<span data-ttu-id="ac047-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac047-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac047-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac047-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac047-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ac047-120">INPUTS</span></span>

### <span data-ttu-id="ac047-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac047-121">PSApplicationGateway</span></span>
<span data-ttu-id="ac047-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ac047-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ac047-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ac047-123">OUTPUTS</span></span>

### <span data-ttu-id="ac047-124">PSApplicationGatewayUrlPathMap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ac047-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="ac047-125">[System.object]. IEnumerable "1 [PSApplicationGatewayUrlPathMap] （）</span><span class="sxs-lookup"><span data-stu-id="ac047-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="ac047-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ac047-126">NOTES</span></span>

## <span data-ttu-id="ac047-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac047-127">RELATED LINKS</span></span>

[<span data-ttu-id="ac047-128">附加 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ac047-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ac047-129">新-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ac047-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ac047-130">移除-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ac047-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ac047-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ac047-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


