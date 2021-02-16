---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142114"
---
# <span data-ttu-id="4caac-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4caac-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="4caac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4caac-102">SYNOPSIS</span></span>
<span data-ttu-id="4caac-103">更新應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="4caac-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="4caac-104">句法</span><span class="sxs-lookup"><span data-stu-id="4caac-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4caac-105">說明</span><span class="sxs-lookup"><span data-stu-id="4caac-105">DESCRIPTION</span></span>
<span data-ttu-id="4caac-106">Set-AzApplicationGatewayBackendHttpSetting Cmdlet 會更新 Azure 應用程式閘道 (HTTP) 設定的後端超文字傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4caac-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="4caac-107">後端 HTTP 設定會套用至池中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="4caac-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="4caac-108">示例</span><span class="sxs-lookup"><span data-stu-id="4caac-108">EXAMPLES</span></span>

### <span data-ttu-id="4caac-109">範例1：更新應用程式閘道的後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="4caac-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="4caac-110">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4caac-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4caac-111">第二個命令會更新 $AppGw 變數中應用程式閘道的 HTTP 設定，以使用埠88（HTTP 通訊協定），並啟用以 cookie 為基礎的關聯。</span><span class="sxs-lookup"><span data-stu-id="4caac-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="4caac-112">參數</span><span class="sxs-lookup"><span data-stu-id="4caac-112">PARAMETERS</span></span>

### <span data-ttu-id="4caac-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="4caac-113">-AffinityCookieName</span></span>
<span data-ttu-id="4caac-114">要用於關聯 cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="4caac-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="4caac-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4caac-115">-ApplicationGateway</span></span>
<span data-ttu-id="4caac-116">指定此 Cmdlet 關聯後端 HTTP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4caac-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4caac-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="4caac-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="4caac-118">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="4caac-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="4caac-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4caac-119">-ConnectionDraining</span></span>
<span data-ttu-id="4caac-120">後端 HTTP 設定資源的連接排出。</span><span class="sxs-lookup"><span data-stu-id="4caac-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="4caac-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="4caac-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="4caac-122">指定是否應為後端伺服器池啟用或停用 cookie 關聯。</span><span class="sxs-lookup"><span data-stu-id="4caac-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="4caac-123">此參數可接受的值為： [已停用] 或 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="4caac-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="4caac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4caac-124">-DefaultProfile</span></span>
<span data-ttu-id="4caac-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4caac-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4caac-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="4caac-126">-HostName</span></span>
<span data-ttu-id="4caac-127">設定要傳送給後端伺服器的主機標頭。</span><span class="sxs-lookup"><span data-stu-id="4caac-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="4caac-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="4caac-128">-Name</span></span>
<span data-ttu-id="4caac-129">指定後端 HTTP 設定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="4caac-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="4caac-130">-Path</span><span class="sxs-lookup"><span data-stu-id="4caac-130">-Path</span></span>
<span data-ttu-id="4caac-131">應該用來做為所有 HTTP 要求的前置詞的路徑。</span><span class="sxs-lookup"><span data-stu-id="4caac-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="4caac-132">如果沒有為此參數提供任何值，就不會將任何路徑加上首碼。</span><span class="sxs-lookup"><span data-stu-id="4caac-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="4caac-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="4caac-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="4caac-134">如果應該從後端伺服器的主機名稱中挑選主機標頭，請標示。</span><span class="sxs-lookup"><span data-stu-id="4caac-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="4caac-135">-埠</span><span class="sxs-lookup"><span data-stu-id="4caac-135">-Port</span></span>
<span data-ttu-id="4caac-136">指定要用於後端伺服器池中每個伺服器的埠。</span><span class="sxs-lookup"><span data-stu-id="4caac-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="4caac-137">探測器</span><span class="sxs-lookup"><span data-stu-id="4caac-137">-Probe</span></span>
<span data-ttu-id="4caac-138">指定與後端 HTTP 設定關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="4caac-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4caac-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="4caac-139">-ProbeId</span></span>
<span data-ttu-id="4caac-140">指定要與後端 HTTP 設定關聯的探針識別碼。</span><span class="sxs-lookup"><span data-stu-id="4caac-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4caac-141">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4caac-141">-Protocol</span></span>
<span data-ttu-id="4caac-142">指定要用於應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4caac-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="4caac-143">此參數可接受的值為： Http 和 Https。</span><span class="sxs-lookup"><span data-stu-id="4caac-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="4caac-144">這個參數會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4caac-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="4caac-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="4caac-145">-RequestTimeout</span></span>
<span data-ttu-id="4caac-146">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="4caac-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="4caac-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4caac-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="4caac-148">應用程式閘道信任的根憑證</span><span class="sxs-lookup"><span data-stu-id="4caac-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="4caac-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4caac-149">CommonParameters</span></span>
<span data-ttu-id="4caac-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4caac-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4caac-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4caac-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4caac-152">輸入</span><span class="sxs-lookup"><span data-stu-id="4caac-152">INPUTS</span></span>

### <span data-ttu-id="4caac-153">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4caac-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4caac-154">輸出</span><span class="sxs-lookup"><span data-stu-id="4caac-154">OUTPUTS</span></span>

### <span data-ttu-id="4caac-155">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4caac-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4caac-156">筆記</span><span class="sxs-lookup"><span data-stu-id="4caac-156">NOTES</span></span>

## <span data-ttu-id="4caac-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="4caac-157">RELATED LINKS</span></span>

[<span data-ttu-id="4caac-158">附加 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4caac-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4caac-159">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4caac-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4caac-160">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4caac-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4caac-161">移除-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4caac-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

