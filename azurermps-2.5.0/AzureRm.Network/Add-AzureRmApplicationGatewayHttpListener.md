---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: bda8ce00d316d57522bb307518c535c591e7b602
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802465"
---
# <span data-ttu-id="90600-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="90600-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="90600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90600-102">SYNOPSIS</span></span>
<span data-ttu-id="90600-103">將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="90600-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90600-104">句法</span><span class="sxs-lookup"><span data-stu-id="90600-104">SYNTAX</span></span>

### <span data-ttu-id="90600-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="90600-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90600-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="90600-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90600-107">說明</span><span class="sxs-lookup"><span data-stu-id="90600-107">DESCRIPTION</span></span>
<span data-ttu-id="90600-108">**AzureRmApplicationGatewayHttpListener** Cmdlet 會將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="90600-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="90600-109">示例</span><span class="sxs-lookup"><span data-stu-id="90600-109">EXAMPLES</span></span>

### <span data-ttu-id="90600-110">範例1：新增 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="90600-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="90600-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將 HTTP 監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="90600-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="90600-112">範例2：新增具有 SSL 的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="90600-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="90600-113">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="90600-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="90600-114">第二個命令會將使用 HTTPS 通訊協定的監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="90600-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="90600-115">參數</span><span class="sxs-lookup"><span data-stu-id="90600-115">PARAMETERS</span></span>

### <span data-ttu-id="90600-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90600-116">-ApplicationGateway</span></span>
<span data-ttu-id="90600-117">指定此 Cmdlet 新增 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="90600-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="90600-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90600-118">-DefaultProfile</span></span>
<span data-ttu-id="90600-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90600-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90600-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="90600-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="90600-121">指定應用程式閘道前端 IP 資源物件。</span><span class="sxs-lookup"><span data-stu-id="90600-121">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="90600-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="90600-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="90600-123">指定應用程式閘道前端 IP ID。</span><span class="sxs-lookup"><span data-stu-id="90600-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="90600-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="90600-124">-FrontendPort</span></span>
<span data-ttu-id="90600-125">指定應用程式閘道的 [前端埠] 物件。</span><span class="sxs-lookup"><span data-stu-id="90600-125">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="90600-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="90600-126">-FrontendPortId</span></span>
<span data-ttu-id="90600-127">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="90600-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="90600-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="90600-128">-HostName</span></span>
<span data-ttu-id="90600-129">指定此 Cmdlet 新增 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="90600-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="90600-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="90600-130">-Name</span></span>
<span data-ttu-id="90600-131">指定此命令所新增之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="90600-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="90600-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="90600-132">-Protocol</span></span>
<span data-ttu-id="90600-133">指定 HTTP 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="90600-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="90600-134">支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="90600-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="90600-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="90600-135">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="90600-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="90600-136">-SslCertificate</span></span>
<span data-ttu-id="90600-137">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="90600-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="90600-138">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="90600-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="90600-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="90600-139">-SslCertificateId</span></span>
<span data-ttu-id="90600-140">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="90600-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="90600-141">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="90600-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="90600-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90600-142">CommonParameters</span></span>
<span data-ttu-id="90600-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90600-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90600-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90600-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90600-145">輸入</span><span class="sxs-lookup"><span data-stu-id="90600-145">INPUTS</span></span>

### <span data-ttu-id="90600-146">System.object</span><span class="sxs-lookup"><span data-stu-id="90600-146">System.String</span></span>

## <span data-ttu-id="90600-147">輸出</span><span class="sxs-lookup"><span data-stu-id="90600-147">OUTPUTS</span></span>

### <span data-ttu-id="90600-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="90600-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90600-149">筆記</span><span class="sxs-lookup"><span data-stu-id="90600-149">NOTES</span></span>

## <span data-ttu-id="90600-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="90600-150">RELATED LINKS</span></span>

[<span data-ttu-id="90600-151">AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="90600-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="90600-152">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="90600-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="90600-153">移除-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="90600-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="90600-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="90600-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


