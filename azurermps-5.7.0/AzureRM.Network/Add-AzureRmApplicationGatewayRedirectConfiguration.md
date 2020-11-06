---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 73d60d86110893005e72152c08e82d4152b1c482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446223"
---
# <span data-ttu-id="30605-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30605-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="30605-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30605-102">SYNOPSIS</span></span>
<span data-ttu-id="30605-103">將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="30605-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30605-104">句法</span><span class="sxs-lookup"><span data-stu-id="30605-104">SYNTAX</span></span>

### <span data-ttu-id="30605-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="30605-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30605-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="30605-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30605-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="30605-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30605-108">說明</span><span class="sxs-lookup"><span data-stu-id="30605-108">DESCRIPTION</span></span>
<span data-ttu-id="30605-109">**AzureRmApplicationGatewayRedirectConfiguration** Cmdlet 會將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="30605-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="30605-110">示例</span><span class="sxs-lookup"><span data-stu-id="30605-110">EXAMPLES</span></span>

### <span data-ttu-id="30605-111">範例1</span><span class="sxs-lookup"><span data-stu-id="30605-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="30605-112">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="30605-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30605-113">第二個命令會將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="30605-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="30605-114">參數</span><span class="sxs-lookup"><span data-stu-id="30605-114">PARAMETERS</span></span>

### <span data-ttu-id="30605-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30605-115">-ApplicationGateway</span></span>
<span data-ttu-id="30605-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30605-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30605-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30605-117">-DefaultProfile</span></span>
<span data-ttu-id="30605-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30605-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30605-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="30605-119">-IncludePath</span></span>
<span data-ttu-id="30605-120">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="30605-120">Include path in the redirected url.</span></span>
<span data-ttu-id="30605-121">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="30605-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30605-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="30605-122">-IncludeQueryString</span></span>
<span data-ttu-id="30605-123">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="30605-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="30605-124">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="30605-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30605-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="30605-125">-Name</span></span>
<span data-ttu-id="30605-126">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="30605-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="30605-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="30605-127">-RedirectType</span></span>
<span data-ttu-id="30605-128">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="30605-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30605-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="30605-129">-TargetListener</span></span>
<span data-ttu-id="30605-130">HTTPListener 以將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="30605-130">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30605-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="30605-131">-TargetListenerID</span></span>
<span data-ttu-id="30605-132">要重新導向要求的偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="30605-132">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30605-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="30605-133">-TargetUrl</span></span>
<span data-ttu-id="30605-134">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="30605-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30605-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30605-135">CommonParameters</span></span>
<span data-ttu-id="30605-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30605-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30605-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30605-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30605-138">輸入</span><span class="sxs-lookup"><span data-stu-id="30605-138">INPUTS</span></span>

### <span data-ttu-id="30605-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="30605-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30605-140">輸出</span><span class="sxs-lookup"><span data-stu-id="30605-140">OUTPUTS</span></span>

### <span data-ttu-id="30605-141">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="30605-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30605-142">筆記</span><span class="sxs-lookup"><span data-stu-id="30605-142">NOTES</span></span>

## <span data-ttu-id="30605-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="30605-143">RELATED LINKS</span></span>

