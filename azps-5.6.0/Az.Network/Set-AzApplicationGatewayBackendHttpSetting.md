---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: d784d3de33f535690e631c4deb21208b76f58078
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912629"
---
# <span data-ttu-id="f7213-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f7213-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="f7213-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7213-102">SYNOPSIS</span></span>
<span data-ttu-id="f7213-103">更新應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="f7213-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="f7213-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7213-104">SYNTAX</span></span>

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

## <span data-ttu-id="f7213-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7213-105">DESCRIPTION</span></span>
<span data-ttu-id="f7213-106">此Set-AzApplicationGatewayBackendHttpSetting Cmdlet 會更新 Azure 應用程式閘道的後端超文字傳輸通訊 (HTTP) 設定。</span><span class="sxs-lookup"><span data-stu-id="f7213-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="f7213-107">後端 HTTP 設定會適用于集中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7213-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="f7213-108">例子</span><span class="sxs-lookup"><span data-stu-id="f7213-108">EXAMPLES</span></span>

### <span data-ttu-id="f7213-109">範例 1：更新應用程式閘道的後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="f7213-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="f7213-110">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="f7213-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f7213-111">第二個命令會更新應用程式閘道在 $AppGw 變數中的 HTTP 設定，以使用埠 88，即 HTTP 通訊協定，並啟用 Cookie 型關聯。</span><span class="sxs-lookup"><span data-stu-id="f7213-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="f7213-112">參數</span><span class="sxs-lookup"><span data-stu-id="f7213-112">PARAMETERS</span></span>

### <span data-ttu-id="f7213-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="f7213-113">-AffinityCookieName</span></span>
<span data-ttu-id="f7213-114">用於關聯 Cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="f7213-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="f7213-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7213-115">-ApplicationGateway</span></span>
<span data-ttu-id="f7213-116">指定此 Cmdlet 與後端 HTTP 設定建立關聯的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="f7213-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f7213-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="f7213-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="f7213-118">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="f7213-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="f7213-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f7213-119">-ConnectionDraining</span></span>
<span data-ttu-id="f7213-120">後端 HTTP 設定資源的連接耗用。</span><span class="sxs-lookup"><span data-stu-id="f7213-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="f7213-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="f7213-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="f7213-122">指定後端伺服器資料庫是否應該啟用或停用 Cookie 型關聯。</span><span class="sxs-lookup"><span data-stu-id="f7213-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="f7213-123">此參數可接受的值為：已停用或已啟用。</span><span class="sxs-lookup"><span data-stu-id="f7213-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="f7213-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7213-124">-DefaultProfile</span></span>
<span data-ttu-id="f7213-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7213-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7213-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="f7213-126">-HostName</span></span>
<span data-ttu-id="f7213-127">設定要送到後端伺服器的主機標題。</span><span class="sxs-lookup"><span data-stu-id="f7213-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="f7213-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7213-128">-Name</span></span>
<span data-ttu-id="f7213-129">指定後端 HTTP 設定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7213-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="f7213-130">-路徑</span><span class="sxs-lookup"><span data-stu-id="f7213-130">-Path</span></span>
<span data-ttu-id="f7213-131">應做為所有 HTTP 要求首碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="f7213-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="f7213-132">如果未為此參數提供值，則任何路徑都會以首碼為首碼。</span><span class="sxs-lookup"><span data-stu-id="f7213-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="f7213-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="f7213-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="f7213-134">如果主機名稱應該從後端伺服器的主機名稱挑選，則標上標出。</span><span class="sxs-lookup"><span data-stu-id="f7213-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="f7213-135">-埠</span><span class="sxs-lookup"><span data-stu-id="f7213-135">-Port</span></span>
<span data-ttu-id="f7213-136">指定後端伺服器資料庫內每個伺服器使用的埠。</span><span class="sxs-lookup"><span data-stu-id="f7213-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="f7213-137">-進位</span><span class="sxs-lookup"><span data-stu-id="f7213-137">-Probe</span></span>
<span data-ttu-id="f7213-138">指定要與後端 HTTP 設定關聯的新設定。</span><span class="sxs-lookup"><span data-stu-id="f7213-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f7213-139">-一維Id</span><span class="sxs-lookup"><span data-stu-id="f7213-139">-ProbeId</span></span>
<span data-ttu-id="f7213-140">指定與後端 HTTP 設定關聯的探索識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7213-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f7213-141">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f7213-141">-Protocol</span></span>
<span data-ttu-id="f7213-142">指定應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f7213-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="f7213-143">此參數可接受的值為：HTTP 和 Https。</span><span class="sxs-lookup"><span data-stu-id="f7213-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="f7213-144">此參數會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f7213-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="f7213-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="f7213-145">-RequestTimeout</span></span>
<span data-ttu-id="f7213-146">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="f7213-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="f7213-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f7213-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="f7213-148">應用程式閘道信任的根憑證</span><span class="sxs-lookup"><span data-stu-id="f7213-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="f7213-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7213-149">CommonParameters</span></span>
<span data-ttu-id="f7213-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7213-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7213-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f7213-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7213-152">輸入</span><span class="sxs-lookup"><span data-stu-id="f7213-152">INPUTS</span></span>

### <span data-ttu-id="f7213-153">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7213-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7213-154">輸出</span><span class="sxs-lookup"><span data-stu-id="f7213-154">OUTPUTS</span></span>

### <span data-ttu-id="f7213-155">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7213-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7213-156">筆記</span><span class="sxs-lookup"><span data-stu-id="f7213-156">NOTES</span></span>

## <span data-ttu-id="f7213-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7213-157">RELATED LINKS</span></span>

[<span data-ttu-id="f7213-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f7213-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f7213-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f7213-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f7213-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f7213-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f7213-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f7213-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

