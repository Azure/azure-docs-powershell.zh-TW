---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789414"
---
# <span data-ttu-id="1fe0a-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe0a-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1fe0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fe0a-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe0a-103">建立應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="1fe0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fe0a-104">SYNTAX</span></span>

### <span data-ttu-id="1fe0a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe0a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fe0a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1fe0a-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fe0a-107">說明</span><span class="sxs-lookup"><span data-stu-id="1fe0a-107">DESCRIPTION</span></span>
<span data-ttu-id="1fe0a-108">**新的-AzApplicationGatewayHttpListener** Cmdlet 會建立 Azure 應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="1fe0a-109">示例</span><span class="sxs-lookup"><span data-stu-id="1fe0a-109">EXAMPLES</span></span>

### <span data-ttu-id="1fe0a-110">範例1：建立 HTTP 監聽程式</span><span class="sxs-lookup"><span data-stu-id="1fe0a-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="1fe0a-111">這個命令會建立一個名為 Listener01 的 HTTP 偵聽程式，並將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="1fe0a-112">範例2：使用 SSL 建立 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="1fe0a-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="1fe0a-113">這個命令會建立使用 SSL 卸載的 HTTP 偵聽程式，並在 $SSLCert 01 變數中提供 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="1fe0a-114">該命令會將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="1fe0a-115">參數</span><span class="sxs-lookup"><span data-stu-id="1fe0a-115">PARAMETERS</span></span>

### <span data-ttu-id="1fe0a-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fe0a-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="1fe0a-117">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="1fe0a-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="1fe0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe0a-118">-DefaultProfile</span></span>
<span data-ttu-id="1fe0a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe0a-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fe0a-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="1fe0a-121">指定 HTTP 偵聽程式的前端 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="1fe0a-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1fe0a-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="1fe0a-123">指定 HTTP 偵聽程式的前端 IP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="1fe0a-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1fe0a-124">-FrontendPort</span></span>
<span data-ttu-id="1fe0a-125">指定 HTTP 偵聽程式的前端埠。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="1fe0a-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="1fe0a-126">-FrontendPortId</span></span>
<span data-ttu-id="1fe0a-127">指定 HTTP 偵聽程式前端埠物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="1fe0a-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="1fe0a-128">-HostName</span></span>
<span data-ttu-id="1fe0a-129">指定應用程式閘道 HTTP 監聽器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="1fe0a-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fe0a-130">-Name</span></span>
<span data-ttu-id="1fe0a-131">指定此 Cmdlet 所建立之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1fe0a-132">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="1fe0a-132">-Protocol</span></span>
<span data-ttu-id="1fe0a-133">指定 HTTP 偵聽程式使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="1fe0a-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="1fe0a-134">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="1fe0a-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe0a-135">-SslCertificate</span></span>
<span data-ttu-id="1fe0a-136">指定 HTTP 偵聽程式的 SSL 憑證物件。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="1fe0a-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="1fe0a-137">-SslCertificateId</span></span>
<span data-ttu-id="1fe0a-138">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="1fe0a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe0a-139">CommonParameters</span></span>
<span data-ttu-id="1fe0a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe0a-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fe0a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe0a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="1fe0a-142">INPUTS</span></span>

### <span data-ttu-id="1fe0a-143">所有</span><span class="sxs-lookup"><span data-stu-id="1fe0a-143">None</span></span>

## <span data-ttu-id="1fe0a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="1fe0a-144">OUTPUTS</span></span>

### <span data-ttu-id="1fe0a-145">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1fe0a-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1fe0a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="1fe0a-146">NOTES</span></span>

## <span data-ttu-id="1fe0a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fe0a-147">RELATED LINKS</span></span>

[<span data-ttu-id="1fe0a-148">附加 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe0a-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1fe0a-149">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe0a-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1fe0a-150">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe0a-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1fe0a-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe0a-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


