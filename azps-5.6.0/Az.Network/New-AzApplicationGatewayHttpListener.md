---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913693"
---
# <span data-ttu-id="f970a-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f970a-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f970a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f970a-102">SYNOPSIS</span></span>
<span data-ttu-id="f970a-103">為應用程式閘道建立 HTTP 聆聽程式。</span><span class="sxs-lookup"><span data-stu-id="f970a-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="f970a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f970a-104">SYNTAX</span></span>

### <span data-ttu-id="f970a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f970a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f970a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f970a-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f970a-107">描述</span><span class="sxs-lookup"><span data-stu-id="f970a-107">DESCRIPTION</span></span>
<span data-ttu-id="f970a-108">**New-AzApplicationGatewayHttpListener** Cmdlet 會為 Azure 應用程式閘道建立 HTTP 聆聽程式。</span><span class="sxs-lookup"><span data-stu-id="f970a-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="f970a-109">例子</span><span class="sxs-lookup"><span data-stu-id="f970a-109">EXAMPLES</span></span>

### <span data-ttu-id="f970a-110">範例 1：建立 HTTP 聆聽者</span><span class="sxs-lookup"><span data-stu-id="f970a-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="f970a-111">此命令會建立名為 Listener01 的 HTTP 聆聽者，並儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f970a-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f970a-112">範例 2：使用 SSL 建立 HTTP 聆聽者</span><span class="sxs-lookup"><span data-stu-id="f970a-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="f970a-113">此命令會建立使用 SSL 卸載的 HTTP 聆聽程式，並提供 $SSLCert 01 變數中的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="f970a-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="f970a-114">該命令會儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f970a-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f970a-115">範例 3：使用防火牆-策略建立 HTTP 聆聽者</span><span class="sxs-lookup"><span data-stu-id="f970a-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="f970a-116">此命令會建立一個名為 Listener01，FirewallPolicy 的 HTTP 聆聽者做為$firewallPolicy，並儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f970a-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f970a-117">範例 4：使用 SSL 和 HostNames 新增 HTTPS 聆聽者</span><span class="sxs-lookup"><span data-stu-id="f970a-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="f970a-118">此命令會建立使用 SSL 卸載的 HTTP 聆聽程式，並提供 $SSLCert 01 變數中的 SSL 憑證以及兩個 HostName。</span><span class="sxs-lookup"><span data-stu-id="f970a-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="f970a-119">該命令會儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f970a-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="f970a-120">參數</span><span class="sxs-lookup"><span data-stu-id="f970a-120">PARAMETERS</span></span>

### <span data-ttu-id="f970a-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f970a-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="f970a-122">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="f970a-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f970a-123">-DefaultProfile</span></span>
<span data-ttu-id="f970a-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f970a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f970a-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f970a-125">-FirewallPolicy</span></span>
<span data-ttu-id="f970a-126">指定頂層防火牆政策的物件參照。</span><span class="sxs-lookup"><span data-stu-id="f970a-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="f970a-127">您可以使用 Cmdlet 建立New-AzApplicationGatewayWebApplicationFirewallPolicy參照。</span><span class="sxs-lookup"><span data-stu-id="f970a-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="f970a-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 使用上述命令建立防火牆原則，可以在路徑規則層級中參考。</span><span class="sxs-lookup"><span data-stu-id="f970a-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="f970a-129">上方命令會建立預設原則設定和受管理規則。</span><span class="sxs-lookup"><span data-stu-id="f970a-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="f970a-130">使用者可以指定 PolicySettings、ManagedRules，而不使用預設值，New-AzApplicationGatewayFirewallPolicySettings和New-AzApplicationGatewayFirewallPolicyManagedRules設定。</span><span class="sxs-lookup"><span data-stu-id="f970a-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f970a-131">-FirewallPolicyId</span></span>
<span data-ttu-id="f970a-132">指定現有頂層 Web 應用程式防火牆資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f970a-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="f970a-133">防火牆策略的 ID 可以使用 Get-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f970a-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="f970a-134">當我們有識別碼之後，您可以使用 *FirewallPolicyId* 參數，而不是 *FirewallPolicy* 參數。</span><span class="sxs-lookup"><span data-stu-id="f970a-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="f970a-135">例如：-FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="f970a-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="f970a-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f970a-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="f970a-137">指定 HTTP 聆聽者前端 IP 組組物件。</span><span class="sxs-lookup"><span data-stu-id="f970a-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f970a-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="f970a-139">指定 HTTP 聆聽者前端 IP 配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f970a-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="f970a-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f970a-140">-FrontendPort</span></span>
<span data-ttu-id="f970a-141">指定 HTTP 聆聽者前端埠。</span><span class="sxs-lookup"><span data-stu-id="f970a-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="f970a-142">-FrontendPortId</span></span>
<span data-ttu-id="f970a-143">指定 HTTP 聆聽者前端埠物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f970a-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="f970a-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="f970a-144">-HostName</span></span>
<span data-ttu-id="f970a-145">指定應用程式閘道 HTTP 聆聽者主機名稱。</span><span class="sxs-lookup"><span data-stu-id="f970a-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f970a-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="f970a-146">-HostNames</span></span>
<span data-ttu-id="f970a-147">主機名稱</span><span class="sxs-lookup"><span data-stu-id="f970a-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="f970a-148">-Name</span></span>
<span data-ttu-id="f970a-149">指定此 Cmdlet 所建立之 HTTP 聆聽者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f970a-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f970a-150">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f970a-150">-Protocol</span></span>
<span data-ttu-id="f970a-151">指定 HTTP 聆聽者使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f970a-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="f970a-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="f970a-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f970a-153">-SslCertificate</span></span>
<span data-ttu-id="f970a-154">指定 HTTP 聆聽者之 SSL 憑證物件。</span><span class="sxs-lookup"><span data-stu-id="f970a-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="f970a-155">-SslCertificateId</span></span>
<span data-ttu-id="f970a-156">指定 HTTP 聆聽者之 SSL 憑證的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f970a-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="f970a-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="f970a-157">-SslProfile</span></span>
<span data-ttu-id="f970a-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="f970a-158">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f970a-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="f970a-159">-SslProfileId</span></span>
<span data-ttu-id="f970a-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="f970a-160">SslProfileId</span></span>

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

### <span data-ttu-id="f970a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f970a-161">CommonParameters</span></span>
<span data-ttu-id="f970a-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f970a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f970a-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f970a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f970a-164">輸入</span><span class="sxs-lookup"><span data-stu-id="f970a-164">INPUTS</span></span>

### <span data-ttu-id="f970a-165">沒有</span><span class="sxs-lookup"><span data-stu-id="f970a-165">None</span></span>

## <span data-ttu-id="f970a-166">輸出</span><span class="sxs-lookup"><span data-stu-id="f970a-166">OUTPUTS</span></span>

### <span data-ttu-id="f970a-167">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f970a-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f970a-168">筆記</span><span class="sxs-lookup"><span data-stu-id="f970a-168">NOTES</span></span>

## <span data-ttu-id="f970a-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="f970a-169">RELATED LINKS</span></span>

[<span data-ttu-id="f970a-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f970a-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f970a-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f970a-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f970a-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f970a-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f970a-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f970a-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


