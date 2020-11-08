---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 840a1bef17fd736dbe3144f9fd8d382a78bcfd87
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141295"
---
# <span data-ttu-id="70aa6-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="70aa6-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="70aa6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="70aa6-103">為應用程式閘道建立後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="70aa6-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="70aa6-104">句法</span><span class="sxs-lookup"><span data-stu-id="70aa6-104">SYNTAX</span></span>

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

## <span data-ttu-id="70aa6-105">說明</span><span class="sxs-lookup"><span data-stu-id="70aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="70aa6-106">New-AzApplicationGatewayBackendHttpSetting Cmdlet 會為應用程式閘道建立後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="70aa6-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="70aa6-107">後端 HTTP 設定會套用至池中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="70aa6-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="70aa6-108">示例</span><span class="sxs-lookup"><span data-stu-id="70aa6-108">EXAMPLES</span></span>

### <span data-ttu-id="70aa6-109">範例1：建立後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="70aa6-109">Example 1: Create back-end HTTP settings</span></span>
```powershell
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="70aa6-110">這個命令會在埠80上使用 HTTP 通訊協定建立後端 HTTP 設定，並停用 cookie 關聯性。</span><span class="sxs-lookup"><span data-stu-id="70aa6-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="70aa6-111">這些設定會儲存在 $Setting 變數中。</span><span class="sxs-lookup"><span data-stu-id="70aa6-111">The settings are stored in the $Setting variable.</span></span>

### <span data-ttu-id="70aa6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="70aa6-112">Example 2</span></span>

<span data-ttu-id="70aa6-113">為應用程式閘道建立後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="70aa6-113">Creates back-end HTTP setting for an application gateway.</span></span> <span data-ttu-id="70aa6-114"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="70aa6-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzApplicationGatewayBackendHttpSetting -CookieBasedAffinity Enabled -Name 'Setting01' -PickHostNameFromBackendAddress -Port 80 -Probe <PSApplicationGatewayProbe> -Protocol http -RequestTimeout <Int32>
```

## <span data-ttu-id="70aa6-115">參數</span><span class="sxs-lookup"><span data-stu-id="70aa6-115">PARAMETERS</span></span>

### <span data-ttu-id="70aa6-116">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="70aa6-116">-AffinityCookieName</span></span>
<span data-ttu-id="70aa6-117">要用於關聯 cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="70aa6-117">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="70aa6-118">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="70aa6-118">-AuthenticationCertificates</span></span>
<span data-ttu-id="70aa6-119">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="70aa6-119">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="70aa6-120">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="70aa6-120">-ConnectionDraining</span></span>
<span data-ttu-id="70aa6-121">後端 HTTP 設定資源的連接排出。</span><span class="sxs-lookup"><span data-stu-id="70aa6-121">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="70aa6-122">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="70aa6-122">-CookieBasedAffinity</span></span>
<span data-ttu-id="70aa6-123">指定是否應針對後端伺服器池啟用或停用 cookie 關聯。</span><span class="sxs-lookup"><span data-stu-id="70aa6-123">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="70aa6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70aa6-124">-DefaultProfile</span></span>
<span data-ttu-id="70aa6-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70aa6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70aa6-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="70aa6-126">-HostName</span></span>
<span data-ttu-id="70aa6-127">設定要傳送給後端伺服器的主機標頭。</span><span class="sxs-lookup"><span data-stu-id="70aa6-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="70aa6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="70aa6-128">-Name</span></span>
<span data-ttu-id="70aa6-129">指定此 Cmdlet 所建立之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="70aa6-129">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="70aa6-130">-Path</span><span class="sxs-lookup"><span data-stu-id="70aa6-130">-Path</span></span>
<span data-ttu-id="70aa6-131">應該用來做為所有 HTTP 要求的前置詞的路徑。</span><span class="sxs-lookup"><span data-stu-id="70aa6-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="70aa6-132">如果沒有為此參數提供任何值，就不會將任何路徑加上首碼。</span><span class="sxs-lookup"><span data-stu-id="70aa6-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="70aa6-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="70aa6-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="70aa6-134">如果應該從後端伺服器的主機名稱中挑選主機標頭，請標示。</span><span class="sxs-lookup"><span data-stu-id="70aa6-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="70aa6-135">-埠</span><span class="sxs-lookup"><span data-stu-id="70aa6-135">-Port</span></span>
<span data-ttu-id="70aa6-136">指定後端伺服器池的埠。</span><span class="sxs-lookup"><span data-stu-id="70aa6-136">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="70aa6-137">探測器</span><span class="sxs-lookup"><span data-stu-id="70aa6-137">-Probe</span></span>
<span data-ttu-id="70aa6-138">指定要與後端伺服器池關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="70aa6-138">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="70aa6-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="70aa6-139">-ProbeId</span></span>
<span data-ttu-id="70aa6-140">指定要與後端伺服器池關聯的探測識別碼。</span><span class="sxs-lookup"><span data-stu-id="70aa6-140">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="70aa6-141">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="70aa6-141">-Protocol</span></span>
<span data-ttu-id="70aa6-142">指定要用於應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="70aa6-142">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="70aa6-143">此參數可接受的值為： Http 和 Https。</span><span class="sxs-lookup"><span data-stu-id="70aa6-143">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="70aa6-144">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="70aa6-144">-RequestTimeout</span></span>
<span data-ttu-id="70aa6-145">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="70aa6-145">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="70aa6-146">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="70aa6-146">-TrustedRootCertificate</span></span>
<span data-ttu-id="70aa6-147">應用程式閘道信任的根憑證</span><span class="sxs-lookup"><span data-stu-id="70aa6-147">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="70aa6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70aa6-148">CommonParameters</span></span>
<span data-ttu-id="70aa6-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70aa6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70aa6-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70aa6-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70aa6-151">輸入</span><span class="sxs-lookup"><span data-stu-id="70aa6-151">INPUTS</span></span>

### <span data-ttu-id="70aa6-152">所有</span><span class="sxs-lookup"><span data-stu-id="70aa6-152">None</span></span>

## <span data-ttu-id="70aa6-153">輸出</span><span class="sxs-lookup"><span data-stu-id="70aa6-153">OUTPUTS</span></span>

### <span data-ttu-id="70aa6-154">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70aa6-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="70aa6-155">筆記</span><span class="sxs-lookup"><span data-stu-id="70aa6-155">NOTES</span></span>

## <span data-ttu-id="70aa6-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="70aa6-156">RELATED LINKS</span></span>

[<span data-ttu-id="70aa6-157">附加 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="70aa6-157">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="70aa6-158">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="70aa6-158">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="70aa6-159">移除-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="70aa6-159">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="70aa6-160">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="70aa6-160">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)
