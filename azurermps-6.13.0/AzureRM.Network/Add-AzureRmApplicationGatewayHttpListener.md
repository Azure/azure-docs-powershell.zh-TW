---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 571739c72b42e07070a3882ef696388a4a923196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455231"
---
# <span data-ttu-id="4d012-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4d012-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4d012-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d012-102">SYNOPSIS</span></span>
<span data-ttu-id="4d012-103">將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4d012-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d012-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d012-104">SYNTAX</span></span>

### <span data-ttu-id="4d012-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d012-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d012-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4d012-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d012-107">說明</span><span class="sxs-lookup"><span data-stu-id="4d012-107">DESCRIPTION</span></span>
<span data-ttu-id="4d012-108">**AzureRmApplicationGatewayHttpListener** Cmdlet 會將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4d012-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="4d012-109">示例</span><span class="sxs-lookup"><span data-stu-id="4d012-109">EXAMPLES</span></span>

### <span data-ttu-id="4d012-110">範例1：新增 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="4d012-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="4d012-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將 HTTP 監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4d012-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="4d012-112">範例2：新增具有 SSL 的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="4d012-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="4d012-113">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4d012-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4d012-114">第二個命令會將使用 HTTPS 通訊協定的監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4d012-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="4d012-115">參數</span><span class="sxs-lookup"><span data-stu-id="4d012-115">PARAMETERS</span></span>

### <span data-ttu-id="4d012-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d012-116">-ApplicationGateway</span></span>
<span data-ttu-id="4d012-117">指定此 Cmdlet 新增 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4d012-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="4d012-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d012-118">-DefaultProfile</span></span>
<span data-ttu-id="4d012-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d012-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d012-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d012-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="4d012-121">指定應用程式閘道前端 IP 資源物件。</span><span class="sxs-lookup"><span data-stu-id="4d012-121">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="4d012-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4d012-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="4d012-123">指定應用程式閘道前端 IP ID。</span><span class="sxs-lookup"><span data-stu-id="4d012-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="4d012-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4d012-124">-FrontendPort</span></span>
<span data-ttu-id="4d012-125">指定應用程式閘道的 [前端埠] 物件。</span><span class="sxs-lookup"><span data-stu-id="4d012-125">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="4d012-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="4d012-126">-FrontendPortId</span></span>
<span data-ttu-id="4d012-127">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="4d012-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="4d012-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="4d012-128">-HostName</span></span>
<span data-ttu-id="4d012-129">指定此 Cmdlet 新增 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4d012-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="4d012-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d012-130">-Name</span></span>
<span data-ttu-id="4d012-131">指定此命令所新增之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d012-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="4d012-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4d012-132">-Protocol</span></span>
<span data-ttu-id="4d012-133">指定 HTTP 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4d012-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="4d012-134">支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="4d012-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="4d012-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="4d012-135">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="4d012-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="4d012-136">-SslCertificate</span></span>
<span data-ttu-id="4d012-137">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="4d012-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="4d012-138">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="4d012-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="4d012-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="4d012-139">-SslCertificateId</span></span>
<span data-ttu-id="4d012-140">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="4d012-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="4d012-141">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="4d012-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="4d012-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d012-142">CommonParameters</span></span>
<span data-ttu-id="4d012-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d012-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d012-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d012-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d012-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4d012-145">INPUTS</span></span>

### <span data-ttu-id="4d012-146">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4d012-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="4d012-147">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4d012-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="4d012-148">輸出</span><span class="sxs-lookup"><span data-stu-id="4d012-148">OUTPUTS</span></span>

### <span data-ttu-id="4d012-149">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4d012-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d012-150">筆記</span><span class="sxs-lookup"><span data-stu-id="4d012-150">NOTES</span></span>

## <span data-ttu-id="4d012-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d012-151">RELATED LINKS</span></span>

[<span data-ttu-id="4d012-152">AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4d012-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4d012-153">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4d012-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4d012-154">移除-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4d012-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4d012-155">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4d012-155">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)

