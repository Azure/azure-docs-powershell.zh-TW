---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789945"
---
# <span data-ttu-id="fddb8-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fddb8-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="fddb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fddb8-102">SYNOPSIS</span></span>
<span data-ttu-id="fddb8-103">建立應用程式閘道的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="fddb8-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="fddb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="fddb8-104">SYNTAX</span></span>

### <span data-ttu-id="fddb8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fddb8-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fddb8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fddb8-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fddb8-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="fddb8-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fddb8-108">說明</span><span class="sxs-lookup"><span data-stu-id="fddb8-108">DESCRIPTION</span></span>
<span data-ttu-id="fddb8-109">**新的-AzApplicationGatewayRedirectConfiguration** Cmdlet 會為應用程式閘道建立重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="fddb8-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="fddb8-110">示例</span><span class="sxs-lookup"><span data-stu-id="fddb8-110">EXAMPLES</span></span>

### <span data-ttu-id="fddb8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fddb8-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="fddb8-112">這個命令會建立名為 Redirect01 的重新導向配置，並將結果儲存在名為 $RedirectConfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="fddb8-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="fddb8-113">參數</span><span class="sxs-lookup"><span data-stu-id="fddb8-113">PARAMETERS</span></span>

### <span data-ttu-id="fddb8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddb8-114">-DefaultProfile</span></span>
<span data-ttu-id="fddb8-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fddb8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fddb8-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="fddb8-116">-IncludePath</span></span>
<span data-ttu-id="fddb8-117">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="fddb8-117">Include path in the redirected url.</span></span>
<span data-ttu-id="fddb8-118">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="fddb8-118">Default is true.</span></span>

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

### <span data-ttu-id="fddb8-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="fddb8-119">-IncludeQueryString</span></span>
<span data-ttu-id="fddb8-120">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="fddb8-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="fddb8-121">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="fddb8-121">Default is true.</span></span>

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

### <span data-ttu-id="fddb8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fddb8-122">-Name</span></span>
<span data-ttu-id="fddb8-123">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="fddb8-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="fddb8-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="fddb8-124">-RedirectType</span></span>
<span data-ttu-id="fddb8-125">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="fddb8-125">The type of redirect</span></span>

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

### <span data-ttu-id="fddb8-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="fddb8-126">-TargetListener</span></span>
<span data-ttu-id="fddb8-127">[HTTP 偵聽程式] 可將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="fddb8-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="fddb8-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="fddb8-128">-TargetListenerID</span></span>
<span data-ttu-id="fddb8-129">要將要求重新導向至的 HTTP 偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="fddb8-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="fddb8-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="fddb8-130">-TargetUrl</span></span>
<span data-ttu-id="fddb8-131">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="fddb8-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="fddb8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddb8-132">CommonParameters</span></span>
<span data-ttu-id="fddb8-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fddb8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddb8-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fddb8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddb8-135">輸入</span><span class="sxs-lookup"><span data-stu-id="fddb8-135">INPUTS</span></span>

### <span data-ttu-id="fddb8-136">所有</span><span class="sxs-lookup"><span data-stu-id="fddb8-136">None</span></span>

## <span data-ttu-id="fddb8-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fddb8-137">OUTPUTS</span></span>

### <span data-ttu-id="fddb8-138">PSApplicationGatewayRedirectConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fddb8-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="fddb8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="fddb8-139">NOTES</span></span>

## <span data-ttu-id="fddb8-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="fddb8-140">RELATED LINKS</span></span>

[<span data-ttu-id="fddb8-141">附加 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fddb8-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fddb8-142">AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fddb8-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fddb8-143">移除-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fddb8-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fddb8-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fddb8-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
