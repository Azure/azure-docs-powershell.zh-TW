---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 23cb65073f25f65a4e09f3b4a28891cff4e49c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625801"
---
# <span data-ttu-id="f31ca-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f31ca-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f31ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f31ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f31ca-103">將自訂錯誤新增至應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="f31ca-103">Adds a custom error to a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f31ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="f31ca-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f31ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="f31ca-105">DESCRIPTION</span></span>
<span data-ttu-id="f31ca-106">**AzureRmApplicationGatewayCustomError** Cmdlet 會將自訂錯誤新增至應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="f31ca-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f31ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="f31ca-107">EXAMPLES</span></span>

### <span data-ttu-id="f31ca-108">範例1：將自訂錯誤新增至 HTTP 攔截器層級</span><span class="sxs-lookup"><span data-stu-id="f31ca-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f31ca-109">這個命令會將 HTTP 狀態碼502的自訂錯誤新增至 HTTP 偵聽程式 $listener 01，並傳回更新的監聽器。</span><span class="sxs-lookup"><span data-stu-id="f31ca-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="f31ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="f31ca-110">PARAMETERS</span></span>

### <span data-ttu-id="f31ca-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f31ca-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f31ca-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="f31ca-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f31ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31ca-113">-DefaultProfile</span></span>
<span data-ttu-id="f31ca-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f31ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31ca-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f31ca-115">-HttpListener</span></span>
<span data-ttu-id="f31ca-116">應用程式閘道 Http 攔截器</span><span class="sxs-lookup"><span data-stu-id="f31ca-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f31ca-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f31ca-117">-StatusCode</span></span>
<span data-ttu-id="f31ca-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="f31ca-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f31ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31ca-119">CommonParameters</span></span>
<span data-ttu-id="f31ca-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f31ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f31ca-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f31ca-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31ca-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f31ca-122">INPUTS</span></span>

### <span data-ttu-id="f31ca-123">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f31ca-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f31ca-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f31ca-124">OUTPUTS</span></span>

### <span data-ttu-id="f31ca-125">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f31ca-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f31ca-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f31ca-126">NOTES</span></span>

## <span data-ttu-id="f31ca-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f31ca-127">RELATED LINKS</span></span>
