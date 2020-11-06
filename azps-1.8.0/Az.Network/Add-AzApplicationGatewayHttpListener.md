---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622191"
---
# <span data-ttu-id="b6f06-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6f06-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b6f06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6f06-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f06-103">將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b6f06-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b6f06-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6f06-104">SYNTAX</span></span>

### <span data-ttu-id="b6f06-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6f06-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6f06-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b6f06-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6f06-107">說明</span><span class="sxs-lookup"><span data-stu-id="b6f06-107">DESCRIPTION</span></span>
<span data-ttu-id="b6f06-108">**AzApplicationGatewayHttpListener** Cmdlet 會將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b6f06-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b6f06-109">示例</span><span class="sxs-lookup"><span data-stu-id="b6f06-109">EXAMPLES</span></span>

### <span data-ttu-id="b6f06-110">範例1：新增 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="b6f06-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="b6f06-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將 HTTP 監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b6f06-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="b6f06-112">範例2：新增具有 SSL 的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="b6f06-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="b6f06-113">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="b6f06-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b6f06-114">第二個命令會將使用 HTTPS 通訊協定的監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b6f06-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="b6f06-115">參數</span><span class="sxs-lookup"><span data-stu-id="b6f06-115">PARAMETERS</span></span>

### <span data-ttu-id="b6f06-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6f06-116">-ApplicationGateway</span></span>
<span data-ttu-id="b6f06-117">指定此 Cmdlet 新增 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b6f06-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="b6f06-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f06-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b6f06-119">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="b6f06-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="b6f06-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f06-120">-DefaultProfile</span></span>
<span data-ttu-id="b6f06-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6f06-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6f06-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f06-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b6f06-123">指定應用程式閘道前端 IP 資源物件。</span><span class="sxs-lookup"><span data-stu-id="b6f06-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="b6f06-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b6f06-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b6f06-125">指定應用程式閘道前端 IP ID。</span><span class="sxs-lookup"><span data-stu-id="b6f06-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="b6f06-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b6f06-126">-FrontendPort</span></span>
<span data-ttu-id="b6f06-127">指定應用程式閘道的 [前端埠] 物件。</span><span class="sxs-lookup"><span data-stu-id="b6f06-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="b6f06-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b6f06-128">-FrontendPortId</span></span>
<span data-ttu-id="b6f06-129">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="b6f06-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="b6f06-130">-HostName</span><span class="sxs-lookup"><span data-stu-id="b6f06-130">-HostName</span></span>
<span data-ttu-id="b6f06-131">指定此 Cmdlet 新增 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="b6f06-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="b6f06-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6f06-132">-Name</span></span>
<span data-ttu-id="b6f06-133">指定此命令所新增之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6f06-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="b6f06-134">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b6f06-134">-Protocol</span></span>
<span data-ttu-id="b6f06-135">指定 HTTP 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b6f06-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="b6f06-136">支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="b6f06-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="b6f06-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b6f06-137">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f06-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6f06-138">-SslCertificate</span></span>
<span data-ttu-id="b6f06-139">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="b6f06-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="b6f06-140">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="b6f06-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="b6f06-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b6f06-141">-SslCertificateId</span></span>
<span data-ttu-id="b6f06-142">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="b6f06-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="b6f06-143">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="b6f06-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="b6f06-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f06-144">CommonParameters</span></span>
<span data-ttu-id="b6f06-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6f06-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f06-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6f06-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f06-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b6f06-147">INPUTS</span></span>

### <span data-ttu-id="b6f06-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b6f06-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6f06-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b6f06-149">OUTPUTS</span></span>

### <span data-ttu-id="b6f06-150">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b6f06-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6f06-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b6f06-151">NOTES</span></span>

## <span data-ttu-id="b6f06-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6f06-152">RELATED LINKS</span></span>

[<span data-ttu-id="b6f06-153">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6f06-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6f06-154">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6f06-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6f06-155">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6f06-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6f06-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6f06-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


