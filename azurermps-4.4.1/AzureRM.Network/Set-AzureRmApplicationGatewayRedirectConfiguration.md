---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23b27fc0b8b2a8d55a2af91d808b846e4de324a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624146"
---
# <span data-ttu-id="ab417-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab417-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="ab417-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab417-102">SYNOPSIS</span></span>
<span data-ttu-id="ab417-103">在現有的應用程式閘道上設定重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="ab417-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab417-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab417-104">SYNTAX</span></span>

### <span data-ttu-id="ab417-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab417-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab417-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ab417-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab417-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="ab417-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab417-108">說明</span><span class="sxs-lookup"><span data-stu-id="ab417-108">DESCRIPTION</span></span>
<span data-ttu-id="ab417-109">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會修改重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="ab417-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="ab417-110">示例</span><span class="sxs-lookup"><span data-stu-id="ab417-110">EXAMPLES</span></span>

### <span data-ttu-id="ab417-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ab417-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="ab417-112">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="ab417-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ab417-113">第二個命令會修改應用程式閘道的重新導向設定，以重新導向類型永久，並使用目標 url。</span><span class="sxs-lookup"><span data-stu-id="ab417-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="ab417-114">參數</span><span class="sxs-lookup"><span data-stu-id="ab417-114">PARAMETERS</span></span>

### <span data-ttu-id="ab417-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab417-115">-ApplicationGateway</span></span>
<span data-ttu-id="ab417-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab417-116">The applicationGateway</span></span>

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

### <span data-ttu-id="ab417-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="ab417-117">-IncludePath</span></span>
<span data-ttu-id="ab417-118">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="ab417-118">Include path in the redirected url.</span></span>
<span data-ttu-id="ab417-119">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="ab417-119">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab417-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="ab417-120">-IncludeQueryString</span></span>
<span data-ttu-id="ab417-121">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="ab417-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="ab417-122">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="ab417-122">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab417-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab417-123">-Name</span></span>
<span data-ttu-id="ab417-124">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="ab417-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="ab417-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="ab417-125">-RedirectType</span></span>
<span data-ttu-id="ab417-126">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="ab417-126">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab417-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="ab417-127">-TargetListener</span></span>
<span data-ttu-id="ab417-128">HTTPListener 以將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="ab417-128">HTTPListener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab417-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="ab417-129">-TargetListenerID</span></span>
<span data-ttu-id="ab417-130">要重新導向要求的偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="ab417-130">ID of  listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab417-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="ab417-131">-TargetUrl</span></span>
<span data-ttu-id="ab417-132">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="ab417-132">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab417-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab417-133">-DefaultProfile</span></span>
<span data-ttu-id="ab417-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab417-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab417-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab417-135">CommonParameters</span></span>
<span data-ttu-id="ab417-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab417-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab417-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab417-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab417-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ab417-138">INPUTS</span></span>

### <span data-ttu-id="ab417-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab417-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab417-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ab417-140">OUTPUTS</span></span>

### <span data-ttu-id="ab417-141">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab417-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab417-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ab417-142">NOTES</span></span>

## <span data-ttu-id="ab417-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab417-143">RELATED LINKS</span></span>

