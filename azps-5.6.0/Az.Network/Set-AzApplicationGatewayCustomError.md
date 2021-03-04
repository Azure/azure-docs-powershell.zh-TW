---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c06b78062500ddb5c33353c00814a46e919bd8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910973"
---
# <span data-ttu-id="bf0f9-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bf0f9-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bf0f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0f9-103">更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="bf0f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="bf0f9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf0f9-105">描述</span><span class="sxs-lookup"><span data-stu-id="bf0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="bf0f9-106">**Set-AzApplicationGatewayCustomError** Cmdlet 會更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="bf0f9-107">例子</span><span class="sxs-lookup"><span data-stu-id="bf0f9-107">EXAMPLES</span></span>

### <span data-ttu-id="bf0f9-108">範例 1：更新應用程式閘道中的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="bf0f9-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="bf0f9-109">此命令會更新應用程式閘道中 HTTP 狀態碼 502 的自訂錯誤$appgw，並返回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="bf0f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf0f9-110">PARAMETERS</span></span>

### <span data-ttu-id="bf0f9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf0f9-111">-ApplicationGateway</span></span>
<span data-ttu-id="bf0f9-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="bf0f9-112">The Application Gateway</span></span>

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

### <span data-ttu-id="bf0f9-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="bf0f9-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="bf0f9-114">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bf0f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0f9-115">-DefaultProfile</span></span>
<span data-ttu-id="bf0f9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0f9-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bf0f9-117">-StatusCode</span></span>
<span data-ttu-id="bf0f9-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bf0f9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0f9-119">CommonParameters</span></span>
<span data-ttu-id="bf0f9-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0f9-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bf0f9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0f9-122">輸入</span><span class="sxs-lookup"><span data-stu-id="bf0f9-122">INPUTS</span></span>

### <span data-ttu-id="bf0f9-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf0f9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf0f9-124">輸出</span><span class="sxs-lookup"><span data-stu-id="bf0f9-124">OUTPUTS</span></span>

### <span data-ttu-id="bf0f9-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bf0f9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bf0f9-126">筆記</span><span class="sxs-lookup"><span data-stu-id="bf0f9-126">NOTES</span></span>

## <span data-ttu-id="bf0f9-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf0f9-127">RELATED LINKS</span></span>

[<span data-ttu-id="bf0f9-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bf0f9-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bf0f9-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bf0f9-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bf0f9-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bf0f9-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bf0f9-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bf0f9-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
