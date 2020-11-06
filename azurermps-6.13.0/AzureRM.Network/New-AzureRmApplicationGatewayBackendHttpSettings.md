---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 3b292b70e96c8da57a87834ecc4c095c9ca3f55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447351"
---
# <span data-ttu-id="b9fc6-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9fc6-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b9fc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fc6-103">為應用程式閘道建立後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9fc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9fc6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fc6-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fc6-106">New-AzureRmApplicationGatewayBackendHttpSettings Cmdlet 會為應用程式閘道建立後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="b9fc6-107">後端 HTTP 設定會套用至池中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="b9fc6-108">示例</span><span class="sxs-lookup"><span data-stu-id="b9fc6-108">EXAMPLES</span></span>

### <span data-ttu-id="b9fc6-109">範例1：建立後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="b9fc6-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="b9fc6-110">這個命令會在埠80上使用 HTTP 通訊協定建立後端 HTTP 設定，並停用 cookie 關聯性。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="b9fc6-111">這些設定會儲存在 $Setting 變數中。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="b9fc6-112">參數</span><span class="sxs-lookup"><span data-stu-id="b9fc6-112">PARAMETERS</span></span>

### <span data-ttu-id="b9fc6-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="b9fc6-113">-AffinityCookieName</span></span>
<span data-ttu-id="b9fc6-114">要用於關聯 cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="b9fc6-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="b9fc6-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="b9fc6-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="b9fc6-116">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="b9fc6-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b9fc6-117">-ConnectionDraining</span></span>
<span data-ttu-id="b9fc6-118">後端 HTTP 設定資源的連接排出。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="b9fc6-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="b9fc6-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="b9fc6-120">指定是否應針對後端伺服器池啟用或停用 cookie 關聯。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="b9fc6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fc6-121">-DefaultProfile</span></span>
<span data-ttu-id="b9fc6-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9fc6-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="b9fc6-123">-HostName</span></span>
<span data-ttu-id="b9fc6-124">設定要傳送給後端伺服器的主機標頭。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="b9fc6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9fc6-125">-Name</span></span>
<span data-ttu-id="b9fc6-126">指定此 Cmdlet 所建立之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b9fc6-127">-Path</span><span class="sxs-lookup"><span data-stu-id="b9fc6-127">-Path</span></span>
<span data-ttu-id="b9fc6-128">應該用來做為所有 HTTP 要求的前置詞的路徑。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="b9fc6-129">如果沒有為此參數提供任何值，就不會將任何路徑加上首碼。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="b9fc6-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="b9fc6-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="b9fc6-131">如果應該從後端伺服器的主機名稱中挑選主機標頭，請標示。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="b9fc6-132">-埠</span><span class="sxs-lookup"><span data-stu-id="b9fc6-132">-Port</span></span>
<span data-ttu-id="b9fc6-133">指定後端伺服器池的埠。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="b9fc6-134">探測器</span><span class="sxs-lookup"><span data-stu-id="b9fc6-134">-Probe</span></span>
<span data-ttu-id="b9fc6-135">指定要與後端伺服器池關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="b9fc6-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="b9fc6-136">-ProbeId</span></span>
<span data-ttu-id="b9fc6-137">指定要與後端伺服器池關聯的探測識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="b9fc6-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b9fc6-138">-Protocol</span></span>
<span data-ttu-id="b9fc6-139">指定要用於應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="b9fc6-140">此參數可接受的值為： Http 和 Https。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="b9fc6-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="b9fc6-141">-RequestTimeout</span></span>
<span data-ttu-id="b9fc6-142">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="b9fc6-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fc6-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="b9fc6-144">應用程式閘道信任的根憑證</span><span class="sxs-lookup"><span data-stu-id="b9fc6-144">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="b9fc6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fc6-145">CommonParameters</span></span>
<span data-ttu-id="b9fc6-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fc6-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9fc6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fc6-148">輸入</span><span class="sxs-lookup"><span data-stu-id="b9fc6-148">INPUTS</span></span>

### <span data-ttu-id="b9fc6-149">所有</span><span class="sxs-lookup"><span data-stu-id="b9fc6-149">None</span></span>

## <span data-ttu-id="b9fc6-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b9fc6-150">OUTPUTS</span></span>

### <span data-ttu-id="b9fc6-151">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b9fc6-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b9fc6-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b9fc6-152">NOTES</span></span>

## <span data-ttu-id="b9fc6-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9fc6-153">RELATED LINKS</span></span>

[<span data-ttu-id="b9fc6-154">附加 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9fc6-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b9fc6-155">AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9fc6-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b9fc6-156">移除-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9fc6-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b9fc6-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b9fc6-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

