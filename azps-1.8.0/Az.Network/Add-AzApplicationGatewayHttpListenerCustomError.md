---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8718d79abef18217a727916d36c09e19de2a2de4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622188"
---
# <span data-ttu-id="498bd-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="498bd-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="498bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="498bd-102">SYNOPSIS</span></span>
<span data-ttu-id="498bd-103">將自訂錯誤新增至應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="498bd-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="498bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="498bd-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="498bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="498bd-105">DESCRIPTION</span></span>
<span data-ttu-id="498bd-106">**AzApplicationGatewayCustomError** Cmdlet 會將自訂錯誤新增至應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="498bd-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="498bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="498bd-107">EXAMPLES</span></span>

### <span data-ttu-id="498bd-108">範例1：將自訂錯誤新增至 HTTP 攔截器層級</span><span class="sxs-lookup"><span data-stu-id="498bd-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="498bd-109">這個命令會將 HTTP 狀態碼502的自訂錯誤新增至 HTTP 偵聽程式 $listener 01，並傳回更新的監聽器。</span><span class="sxs-lookup"><span data-stu-id="498bd-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="498bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="498bd-110">PARAMETERS</span></span>

### <span data-ttu-id="498bd-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="498bd-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="498bd-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="498bd-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="498bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498bd-113">-DefaultProfile</span></span>
<span data-ttu-id="498bd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="498bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498bd-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="498bd-115">-HttpListener</span></span>
<span data-ttu-id="498bd-116">應用程式閘道 Http 攔截器</span><span class="sxs-lookup"><span data-stu-id="498bd-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498bd-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="498bd-117">-StatusCode</span></span>
<span data-ttu-id="498bd-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="498bd-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="498bd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498bd-119">CommonParameters</span></span>
<span data-ttu-id="498bd-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="498bd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498bd-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="498bd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498bd-122">輸入</span><span class="sxs-lookup"><span data-stu-id="498bd-122">INPUTS</span></span>

### <span data-ttu-id="498bd-123">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="498bd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="498bd-124">輸出</span><span class="sxs-lookup"><span data-stu-id="498bd-124">OUTPUTS</span></span>

### <span data-ttu-id="498bd-125">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="498bd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="498bd-126">筆記</span><span class="sxs-lookup"><span data-stu-id="498bd-126">NOTES</span></span>

## <span data-ttu-id="498bd-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="498bd-127">RELATED LINKS</span></span>

[<span data-ttu-id="498bd-128">AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="498bd-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="498bd-129">移除-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="498bd-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="498bd-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="498bd-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
