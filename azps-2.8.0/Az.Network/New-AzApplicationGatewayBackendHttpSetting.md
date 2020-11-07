---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 014309ceb54b1d16b2a55c97b03887deaf4ef281
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789982"
---
# <span data-ttu-id="55733-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="55733-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="55733-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55733-102">SYNOPSIS</span></span>
<span data-ttu-id="55733-103">為應用程式閘道建立後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="55733-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="55733-104">句法</span><span class="sxs-lookup"><span data-stu-id="55733-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55733-105">說明</span><span class="sxs-lookup"><span data-stu-id="55733-105">DESCRIPTION</span></span>
<span data-ttu-id="55733-106">New-AzApplicationGatewayBackendHttpSetting Cmdlet 會為應用程式閘道建立後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="55733-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="55733-107">後端 HTTP 設定會套用至池中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="55733-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="55733-108">示例</span><span class="sxs-lookup"><span data-stu-id="55733-108">EXAMPLES</span></span>

### <span data-ttu-id="55733-109">範例1：建立後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="55733-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="55733-110">這個命令會在埠80上使用 HTTP 通訊協定建立後端 HTTP 設定，並停用 cookie 關聯性。</span><span class="sxs-lookup"><span data-stu-id="55733-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="55733-111">這些設定會儲存在 $Setting 變數中。</span><span class="sxs-lookup"><span data-stu-id="55733-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="55733-112">參數</span><span class="sxs-lookup"><span data-stu-id="55733-112">PARAMETERS</span></span>

### <span data-ttu-id="55733-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="55733-113">-AffinityCookieName</span></span>
<span data-ttu-id="55733-114">要用於關聯 cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="55733-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="55733-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="55733-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="55733-116">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="55733-116">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55733-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="55733-117">-ConnectionDraining</span></span>
<span data-ttu-id="55733-118">後端 HTTP 設定資源的連接排出。</span><span class="sxs-lookup"><span data-stu-id="55733-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="55733-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="55733-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="55733-120">指定是否應針對後端伺服器池啟用或停用 cookie 關聯。</span><span class="sxs-lookup"><span data-stu-id="55733-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="55733-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55733-121">-DefaultProfile</span></span>
<span data-ttu-id="55733-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55733-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55733-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="55733-123">-HostName</span></span>
<span data-ttu-id="55733-124">設定要傳送給後端伺服器的主機標頭。</span><span class="sxs-lookup"><span data-stu-id="55733-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="55733-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="55733-125">-Name</span></span>
<span data-ttu-id="55733-126">指定此 Cmdlet 所建立之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="55733-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="55733-127">-Path</span><span class="sxs-lookup"><span data-stu-id="55733-127">-Path</span></span>
<span data-ttu-id="55733-128">應該用來做為所有 HTTP 要求的前置詞的路徑。</span><span class="sxs-lookup"><span data-stu-id="55733-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="55733-129">如果沒有為此參數提供任何值，就不會將任何路徑加上首碼。</span><span class="sxs-lookup"><span data-stu-id="55733-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="55733-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="55733-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="55733-131">如果應該從後端伺服器的主機名稱中挑選主機標頭，請標示。</span><span class="sxs-lookup"><span data-stu-id="55733-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="55733-132">-埠</span><span class="sxs-lookup"><span data-stu-id="55733-132">-Port</span></span>
<span data-ttu-id="55733-133">指定後端伺服器池的埠。</span><span class="sxs-lookup"><span data-stu-id="55733-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="55733-134">探測器</span><span class="sxs-lookup"><span data-stu-id="55733-134">-Probe</span></span>
<span data-ttu-id="55733-135">指定要與後端伺服器池關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="55733-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="55733-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="55733-136">-ProbeId</span></span>
<span data-ttu-id="55733-137">指定要與後端伺服器池關聯的探測識別碼。</span><span class="sxs-lookup"><span data-stu-id="55733-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="55733-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="55733-138">-Protocol</span></span>
<span data-ttu-id="55733-139">指定要用於應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="55733-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="55733-140">此參數可接受的值為： Http 和 Https。</span><span class="sxs-lookup"><span data-stu-id="55733-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="55733-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="55733-141">-RequestTimeout</span></span>
<span data-ttu-id="55733-142">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="55733-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="55733-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="55733-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="55733-144">應用程式閘道信任的根憑證</span><span class="sxs-lookup"><span data-stu-id="55733-144">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55733-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55733-145">CommonParameters</span></span>
<span data-ttu-id="55733-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55733-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55733-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55733-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55733-148">輸入</span><span class="sxs-lookup"><span data-stu-id="55733-148">INPUTS</span></span>

### <span data-ttu-id="55733-149">所有</span><span class="sxs-lookup"><span data-stu-id="55733-149">None</span></span>

## <span data-ttu-id="55733-150">輸出</span><span class="sxs-lookup"><span data-stu-id="55733-150">OUTPUTS</span></span>

### <span data-ttu-id="55733-151">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55733-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="55733-152">筆記</span><span class="sxs-lookup"><span data-stu-id="55733-152">NOTES</span></span>

## <span data-ttu-id="55733-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="55733-153">RELATED LINKS</span></span>

[<span data-ttu-id="55733-154">附加 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="55733-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="55733-155">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="55733-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="55733-156">移除-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="55733-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="55733-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="55733-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

