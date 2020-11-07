---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 4361d025026e3ff9c9a72a092a99a72b8b63c850
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794545"
---
# <span data-ttu-id="4987a-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4987a-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="4987a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4987a-102">SYNOPSIS</span></span>
<span data-ttu-id="4987a-103">將後端 HTTP 設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4987a-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="4987a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4987a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4987a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4987a-105">DESCRIPTION</span></span>
<span data-ttu-id="4987a-106">Add-AzApplicationGatewayBackendHttpSetting Cmdlet 會將後端 HTTP 設定新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4987a-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="4987a-107">後端 HTTP 設定會套用至池中的所有後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="4987a-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="4987a-108">示例</span><span class="sxs-lookup"><span data-stu-id="4987a-108">EXAMPLES</span></span>

### <span data-ttu-id="4987a-109">範例1：將後端 HTTP 設定新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="4987a-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="4987a-110">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將後端 HTTP 設定新增到應用程式閘道，將埠設定為88，將 [通訊協定] 設為 [HTTP]，並為 [設定] Setting02 命名。</span><span class="sxs-lookup"><span data-stu-id="4987a-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="4987a-111">參數</span><span class="sxs-lookup"><span data-stu-id="4987a-111">PARAMETERS</span></span>

### <span data-ttu-id="4987a-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="4987a-112">-AffinityCookieName</span></span>
<span data-ttu-id="4987a-113">要用於關聯 cookie 的 Cookie 名稱</span><span class="sxs-lookup"><span data-stu-id="4987a-113">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4987a-114">-ApplicationGateway</span></span>
<span data-ttu-id="4987a-115">指定此 Cmdlet 新增設定的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="4987a-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="4987a-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="4987a-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="4987a-117">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="4987a-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="4987a-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4987a-118">-ConnectionDraining</span></span>
<span data-ttu-id="4987a-119">後端 HTTP 設定資源的連接排出。</span><span class="sxs-lookup"><span data-stu-id="4987a-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="4987a-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="4987a-121">指定是否應為後端伺服器池啟用或停用 cookie 關聯。</span><span class="sxs-lookup"><span data-stu-id="4987a-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="4987a-122">此參數可接受的值為： [已停用]、[已啟用]。</span><span class="sxs-lookup"><span data-stu-id="4987a-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4987a-123">-DefaultProfile</span></span>
<span data-ttu-id="4987a-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4987a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4987a-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="4987a-125">-HostName</span></span>
<span data-ttu-id="4987a-126">設定要傳送給後端伺服器的主機標頭。</span><span class="sxs-lookup"><span data-stu-id="4987a-126">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4987a-127">-Name</span></span>
<span data-ttu-id="4987a-128">指定此 Cmdlet 所新增之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="4987a-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="4987a-129">-Path</span><span class="sxs-lookup"><span data-stu-id="4987a-129">-Path</span></span>
<span data-ttu-id="4987a-130">應該用來做為所有 HTTP 要求的前置詞的路徑。</span><span class="sxs-lookup"><span data-stu-id="4987a-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="4987a-131">如果沒有為此參數提供任何值，就不會將任何路徑加上首碼。</span><span class="sxs-lookup"><span data-stu-id="4987a-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="4987a-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="4987a-133">如果應該從後端伺服器的主機名稱中挑選主機標頭，請標示。</span><span class="sxs-lookup"><span data-stu-id="4987a-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-134">-埠</span><span class="sxs-lookup"><span data-stu-id="4987a-134">-Port</span></span>
<span data-ttu-id="4987a-135">指定後端伺服器池的埠。</span><span class="sxs-lookup"><span data-stu-id="4987a-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-136">探測器</span><span class="sxs-lookup"><span data-stu-id="4987a-136">-Probe</span></span>
<span data-ttu-id="4987a-137">指定要與後端伺服器建立關聯的探測器。</span><span class="sxs-lookup"><span data-stu-id="4987a-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="4987a-138">-ProbeEnabled</span></span>
<span data-ttu-id="4987a-139">如果應啟用探測器，則標示。</span><span class="sxs-lookup"><span data-stu-id="4987a-139">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-140">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="4987a-140">-ProbeId</span></span>
<span data-ttu-id="4987a-141">指定要與後端伺服器關聯的探測識別碼。</span><span class="sxs-lookup"><span data-stu-id="4987a-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-142">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4987a-142">-Protocol</span></span>
<span data-ttu-id="4987a-143">指定應用程式閘道與後端伺服器之間通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4987a-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="4987a-144">此參數可接受的值為： Http 和 Https。</span><span class="sxs-lookup"><span data-stu-id="4987a-144">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="4987a-145">-RequestTimeout</span></span>
<span data-ttu-id="4987a-146">指定要求超時值。</span><span class="sxs-lookup"><span data-stu-id="4987a-146">Specifies the request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4987a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4987a-147">CommonParameters</span></span>
<span data-ttu-id="4987a-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4987a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4987a-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4987a-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4987a-150">輸入</span><span class="sxs-lookup"><span data-stu-id="4987a-150">INPUTS</span></span>

### <span data-ttu-id="4987a-151">System.object</span><span class="sxs-lookup"><span data-stu-id="4987a-151">System.String</span></span>

## <span data-ttu-id="4987a-152">輸出</span><span class="sxs-lookup"><span data-stu-id="4987a-152">OUTPUTS</span></span>

### <span data-ttu-id="4987a-153">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4987a-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4987a-154">筆記</span><span class="sxs-lookup"><span data-stu-id="4987a-154">NOTES</span></span>

## <span data-ttu-id="4987a-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="4987a-155">RELATED LINKS</span></span>

[<span data-ttu-id="4987a-156">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4987a-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="4987a-157">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4987a-157">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="4987a-158">移除-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4987a-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="4987a-159">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4987a-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

