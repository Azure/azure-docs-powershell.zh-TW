---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 92d970d87b79b1a392b6da73c567d6e8445cfd90
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794448"
---
# <span data-ttu-id="f04ce-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f04ce-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f04ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f04ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f04ce-103">取得與後端伺服器池的 URL 路徑對應陣列。</span><span class="sxs-lookup"><span data-stu-id="f04ce-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f04ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="f04ce-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f04ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="f04ce-105">DESCRIPTION</span></span>
<span data-ttu-id="f04ce-106">**AzApplicationGatewayURLPathMapConfig** Cmdlet 會取得 URL 路徑對應至後端伺服器池的陣列。</span><span class="sxs-lookup"><span data-stu-id="f04ce-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f04ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="f04ce-107">EXAMPLES</span></span>

### <span data-ttu-id="f04ce-108">範例1：取得 URL 路徑對應配置</span><span class="sxs-lookup"><span data-stu-id="f04ce-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="f04ce-109">這個命令會從位於名為「閘道」的應用程式閘道上的後端伺服器上，取得 URL 路徑對應配置。</span><span class="sxs-lookup"><span data-stu-id="f04ce-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="f04ce-110">參數</span><span class="sxs-lookup"><span data-stu-id="f04ce-110">PARAMETERS</span></span>

### <span data-ttu-id="f04ce-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f04ce-111">-ApplicationGateway</span></span>
<span data-ttu-id="f04ce-112">指定此 Cmdlet 取得 URL 路徑對應設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f04ce-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="f04ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f04ce-113">-DefaultProfile</span></span>
<span data-ttu-id="f04ce-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f04ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f04ce-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f04ce-115">-Name</span></span>
<span data-ttu-id="f04ce-116">指定此 Cmdlet 取得路徑對應配置的 URL 路徑對應名稱。</span><span class="sxs-lookup"><span data-stu-id="f04ce-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="f04ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04ce-117">CommonParameters</span></span>
<span data-ttu-id="f04ce-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f04ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04ce-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f04ce-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04ce-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f04ce-120">INPUTS</span></span>

### <span data-ttu-id="f04ce-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f04ce-121">PSApplicationGateway</span></span>
<span data-ttu-id="f04ce-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f04ce-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f04ce-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f04ce-123">OUTPUTS</span></span>

### <span data-ttu-id="f04ce-124">PSApplicationGatewayUrlPathMap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f04ce-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="f04ce-125">[System.object]. IEnumerable "1 [PSApplicationGatewayUrlPathMap] （）</span><span class="sxs-lookup"><span data-stu-id="f04ce-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="f04ce-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f04ce-126">NOTES</span></span>

## <span data-ttu-id="f04ce-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f04ce-127">RELATED LINKS</span></span>

[<span data-ttu-id="f04ce-128">附加 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f04ce-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f04ce-129">新-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f04ce-129">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f04ce-130">移除-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f04ce-130">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f04ce-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f04ce-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


