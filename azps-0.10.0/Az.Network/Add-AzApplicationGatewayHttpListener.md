---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: eaae79c09f6ee609d7a7bf645c2312007a78ad59
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794537"
---
# <span data-ttu-id="4f8bf-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f8bf-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4f8bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8bf-103">將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="4f8bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f8bf-104">SYNTAX</span></span>

### <span data-ttu-id="4f8bf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f8bf-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f8bf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4f8bf-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f8bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="4f8bf-107">DESCRIPTION</span></span>
<span data-ttu-id="4f8bf-108">**AzApplicationGatewayHttpListener** Cmdlet 會將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="4f8bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f8bf-109">EXAMPLES</span></span>

### <span data-ttu-id="4f8bf-110">範例1：新增 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="4f8bf-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="4f8bf-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將 HTTP 監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="4f8bf-112">範例2：新增具有 SSL 的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="4f8bf-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="4f8bf-113">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4f8bf-114">第二個命令會將使用 HTTPS 通訊協定的監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="4f8bf-115">參數</span><span class="sxs-lookup"><span data-stu-id="4f8bf-115">PARAMETERS</span></span>

### <span data-ttu-id="4f8bf-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f8bf-116">-ApplicationGateway</span></span>
<span data-ttu-id="4f8bf-117">指定此 Cmdlet 新增 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="4f8bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8bf-118">-DefaultProfile</span></span>
<span data-ttu-id="4f8bf-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f8bf-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f8bf-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="4f8bf-121">指定應用程式閘道前端 IP 資源物件。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-121">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8bf-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4f8bf-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="4f8bf-123">指定應用程式閘道前端 IP ID。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-123">Specifies the application gateway front-end IP ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8bf-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f8bf-124">-FrontendPort</span></span>
<span data-ttu-id="4f8bf-125">指定應用程式閘道的 [前端埠] 物件。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-125">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8bf-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="4f8bf-126">-FrontendPortId</span></span>
<span data-ttu-id="4f8bf-127">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-127">Specifies the application gateway front-end port ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8bf-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="4f8bf-128">-HostName</span></span>
<span data-ttu-id="4f8bf-129">指定此 Cmdlet 新增 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="4f8bf-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f8bf-130">-Name</span></span>
<span data-ttu-id="4f8bf-131">指定此命令所新增之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="4f8bf-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4f8bf-132">-Protocol</span></span>
<span data-ttu-id="4f8bf-133">指定 HTTP 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="4f8bf-134">支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="4f8bf-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="4f8bf-135">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8bf-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="4f8bf-136">-SslCertificate</span></span>
<span data-ttu-id="4f8bf-137">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="4f8bf-138">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8bf-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="4f8bf-139">-SslCertificateId</span></span>
<span data-ttu-id="4f8bf-140">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="4f8bf-141">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8bf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8bf-142">CommonParameters</span></span>
<span data-ttu-id="4f8bf-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8bf-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f8bf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8bf-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4f8bf-145">INPUTS</span></span>

### <span data-ttu-id="4f8bf-146">System.object</span><span class="sxs-lookup"><span data-stu-id="4f8bf-146">System.String</span></span>

## <span data-ttu-id="4f8bf-147">輸出</span><span class="sxs-lookup"><span data-stu-id="4f8bf-147">OUTPUTS</span></span>

### <span data-ttu-id="4f8bf-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4f8bf-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4f8bf-149">筆記</span><span class="sxs-lookup"><span data-stu-id="4f8bf-149">NOTES</span></span>

## <span data-ttu-id="4f8bf-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f8bf-150">RELATED LINKS</span></span>

[<span data-ttu-id="4f8bf-151">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f8bf-151">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f8bf-152">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f8bf-152">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f8bf-153">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f8bf-153">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4f8bf-154">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f8bf-154">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


