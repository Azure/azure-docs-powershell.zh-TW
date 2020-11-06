---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449008"
---
# <span data-ttu-id="34883-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="34883-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="34883-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34883-102">SYNOPSIS</span></span>
<span data-ttu-id="34883-103">更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="34883-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34883-104">句法</span><span class="sxs-lookup"><span data-stu-id="34883-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34883-105">說明</span><span class="sxs-lookup"><span data-stu-id="34883-105">DESCRIPTION</span></span>
<span data-ttu-id="34883-106">**AzureRmApplicationGatewayCustomError** Cmdlet 會更新應用程式閘道中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="34883-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="34883-107">示例</span><span class="sxs-lookup"><span data-stu-id="34883-107">EXAMPLES</span></span>

### <span data-ttu-id="34883-108">範例1：更新應用程式閘道中的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="34883-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="34883-109">這個命令會在應用程式閘道 $appgw 中，更新 HTTP 狀態碼502的自訂錯誤，並傳回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="34883-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="34883-110">參數</span><span class="sxs-lookup"><span data-stu-id="34883-110">PARAMETERS</span></span>

### <span data-ttu-id="34883-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34883-111">-ApplicationGateway</span></span>
<span data-ttu-id="34883-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="34883-112">The Application Gateway</span></span>

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

### <span data-ttu-id="34883-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="34883-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="34883-114">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="34883-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="34883-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34883-115">-DefaultProfile</span></span>
<span data-ttu-id="34883-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34883-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34883-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="34883-117">-StatusCode</span></span>
<span data-ttu-id="34883-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="34883-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="34883-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34883-119">CommonParameters</span></span>
<span data-ttu-id="34883-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34883-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34883-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34883-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34883-122">輸入</span><span class="sxs-lookup"><span data-stu-id="34883-122">INPUTS</span></span>

### <span data-ttu-id="34883-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34883-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34883-124">輸出</span><span class="sxs-lookup"><span data-stu-id="34883-124">OUTPUTS</span></span>

### <span data-ttu-id="34883-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34883-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34883-126">筆記</span><span class="sxs-lookup"><span data-stu-id="34883-126">NOTES</span></span>

## <span data-ttu-id="34883-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="34883-127">RELATED LINKS</span></span>
