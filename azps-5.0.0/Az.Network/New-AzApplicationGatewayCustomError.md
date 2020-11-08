---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141402"
---
# <span data-ttu-id="e3525-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e3525-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e3525-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3525-102">SYNOPSIS</span></span>
<span data-ttu-id="e3525-103">使用 HTTP 狀態碼與自訂錯誤頁面 url 來建立自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="e3525-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="e3525-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3525-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3525-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3525-105">DESCRIPTION</span></span>
<span data-ttu-id="e3525-106">**新的-AzApplicationGatewayCustomError** Cmdlet 會建立自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3525-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="e3525-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3525-107">EXAMPLES</span></span>

### <span data-ttu-id="e3525-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e3525-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="e3525-109">這個命令會建立 HTTP 狀態碼403的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3525-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="e3525-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3525-110">PARAMETERS</span></span>

### <span data-ttu-id="e3525-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e3525-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e3525-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="e3525-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e3525-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3525-113">-DefaultProfile</span></span>
<span data-ttu-id="e3525-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3525-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3525-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e3525-115">-StatusCode</span></span>
<span data-ttu-id="e3525-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="e3525-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e3525-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3525-117">CommonParameters</span></span>
<span data-ttu-id="e3525-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3525-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3525-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3525-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3525-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e3525-120">INPUTS</span></span>

### <span data-ttu-id="e3525-121">所有</span><span class="sxs-lookup"><span data-stu-id="e3525-121">None</span></span>

## <span data-ttu-id="e3525-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e3525-122">OUTPUTS</span></span>

### <span data-ttu-id="e3525-123">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3525-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e3525-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e3525-124">NOTES</span></span>

## <span data-ttu-id="e3525-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3525-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3525-126">附加 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e3525-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e3525-127">AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e3525-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e3525-128">移除-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e3525-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e3525-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e3525-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
