---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: a59646c6214b3c4372eef9def61f67fe4a5bd912
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621508"
---
# <span data-ttu-id="0cb8f-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0cb8f-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0cb8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb8f-103">更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="0cb8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0cb8f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cb8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="0cb8f-105">DESCRIPTION</span></span>
<span data-ttu-id="0cb8f-106">**AzApplicationGatewayCustomError** Cmdlet 會更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="0cb8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="0cb8f-107">EXAMPLES</span></span>

### <span data-ttu-id="0cb8f-108">範例1：更新應用程式閘道中的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="0cb8f-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="0cb8f-109">這個命令會在應用程式閘道 $appgw 中，更新 HTTP 狀態碼502的自訂錯誤，並傳回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="0cb8f-110">參數</span><span class="sxs-lookup"><span data-stu-id="0cb8f-110">PARAMETERS</span></span>

### <span data-ttu-id="0cb8f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0cb8f-111">-ApplicationGateway</span></span>
<span data-ttu-id="0cb8f-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="0cb8f-112">The Application Gateway</span></span>

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

### <span data-ttu-id="0cb8f-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="0cb8f-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="0cb8f-114">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0cb8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb8f-115">-DefaultProfile</span></span>
<span data-ttu-id="0cb8f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cb8f-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="0cb8f-117">-StatusCode</span></span>
<span data-ttu-id="0cb8f-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0cb8f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb8f-119">CommonParameters</span></span>
<span data-ttu-id="0cb8f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb8f-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0cb8f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb8f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0cb8f-122">INPUTS</span></span>

### <span data-ttu-id="0cb8f-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0cb8f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0cb8f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0cb8f-124">OUTPUTS</span></span>

### <span data-ttu-id="0cb8f-125">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0cb8f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0cb8f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0cb8f-126">NOTES</span></span>

## <span data-ttu-id="0cb8f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cb8f-127">RELATED LINKS</span></span>

[<span data-ttu-id="0cb8f-128">附加 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0cb8f-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="0cb8f-129">AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0cb8f-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="0cb8f-130">新-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0cb8f-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="0cb8f-131">移除-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0cb8f-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
