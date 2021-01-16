---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273431"
---
# <span data-ttu-id="59655-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="59655-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="59655-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59655-102">SYNOPSIS</span></span>
<span data-ttu-id="59655-103">更新應用程式閘道的 HTTP 攔截器中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="59655-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="59655-104">句法</span><span class="sxs-lookup"><span data-stu-id="59655-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59655-105">說明</span><span class="sxs-lookup"><span data-stu-id="59655-105">DESCRIPTION</span></span>
<span data-ttu-id="59655-106">**AzApplicationGatewayCustomError** Cmdlet 會在應用程式閘道的 HTTP 偵聽程式中更新自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="59655-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="59655-107">示例</span><span class="sxs-lookup"><span data-stu-id="59655-107">EXAMPLES</span></span>

### <span data-ttu-id="59655-108">範例1：從 HTTP 偵聽程式更新自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="59655-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="59655-109">這個命令會在 HTTP 偵聽程式 $listener 01 中，更新 HTTP 狀態碼502的自訂錯誤，並傳回已更新的監聽器。</span><span class="sxs-lookup"><span data-stu-id="59655-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="59655-110">參數</span><span class="sxs-lookup"><span data-stu-id="59655-110">PARAMETERS</span></span>

### <span data-ttu-id="59655-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="59655-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="59655-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="59655-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="59655-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59655-113">-DefaultProfile</span></span>
<span data-ttu-id="59655-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59655-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59655-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="59655-115">-HttpListener</span></span>
<span data-ttu-id="59655-116">應用程式閘道 Http 攔截器</span><span class="sxs-lookup"><span data-stu-id="59655-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="59655-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="59655-117">-StatusCode</span></span>
<span data-ttu-id="59655-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="59655-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="59655-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59655-119">CommonParameters</span></span>
<span data-ttu-id="59655-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59655-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59655-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59655-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59655-122">輸入</span><span class="sxs-lookup"><span data-stu-id="59655-122">INPUTS</span></span>

### <span data-ttu-id="59655-123">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="59655-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="59655-124">輸出</span><span class="sxs-lookup"><span data-stu-id="59655-124">OUTPUTS</span></span>

### <span data-ttu-id="59655-125">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="59655-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="59655-126">筆記</span><span class="sxs-lookup"><span data-stu-id="59655-126">NOTES</span></span>

## <span data-ttu-id="59655-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="59655-127">RELATED LINKS</span></span>

[<span data-ttu-id="59655-128">附加 AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="59655-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="59655-129">AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="59655-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="59655-130">移除-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="59655-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
