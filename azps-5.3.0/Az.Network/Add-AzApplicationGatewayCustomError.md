---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: e3bac58fca1c405aeef3366cb3ec1ee1b01a0891
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287256"
---
# <span data-ttu-id="e8386-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e8386-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e8386-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8386-102">SYNOPSIS</span></span>
<span data-ttu-id="e8386-103">將自訂錯誤新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e8386-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="e8386-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8386-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8386-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8386-105">DESCRIPTION</span></span>
<span data-ttu-id="e8386-106">**載入 AzApplicationGatewayCustomError** Cmdlet 會將自訂錯誤新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e8386-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="e8386-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8386-107">EXAMPLES</span></span>

### <span data-ttu-id="e8386-108">範例1：將自訂錯誤新增至應用程式閘道層級</span><span class="sxs-lookup"><span data-stu-id="e8386-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e8386-109">這個命令會將 HTTP 狀態碼502的自訂錯誤新增至應用程式閘道 $appgw，然後返回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="e8386-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="e8386-110">範例2：將自訂錯誤新增至應用程式閘道攔截器層級</span><span class="sxs-lookup"><span data-stu-id="e8386-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e8386-111">這個命令會將 HTTP 狀態碼502的自訂錯誤新增到攔截器層級的應用程式閘道 $appgw，並傳回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="e8386-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="e8386-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8386-112">PARAMETERS</span></span>

### <span data-ttu-id="e8386-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8386-113">-ApplicationGateway</span></span>
<span data-ttu-id="e8386-114">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="e8386-114">The Application Gateway</span></span>

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

### <span data-ttu-id="e8386-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e8386-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e8386-116">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="e8386-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e8386-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8386-117">-DefaultProfile</span></span>
<span data-ttu-id="e8386-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8386-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8386-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e8386-119">-StatusCode</span></span>
<span data-ttu-id="e8386-120">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="e8386-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e8386-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8386-121">CommonParameters</span></span>
<span data-ttu-id="e8386-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8386-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8386-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8386-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8386-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e8386-124">INPUTS</span></span>

### <span data-ttu-id="e8386-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8386-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8386-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e8386-126">OUTPUTS</span></span>

### <span data-ttu-id="e8386-127">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8386-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e8386-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e8386-128">NOTES</span></span>

## <span data-ttu-id="e8386-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8386-129">RELATED LINKS</span></span>

[<span data-ttu-id="e8386-130">AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e8386-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e8386-131">新-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e8386-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e8386-132">移除-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e8386-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e8386-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e8386-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
