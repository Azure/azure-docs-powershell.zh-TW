---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790546"
---
# <span data-ttu-id="9d3ba-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d3ba-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9d3ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9d3ba-103">修改應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="9d3ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d3ba-104">SYNTAX</span></span>

### <span data-ttu-id="9d3ba-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d3ba-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d3ba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d3ba-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d3ba-107">說明</span><span class="sxs-lookup"><span data-stu-id="9d3ba-107">DESCRIPTION</span></span>
<span data-ttu-id="9d3ba-108">**AzApplicationGatewayHttpListener** Cmdlet 會修改 Azure 應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="9d3ba-109">示例</span><span class="sxs-lookup"><span data-stu-id="9d3ba-109">EXAMPLES</span></span>

### <span data-ttu-id="9d3ba-110">範例1：設定 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="9d3ba-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="9d3ba-111">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9d3ba-112">第二個命令會將閘道的 HTTP 偵聽程式設定為使用以埠80上的 HTTP 通訊協定儲存在 $FIP 01 中的前端配置。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="9d3ba-113">參數</span><span class="sxs-lookup"><span data-stu-id="9d3ba-113">PARAMETERS</span></span>

### <span data-ttu-id="9d3ba-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d3ba-114">-ApplicationGateway</span></span>
<span data-ttu-id="9d3ba-115">指定此 Cmdlet 與 HTTP 偵聽程式關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="9d3ba-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d3ba-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="9d3ba-117">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="9d3ba-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="9d3ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d3ba-118">-DefaultProfile</span></span>
<span data-ttu-id="9d3ba-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d3ba-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d3ba-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="9d3ba-121">指定應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9d3ba-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9d3ba-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="9d3ba-123">指定應用程式閘道的前端 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9d3ba-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9d3ba-124">-FrontendPort</span></span>
<span data-ttu-id="9d3ba-125">指定應用程式閘道前端埠。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="9d3ba-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="9d3ba-126">-FrontendPortId</span></span>
<span data-ttu-id="9d3ba-127">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="9d3ba-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="9d3ba-128">-HostName</span></span>
<span data-ttu-id="9d3ba-129">指定此 Cmdlet 傳送 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="9d3ba-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d3ba-130">-Name</span></span>
<span data-ttu-id="9d3ba-131">指定 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="9d3ba-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9d3ba-132">-Protocol</span></span>
<span data-ttu-id="9d3ba-133">指定 HTTP 偵聽程式使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="9d3ba-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9d3ba-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d3ba-135">Http</span><span class="sxs-lookup"><span data-stu-id="9d3ba-135">Http</span></span>
- <span data-ttu-id="9d3ba-136">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="9d3ba-136">Https</span></span>

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

### <span data-ttu-id="9d3ba-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="9d3ba-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="9d3ba-138">指定 Cmdlet 是否需要伺服器名稱指示。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="9d3ba-139">此參數可接受的值為： true 或 false。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="9d3ba-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9d3ba-140">-SslCertificate</span></span>
<span data-ttu-id="9d3ba-141">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="9d3ba-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="9d3ba-142">-SslCertificateId</span></span>
<span data-ttu-id="9d3ba-143">指定 (SSL) HTTP 偵聽程式的憑證 ID 的安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="9d3ba-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d3ba-144">CommonParameters</span></span>
<span data-ttu-id="9d3ba-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d3ba-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d3ba-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d3ba-147">輸入</span><span class="sxs-lookup"><span data-stu-id="9d3ba-147">INPUTS</span></span>

### <span data-ttu-id="9d3ba-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d3ba-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d3ba-149">輸出</span><span class="sxs-lookup"><span data-stu-id="9d3ba-149">OUTPUTS</span></span>

### <span data-ttu-id="9d3ba-150">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d3ba-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d3ba-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9d3ba-151">NOTES</span></span>

## <span data-ttu-id="9d3ba-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d3ba-152">RELATED LINKS</span></span>

[<span data-ttu-id="9d3ba-153">附加 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d3ba-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9d3ba-154">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d3ba-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9d3ba-155">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d3ba-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9d3ba-156">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d3ba-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


