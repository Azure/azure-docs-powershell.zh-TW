---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 377145933832c587691ed30db08754ef1e6f1f64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906902"
---
# <span data-ttu-id="00aad-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00aad-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="00aad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00aad-102">SYNOPSIS</span></span>
<span data-ttu-id="00aad-103">使用 HTTP 狀態碼和自訂錯誤頁面 URL 建立自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="00aad-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="00aad-104">語法</span><span class="sxs-lookup"><span data-stu-id="00aad-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00aad-105">描述</span><span class="sxs-lookup"><span data-stu-id="00aad-105">DESCRIPTION</span></span>
<span data-ttu-id="00aad-106">**New-AzApplicationGatewayCustomError** Cmdlet 會建立自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="00aad-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="00aad-107">例子</span><span class="sxs-lookup"><span data-stu-id="00aad-107">EXAMPLES</span></span>

### <span data-ttu-id="00aad-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="00aad-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="00aad-109">此命令會建立 HTTP 狀態碼 403 的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="00aad-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="00aad-110">參數</span><span class="sxs-lookup"><span data-stu-id="00aad-110">PARAMETERS</span></span>

### <span data-ttu-id="00aad-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="00aad-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="00aad-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="00aad-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="00aad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00aad-113">-DefaultProfile</span></span>
<span data-ttu-id="00aad-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00aad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00aad-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="00aad-115">-StatusCode</span></span>
<span data-ttu-id="00aad-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="00aad-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="00aad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00aad-117">CommonParameters</span></span>
<span data-ttu-id="00aad-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00aad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00aad-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00aad-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00aad-120">輸入</span><span class="sxs-lookup"><span data-stu-id="00aad-120">INPUTS</span></span>

### <span data-ttu-id="00aad-121">沒有</span><span class="sxs-lookup"><span data-stu-id="00aad-121">None</span></span>

## <span data-ttu-id="00aad-122">輸出</span><span class="sxs-lookup"><span data-stu-id="00aad-122">OUTPUTS</span></span>

### <span data-ttu-id="00aad-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00aad-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="00aad-124">筆記</span><span class="sxs-lookup"><span data-stu-id="00aad-124">NOTES</span></span>

## <span data-ttu-id="00aad-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="00aad-125">RELATED LINKS</span></span>

[<span data-ttu-id="00aad-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00aad-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="00aad-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00aad-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="00aad-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00aad-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="00aad-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00aad-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
