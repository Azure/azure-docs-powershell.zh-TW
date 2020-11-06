---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 07820860f1a6a43f51f8436fa3ba28d6238de087
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453703"
---
# <span data-ttu-id="6f42f-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6f42f-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="6f42f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f42f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f42f-103">將後端 HTTP 設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6f42f-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f42f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f42f-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f42f-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f42f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f42f-106">Add-AzureRmApplicationGatewayBackendHttpSettings Cmdlet 會將後端 HTTP 設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6f42f-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="6f42f-107">後端 HTTP 設定會套用至池中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="6f42f-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="6f42f-108">示例</span><span class="sxs-lookup"><span data-stu-id="6f42f-108">EXAMPLES</span></span>

### <span data-ttu-id="6f42f-109">範例1：將後端 HTTP 設定新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="6f42f-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="6f42f-110">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將後端 HTTP 設定新增到應用程式閘道，將埠設定為88，將 [通訊協定] 設為 [HTTP]，並為 [設定] Setting02 命名。</span><span class="sxs-lookup"><span data-stu-id="6f42f-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="6f42f-111">參數</span><span class="sxs-lookup"><span data-stu-id="6f42f-111">PARAMETERS</span></span>

### <span data-ttu-id="6f42f-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="6f42f-112">-AffinityCookieName</span></span>
<span data-ttu-id="6f42f-113">要用於關聯 cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="6f42f-113">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f42f-114">-ApplicationGateway</span></span>
<span data-ttu-id="6f42f-115">指定此 Cmdlet 新增設定的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="6f42f-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="6f42f-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="6f42f-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="6f42f-117">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="6f42f-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="6f42f-118">-ConnectionDraining</span></span>
<span data-ttu-id="6f42f-119">後端 HTTP 設定資源的連接排出。</span><span class="sxs-lookup"><span data-stu-id="6f42f-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="6f42f-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="6f42f-121">指定是否應為後端伺服器池啟用或停用 cookie 關聯。</span><span class="sxs-lookup"><span data-stu-id="6f42f-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="6f42f-122">此參數可接受的值為： [已停用]、[已啟用]。</span><span class="sxs-lookup"><span data-stu-id="6f42f-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f42f-123">-DefaultProfile</span></span>
<span data-ttu-id="6f42f-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f42f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f42f-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="6f42f-125">-HostName</span></span>
<span data-ttu-id="6f42f-126">設定要傳送給後端伺服器的主機標頭。</span><span class="sxs-lookup"><span data-stu-id="6f42f-126">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f42f-127">-Name</span></span>
<span data-ttu-id="6f42f-128">指定此 Cmdlet 所新增之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f42f-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="6f42f-129">-Path</span><span class="sxs-lookup"><span data-stu-id="6f42f-129">-Path</span></span>
<span data-ttu-id="6f42f-130">應該用來做為所有 HTTP 要求的前置詞的路徑。</span><span class="sxs-lookup"><span data-stu-id="6f42f-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="6f42f-131">如果沒有為此參數提供任何值，就不會將任何路徑加上首碼。</span><span class="sxs-lookup"><span data-stu-id="6f42f-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="6f42f-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="6f42f-133">如果應該從後端伺服器的主機名稱中挑選主機標頭，請標示。</span><span class="sxs-lookup"><span data-stu-id="6f42f-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-134">-埠</span><span class="sxs-lookup"><span data-stu-id="6f42f-134">-Port</span></span>
<span data-ttu-id="6f42f-135">指定後端伺服器池的埠。</span><span class="sxs-lookup"><span data-stu-id="6f42f-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-136">探測器</span><span class="sxs-lookup"><span data-stu-id="6f42f-136">-Probe</span></span>
<span data-ttu-id="6f42f-137">指定要與後端伺服器建立關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="6f42f-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="6f42f-138">-ProbeId</span></span>
<span data-ttu-id="6f42f-139">指定要與後端伺服器關聯的探測識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f42f-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-140">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="6f42f-140">-Protocol</span></span>
<span data-ttu-id="6f42f-141">指定應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6f42f-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="6f42f-142">此參數可接受的值為： Http 和 Https。</span><span class="sxs-lookup"><span data-stu-id="6f42f-142">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="6f42f-143">-RequestTimeout</span></span>
<span data-ttu-id="6f42f-144">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="6f42f-144">Specifies the request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6f42f-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="6f42f-146">應用程式閘道信任的根憑證</span><span class="sxs-lookup"><span data-stu-id="6f42f-146">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f42f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f42f-147">CommonParameters</span></span>
<span data-ttu-id="6f42f-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f42f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f42f-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f42f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f42f-150">輸入</span><span class="sxs-lookup"><span data-stu-id="6f42f-150">INPUTS</span></span>

### <span data-ttu-id="6f42f-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6f42f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="6f42f-152">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6f42f-152">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="6f42f-153">輸出</span><span class="sxs-lookup"><span data-stu-id="6f42f-153">OUTPUTS</span></span>

### <span data-ttu-id="6f42f-154">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6f42f-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f42f-155">筆記</span><span class="sxs-lookup"><span data-stu-id="6f42f-155">NOTES</span></span>

## <span data-ttu-id="6f42f-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f42f-156">RELATED LINKS</span></span>

[<span data-ttu-id="6f42f-157">AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6f42f-157">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="6f42f-158">新-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6f42f-158">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="6f42f-159">移除-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6f42f-159">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="6f42f-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6f42f-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

