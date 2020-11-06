---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446942"
---
# <span data-ttu-id="77ae1-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="77ae1-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="77ae1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="77ae1-103">從應用程式閘道移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="77ae1-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77ae1-104">句法</span><span class="sxs-lookup"><span data-stu-id="77ae1-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77ae1-105">說明</span><span class="sxs-lookup"><span data-stu-id="77ae1-105">DESCRIPTION</span></span>
<span data-ttu-id="77ae1-106">**AzureRmApplicationGatewayCustomError** Cmdlet 會從應用程式閘道中移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="77ae1-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="77ae1-107">示例</span><span class="sxs-lookup"><span data-stu-id="77ae1-107">EXAMPLES</span></span>

### <span data-ttu-id="77ae1-108">範例1：從應用程式閘道移除自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="77ae1-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="77ae1-109">這個命令會從應用程式閘道 $appgw 中移除 HTTP 狀態碼502的自訂錯誤，並傳回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="77ae1-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="77ae1-110">參數</span><span class="sxs-lookup"><span data-stu-id="77ae1-110">PARAMETERS</span></span>

### <span data-ttu-id="77ae1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77ae1-111">-ApplicationGateway</span></span>
<span data-ttu-id="77ae1-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="77ae1-112">The Application Gateway</span></span>

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

### <span data-ttu-id="77ae1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ae1-113">-DefaultProfile</span></span>
<span data-ttu-id="77ae1-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77ae1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77ae1-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="77ae1-115">-StatusCode</span></span>
<span data-ttu-id="77ae1-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="77ae1-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="77ae1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ae1-117">CommonParameters</span></span>
<span data-ttu-id="77ae1-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77ae1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ae1-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77ae1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ae1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="77ae1-120">INPUTS</span></span>

### <span data-ttu-id="77ae1-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="77ae1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77ae1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="77ae1-122">OUTPUTS</span></span>

### <span data-ttu-id="77ae1-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="77ae1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77ae1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="77ae1-124">NOTES</span></span>

## <span data-ttu-id="77ae1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="77ae1-125">RELATED LINKS</span></span>
