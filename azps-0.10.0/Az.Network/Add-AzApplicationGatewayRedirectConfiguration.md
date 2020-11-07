---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 60b98db10aab4456ea8ca463f49ee3f7f58ffdd2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794530"
---
# <span data-ttu-id="4ff32-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff32-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="4ff32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ff32-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff32-103">將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4ff32-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="4ff32-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ff32-104">SYNTAX</span></span>

### <span data-ttu-id="4ff32-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ff32-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ff32-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4ff32-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ff32-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="4ff32-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ff32-108">說明</span><span class="sxs-lookup"><span data-stu-id="4ff32-108">DESCRIPTION</span></span>
<span data-ttu-id="4ff32-109">**AzApplicationGatewayRedirectConfiguration** Cmdlet 會將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4ff32-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="4ff32-110">示例</span><span class="sxs-lookup"><span data-stu-id="4ff32-110">EXAMPLES</span></span>

### <span data-ttu-id="4ff32-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4ff32-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="4ff32-112">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4ff32-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4ff32-113">第二個命令會將重新導向設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4ff32-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="4ff32-114">參數</span><span class="sxs-lookup"><span data-stu-id="4ff32-114">PARAMETERS</span></span>

### <span data-ttu-id="4ff32-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ff32-115">-ApplicationGateway</span></span>
<span data-ttu-id="4ff32-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ff32-116">The applicationGateway</span></span>

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

### <span data-ttu-id="4ff32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff32-117">-DefaultProfile</span></span>
<span data-ttu-id="4ff32-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ff32-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ff32-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="4ff32-119">-IncludePath</span></span>
<span data-ttu-id="4ff32-120">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="4ff32-120">Include path in the redirected url.</span></span>
<span data-ttu-id="4ff32-121">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="4ff32-121">Default is true.</span></span>

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

### <span data-ttu-id="4ff32-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="4ff32-122">-IncludeQueryString</span></span>
<span data-ttu-id="4ff32-123">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="4ff32-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="4ff32-124">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="4ff32-124">Default is true.</span></span>

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

### <span data-ttu-id="4ff32-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ff32-125">-Name</span></span>
<span data-ttu-id="4ff32-126">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="4ff32-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="4ff32-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="4ff32-127">-RedirectType</span></span>
<span data-ttu-id="4ff32-128">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="4ff32-128">The type of redirect</span></span>

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

### <span data-ttu-id="4ff32-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="4ff32-129">-TargetListener</span></span>
<span data-ttu-id="4ff32-130">HTTPListener 以將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="4ff32-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="4ff32-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="4ff32-131">-TargetListenerID</span></span>
<span data-ttu-id="4ff32-132">要重新導向要求的偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="4ff32-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="4ff32-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="4ff32-133">-TargetUrl</span></span>
<span data-ttu-id="4ff32-134">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="4ff32-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="4ff32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff32-135">CommonParameters</span></span>
<span data-ttu-id="4ff32-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ff32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff32-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ff32-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff32-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4ff32-138">INPUTS</span></span>

### <span data-ttu-id="4ff32-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ff32-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ff32-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4ff32-140">OUTPUTS</span></span>

### <span data-ttu-id="4ff32-141">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ff32-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ff32-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4ff32-142">NOTES</span></span>

## <span data-ttu-id="4ff32-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ff32-143">RELATED LINKS</span></span>

