---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 325c4ca100bae93f88baaa9eb5c3fa6f2d3ecafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622197"
---
# <span data-ttu-id="d46c5-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d46c5-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="d46c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d46c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d46c5-103">將後端 HTTP 設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d46c5-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="d46c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d46c5-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d46c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d46c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d46c5-106">Add-AzApplicationGatewayBackendHttpSetting Cmdlet 會將後端 HTTP 設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d46c5-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="d46c5-107">後端 HTTP 設定會套用至池中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="d46c5-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="d46c5-108">示例</span><span class="sxs-lookup"><span data-stu-id="d46c5-108">EXAMPLES</span></span>

### <span data-ttu-id="d46c5-109">範例1：將後端 HTTP 設定新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="d46c5-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="d46c5-110">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將後端 HTTP 設定新增到應用程式閘道，將埠設定為88，將 [通訊協定] 設為 [HTTP]，並為 [設定] Setting02 命名。</span><span class="sxs-lookup"><span data-stu-id="d46c5-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="d46c5-111">參數</span><span class="sxs-lookup"><span data-stu-id="d46c5-111">PARAMETERS</span></span>

### <span data-ttu-id="d46c5-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="d46c5-112">-AffinityCookieName</span></span>
<span data-ttu-id="d46c5-113">要用於關聯 cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="d46c5-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="d46c5-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d46c5-114">-ApplicationGateway</span></span>
<span data-ttu-id="d46c5-115">指定此 Cmdlet 新增設定的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="d46c5-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="d46c5-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="d46c5-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="d46c5-117">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="d46c5-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="d46c5-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d46c5-118">-ConnectionDraining</span></span>
<span data-ttu-id="d46c5-119">後端 HTTP 設定資源的連接排出。</span><span class="sxs-lookup"><span data-stu-id="d46c5-119">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="d46c5-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="d46c5-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="d46c5-121">指定是否應為後端伺服器池啟用或停用 cookie 關聯。</span><span class="sxs-lookup"><span data-stu-id="d46c5-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="d46c5-122">此參數可接受的值為： [已停用]、[已啟用]。</span><span class="sxs-lookup"><span data-stu-id="d46c5-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

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

### <span data-ttu-id="d46c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46c5-123">-DefaultProfile</span></span>
<span data-ttu-id="d46c5-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d46c5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d46c5-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="d46c5-125">-HostName</span></span>
<span data-ttu-id="d46c5-126">設定要傳送給後端伺服器的主機標頭。</span><span class="sxs-lookup"><span data-stu-id="d46c5-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="d46c5-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="d46c5-127">-Name</span></span>
<span data-ttu-id="d46c5-128">指定此 Cmdlet 所新增之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="d46c5-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="d46c5-129">-Path</span><span class="sxs-lookup"><span data-stu-id="d46c5-129">-Path</span></span>
<span data-ttu-id="d46c5-130">應該用來做為所有 HTTP 要求的前置詞的路徑。</span><span class="sxs-lookup"><span data-stu-id="d46c5-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="d46c5-131">如果沒有為此參數提供任何值，就不會將任何路徑加上首碼。</span><span class="sxs-lookup"><span data-stu-id="d46c5-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="d46c5-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="d46c5-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="d46c5-133">如果應該從後端伺服器的主機名稱中挑選主機標頭，請標示。</span><span class="sxs-lookup"><span data-stu-id="d46c5-133">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="d46c5-134">-埠</span><span class="sxs-lookup"><span data-stu-id="d46c5-134">-Port</span></span>
<span data-ttu-id="d46c5-135">指定後端伺服器池的埠。</span><span class="sxs-lookup"><span data-stu-id="d46c5-135">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="d46c5-136">探測器</span><span class="sxs-lookup"><span data-stu-id="d46c5-136">-Probe</span></span>
<span data-ttu-id="d46c5-137">指定要與後端伺服器建立關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="d46c5-137">Specifies a probe to associate with a back-end server.</span></span>

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

### <span data-ttu-id="d46c5-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="d46c5-138">-ProbeId</span></span>
<span data-ttu-id="d46c5-139">指定要與後端伺服器關聯的探測識別碼。</span><span class="sxs-lookup"><span data-stu-id="d46c5-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="d46c5-140">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d46c5-140">-Protocol</span></span>
<span data-ttu-id="d46c5-141">指定應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d46c5-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="d46c5-142">此參數可接受的值為： Http 和 Https。</span><span class="sxs-lookup"><span data-stu-id="d46c5-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="d46c5-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="d46c5-143">-RequestTimeout</span></span>
<span data-ttu-id="d46c5-144">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="d46c5-144">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="d46c5-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d46c5-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="d46c5-146">應用程式閘道信任的根憑證</span><span class="sxs-lookup"><span data-stu-id="d46c5-146">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="d46c5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46c5-147">CommonParameters</span></span>
<span data-ttu-id="d46c5-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d46c5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46c5-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d46c5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46c5-150">輸入</span><span class="sxs-lookup"><span data-stu-id="d46c5-150">INPUTS</span></span>

### <span data-ttu-id="d46c5-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d46c5-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d46c5-152">輸出</span><span class="sxs-lookup"><span data-stu-id="d46c5-152">OUTPUTS</span></span>

### <span data-ttu-id="d46c5-153">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d46c5-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d46c5-154">筆記</span><span class="sxs-lookup"><span data-stu-id="d46c5-154">NOTES</span></span>

## <span data-ttu-id="d46c5-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="d46c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="d46c5-156">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d46c5-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="d46c5-157">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d46c5-157">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="d46c5-158">移除-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d46c5-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="d46c5-159">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d46c5-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

