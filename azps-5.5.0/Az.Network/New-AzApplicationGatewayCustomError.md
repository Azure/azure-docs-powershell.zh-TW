---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140434"
---
# <span data-ttu-id="8814d-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8814d-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8814d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8814d-102">SYNOPSIS</span></span>
<span data-ttu-id="8814d-103">使用 HTTP 狀態碼與自訂錯誤頁面 url 來建立自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="8814d-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="8814d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8814d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8814d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8814d-105">DESCRIPTION</span></span>
<span data-ttu-id="8814d-106">**新的-AzApplicationGatewayCustomError** Cmdlet 會建立自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="8814d-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="8814d-107">示例</span><span class="sxs-lookup"><span data-stu-id="8814d-107">EXAMPLES</span></span>

### <span data-ttu-id="8814d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8814d-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="8814d-109">這個命令會建立 HTTP 狀態碼403的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="8814d-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="8814d-110">參數</span><span class="sxs-lookup"><span data-stu-id="8814d-110">PARAMETERS</span></span>

### <span data-ttu-id="8814d-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="8814d-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="8814d-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="8814d-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8814d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8814d-113">-DefaultProfile</span></span>
<span data-ttu-id="8814d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8814d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8814d-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="8814d-115">-StatusCode</span></span>
<span data-ttu-id="8814d-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="8814d-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8814d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8814d-117">CommonParameters</span></span>
<span data-ttu-id="8814d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8814d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8814d-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8814d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8814d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8814d-120">INPUTS</span></span>

### <span data-ttu-id="8814d-121">所有</span><span class="sxs-lookup"><span data-stu-id="8814d-121">None</span></span>

## <span data-ttu-id="8814d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="8814d-122">OUTPUTS</span></span>

### <span data-ttu-id="8814d-123">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8814d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8814d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="8814d-124">NOTES</span></span>

## <span data-ttu-id="8814d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="8814d-125">RELATED LINKS</span></span>

[<span data-ttu-id="8814d-126">附加 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8814d-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8814d-127">AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8814d-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8814d-128">移除-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8814d-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8814d-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8814d-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
