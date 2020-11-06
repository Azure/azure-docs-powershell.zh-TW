---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453663"
---
# <span data-ttu-id="fed62-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fed62-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="fed62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fed62-102">SYNOPSIS</span></span>
<span data-ttu-id="fed62-103">使用 HTTP 狀態碼與自訂錯誤頁面 url 來建立自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="fed62-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fed62-104">句法</span><span class="sxs-lookup"><span data-stu-id="fed62-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fed62-105">說明</span><span class="sxs-lookup"><span data-stu-id="fed62-105">DESCRIPTION</span></span>
<span data-ttu-id="fed62-106">**新的-AzureRmApplicationGatewayCustomError** Cmdlet 會建立自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="fed62-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="fed62-107">示例</span><span class="sxs-lookup"><span data-stu-id="fed62-107">EXAMPLES</span></span>

### <span data-ttu-id="fed62-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fed62-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="fed62-109">這個命令會建立 HTTP 狀態碼403的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="fed62-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="fed62-110">參數</span><span class="sxs-lookup"><span data-stu-id="fed62-110">PARAMETERS</span></span>

### <span data-ttu-id="fed62-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="fed62-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="fed62-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="fed62-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="fed62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed62-113">-DefaultProfile</span></span>
<span data-ttu-id="fed62-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fed62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fed62-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="fed62-115">-StatusCode</span></span>
<span data-ttu-id="fed62-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="fed62-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="fed62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed62-117">CommonParameters</span></span>
<span data-ttu-id="fed62-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fed62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fed62-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fed62-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed62-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fed62-120">INPUTS</span></span>

### <span data-ttu-id="fed62-121">所有</span><span class="sxs-lookup"><span data-stu-id="fed62-121">None</span></span>

## <span data-ttu-id="fed62-122">輸出</span><span class="sxs-lookup"><span data-stu-id="fed62-122">OUTPUTS</span></span>

### <span data-ttu-id="fed62-123">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fed62-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="fed62-124">筆記</span><span class="sxs-lookup"><span data-stu-id="fed62-124">NOTES</span></span>

## <span data-ttu-id="fed62-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="fed62-125">RELATED LINKS</span></span>
