---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 449c3999a3041be819b9f5f665054969223c1557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625497"
---
# <span data-ttu-id="7d648-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d648-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7d648-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d648-102">SYNOPSIS</span></span>
<span data-ttu-id="7d648-103">將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7d648-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d648-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d648-104">SYNTAX</span></span>

### <span data-ttu-id="7d648-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d648-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d648-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7d648-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d648-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="7d648-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d648-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d648-108">DESCRIPTION</span></span>
<span data-ttu-id="7d648-109">**AzureRmApplicationGatewayRedirectConfiguration** Cmdlet 會將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7d648-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="7d648-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d648-110">EXAMPLES</span></span>

### <span data-ttu-id="7d648-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7d648-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="7d648-112">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7d648-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7d648-113">第二個命令會將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7d648-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="7d648-114">參數</span><span class="sxs-lookup"><span data-stu-id="7d648-114">PARAMETERS</span></span>

### <span data-ttu-id="7d648-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d648-115">-ApplicationGateway</span></span>
<span data-ttu-id="7d648-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d648-116">The applicationGateway</span></span>

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

### <span data-ttu-id="7d648-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="7d648-117">-IncludePath</span></span>
<span data-ttu-id="7d648-118">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="7d648-118">Include path in the redirected url.</span></span>
<span data-ttu-id="7d648-119">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="7d648-119">Default is true.</span></span>

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

### <span data-ttu-id="7d648-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="7d648-120">-IncludeQueryString</span></span>
<span data-ttu-id="7d648-121">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="7d648-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="7d648-122">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="7d648-122">Default is true.</span></span>

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

### <span data-ttu-id="7d648-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d648-123">-Name</span></span>
<span data-ttu-id="7d648-124">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="7d648-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="7d648-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="7d648-125">-RedirectType</span></span>
<span data-ttu-id="7d648-126">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="7d648-126">The type of redirect</span></span>

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

### <span data-ttu-id="7d648-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="7d648-127">-TargetListener</span></span>
<span data-ttu-id="7d648-128">HTTPListener 以將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="7d648-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="7d648-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="7d648-129">-TargetListenerID</span></span>
<span data-ttu-id="7d648-130">要重新導向要求的偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="7d648-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="7d648-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="7d648-131">-TargetUrl</span></span>
<span data-ttu-id="7d648-132">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="7d648-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="7d648-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d648-133">-DefaultProfile</span></span>
<span data-ttu-id="7d648-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d648-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d648-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d648-135">CommonParameters</span></span>
<span data-ttu-id="7d648-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d648-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d648-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d648-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d648-138">輸入</span><span class="sxs-lookup"><span data-stu-id="7d648-138">INPUTS</span></span>

### <span data-ttu-id="7d648-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d648-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7d648-140">輸出</span><span class="sxs-lookup"><span data-stu-id="7d648-140">OUTPUTS</span></span>

### <span data-ttu-id="7d648-141">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d648-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7d648-142">筆記</span><span class="sxs-lookup"><span data-stu-id="7d648-142">NOTES</span></span>

## <span data-ttu-id="7d648-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d648-143">RELATED LINKS</span></span>

