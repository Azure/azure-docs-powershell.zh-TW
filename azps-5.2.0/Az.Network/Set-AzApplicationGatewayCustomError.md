---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284567"
---
# <span data-ttu-id="48a6d-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48a6d-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="48a6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="48a6d-103">更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="48a6d-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="48a6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="48a6d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48a6d-105">說明</span><span class="sxs-lookup"><span data-stu-id="48a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="48a6d-106">**AzApplicationGatewayCustomError** Cmdlet 會更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="48a6d-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="48a6d-107">示例</span><span class="sxs-lookup"><span data-stu-id="48a6d-107">EXAMPLES</span></span>

### <span data-ttu-id="48a6d-108">範例1：更新應用程式閘道中的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="48a6d-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="48a6d-109">這個命令會在應用程式閘道 $appgw 中，更新 HTTP 狀態碼502的自訂錯誤，並傳回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="48a6d-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="48a6d-110">參數</span><span class="sxs-lookup"><span data-stu-id="48a6d-110">PARAMETERS</span></span>

### <span data-ttu-id="48a6d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48a6d-111">-ApplicationGateway</span></span>
<span data-ttu-id="48a6d-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="48a6d-112">The Application Gateway</span></span>

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

### <span data-ttu-id="48a6d-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="48a6d-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="48a6d-114">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="48a6d-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="48a6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a6d-115">-DefaultProfile</span></span>
<span data-ttu-id="48a6d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48a6d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48a6d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="48a6d-117">-StatusCode</span></span>
<span data-ttu-id="48a6d-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="48a6d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="48a6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a6d-119">CommonParameters</span></span>
<span data-ttu-id="48a6d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48a6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a6d-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48a6d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a6d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="48a6d-122">INPUTS</span></span>

### <span data-ttu-id="48a6d-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="48a6d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48a6d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="48a6d-124">OUTPUTS</span></span>

### <span data-ttu-id="48a6d-125">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="48a6d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="48a6d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="48a6d-126">NOTES</span></span>

## <span data-ttu-id="48a6d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="48a6d-127">RELATED LINKS</span></span>

[<span data-ttu-id="48a6d-128">附加 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48a6d-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="48a6d-129">AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48a6d-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="48a6d-130">新-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48a6d-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="48a6d-131">移除-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48a6d-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
