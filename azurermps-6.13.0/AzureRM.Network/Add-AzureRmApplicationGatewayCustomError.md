---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446965"
---
# <span data-ttu-id="c8bf6-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c8bf6-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c8bf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bf6-103">將自訂錯誤新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8bf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8bf6-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8bf6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="c8bf6-106">**載入 AzureRmApplicationGatewayCustomError** Cmdlet 會將自訂錯誤新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="c8bf6-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="c8bf6-108">範例1：將自訂錯誤新增至應用程式閘道層級</span><span class="sxs-lookup"><span data-stu-id="c8bf6-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="c8bf6-109">這個命令會將 HTTP 狀態碼502的自訂錯誤新增至應用程式閘道 $appgw，然後返回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="c8bf6-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8bf6-110">PARAMETERS</span></span>

### <span data-ttu-id="c8bf6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8bf6-111">-ApplicationGateway</span></span>
<span data-ttu-id="c8bf6-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="c8bf6-112">The Application Gateway</span></span>

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

### <span data-ttu-id="c8bf6-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c8bf6-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c8bf6-114">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c8bf6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bf6-115">-DefaultProfile</span></span>
<span data-ttu-id="c8bf6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8bf6-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c8bf6-117">-StatusCode</span></span>
<span data-ttu-id="c8bf6-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c8bf6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bf6-119">CommonParameters</span></span>
<span data-ttu-id="c8bf6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bf6-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8bf6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bf6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c8bf6-122">INPUTS</span></span>

### <span data-ttu-id="c8bf6-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8bf6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c8bf6-124">OUTPUTS</span></span>

### <span data-ttu-id="c8bf6-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8bf6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c8bf6-126">NOTES</span></span>

## <span data-ttu-id="c8bf6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8bf6-127">RELATED LINKS</span></span>
