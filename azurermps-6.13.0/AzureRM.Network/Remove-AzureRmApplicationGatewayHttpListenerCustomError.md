---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446938"
---
# <span data-ttu-id="26f27-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="26f27-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="26f27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26f27-102">SYNOPSIS</span></span>
<span data-ttu-id="26f27-103">從應用程式閘道的 HTTP 攔截器中移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="26f27-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26f27-104">句法</span><span class="sxs-lookup"><span data-stu-id="26f27-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26f27-105">說明</span><span class="sxs-lookup"><span data-stu-id="26f27-105">DESCRIPTION</span></span>
<span data-ttu-id="26f27-106">**AzureRmApplicationGatewayCustomError** Cmdlet 會從應用程式閘道的 HTTP 攔截器中移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="26f27-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="26f27-107">示例</span><span class="sxs-lookup"><span data-stu-id="26f27-107">EXAMPLES</span></span>

### <span data-ttu-id="26f27-108">範例1：移除來自 HTTP 偵聽程式的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="26f27-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="26f27-109">這個命令會從 HTTP 偵聽程式 $listener 01 中移除 HTTP 狀態碼502的自訂錯誤，並傳回更新的監聽程式。</span><span class="sxs-lookup"><span data-stu-id="26f27-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="26f27-110">參數</span><span class="sxs-lookup"><span data-stu-id="26f27-110">PARAMETERS</span></span>

### <span data-ttu-id="26f27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f27-111">-DefaultProfile</span></span>
<span data-ttu-id="26f27-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26f27-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f27-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="26f27-113">-HttpListener</span></span>
<span data-ttu-id="26f27-114">應用程式閘道 Http 攔截器</span><span class="sxs-lookup"><span data-stu-id="26f27-114">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26f27-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="26f27-115">-StatusCode</span></span>
<span data-ttu-id="26f27-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="26f27-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="26f27-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f27-117">CommonParameters</span></span>
<span data-ttu-id="26f27-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26f27-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26f27-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26f27-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f27-120">輸入</span><span class="sxs-lookup"><span data-stu-id="26f27-120">INPUTS</span></span>

### <span data-ttu-id="26f27-121">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26f27-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="26f27-122">輸出</span><span class="sxs-lookup"><span data-stu-id="26f27-122">OUTPUTS</span></span>

### <span data-ttu-id="26f27-123">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26f27-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="26f27-124">筆記</span><span class="sxs-lookup"><span data-stu-id="26f27-124">NOTES</span></span>

## <span data-ttu-id="26f27-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f27-125">RELATED LINKS</span></span>
