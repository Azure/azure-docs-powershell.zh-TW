---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6805eaa6f1d710c607a7911b628d3642d48ece29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624543"
---
# <span data-ttu-id="d9932-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d9932-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d9932-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9932-102">SYNOPSIS</span></span>
<span data-ttu-id="d9932-103">修改應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="d9932-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9932-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9932-104">SYNTAX</span></span>

### <span data-ttu-id="d9932-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9932-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9932-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d9932-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9932-107">說明</span><span class="sxs-lookup"><span data-stu-id="d9932-107">DESCRIPTION</span></span>
<span data-ttu-id="d9932-108">**AzureRmApplicationGatewayHttpListener** Cmdlet 會修改 Azure 應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="d9932-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="d9932-109">示例</span><span class="sxs-lookup"><span data-stu-id="d9932-109">EXAMPLES</span></span>

### <span data-ttu-id="d9932-110">範例1：設定 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="d9932-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="d9932-111">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="d9932-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="d9932-112">第二個命令會將閘道的 HTTP 偵聽程式設定為使用以埠80上的 HTTP 通訊協定儲存在 $FIP 01 中的前端配置。</span><span class="sxs-lookup"><span data-stu-id="d9932-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="d9932-113">參數</span><span class="sxs-lookup"><span data-stu-id="d9932-113">PARAMETERS</span></span>

### <span data-ttu-id="d9932-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9932-114">-ApplicationGateway</span></span>
<span data-ttu-id="d9932-115">指定此 Cmdlet 與 HTTP 偵聽程式關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d9932-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="d9932-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9932-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d9932-117">指定應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d9932-117">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d9932-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d9932-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d9932-119">指定應用程式閘道的前端 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9932-119">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d9932-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d9932-120">-FrontendPort</span></span>
<span data-ttu-id="d9932-121">指定應用程式閘道前端埠。</span><span class="sxs-lookup"><span data-stu-id="d9932-121">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="d9932-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="d9932-122">-FrontendPortId</span></span>
<span data-ttu-id="d9932-123">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="d9932-123">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="d9932-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="d9932-124">-HostName</span></span>
<span data-ttu-id="d9932-125">指定此 Cmdlet 傳送 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d9932-125">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="d9932-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9932-126">-Name</span></span>
<span data-ttu-id="d9932-127">指定 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9932-127">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="d9932-128">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d9932-128">-Protocol</span></span>
<span data-ttu-id="d9932-129">指定 HTTP 偵聽程式使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d9932-129">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="d9932-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d9932-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9932-131">Http</span><span class="sxs-lookup"><span data-stu-id="d9932-131">Http</span></span>
- <span data-ttu-id="d9932-132">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="d9932-132">Https</span></span>

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

### <span data-ttu-id="d9932-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d9932-133">-RequireServerNameIndication</span></span>
<span data-ttu-id="d9932-134">指定 Cmdlet 是否需要伺服器名稱指示。</span><span class="sxs-lookup"><span data-stu-id="d9932-134">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="d9932-135">此參數可接受的值為： true 或 false。</span><span class="sxs-lookup"><span data-stu-id="d9932-135">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="d9932-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d9932-136">-SslCertificate</span></span>
<span data-ttu-id="d9932-137">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="d9932-137">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="d9932-138">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="d9932-138">-SslCertificateId</span></span>
<span data-ttu-id="d9932-139">指定 (SSL) HTTP 偵聽程式的憑證 ID 的安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="d9932-139">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="d9932-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9932-140">-DefaultProfile</span></span>
<span data-ttu-id="d9932-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9932-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9932-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9932-142">CommonParameters</span></span>
<span data-ttu-id="d9932-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9932-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9932-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9932-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9932-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d9932-145">INPUTS</span></span>

### <span data-ttu-id="d9932-146">System.object</span><span class="sxs-lookup"><span data-stu-id="d9932-146">System.String</span></span>

## <span data-ttu-id="d9932-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d9932-147">OUTPUTS</span></span>

### <span data-ttu-id="d9932-148">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d9932-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9932-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d9932-149">NOTES</span></span>

## <span data-ttu-id="d9932-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9932-150">RELATED LINKS</span></span>

[<span data-ttu-id="d9932-151">附加 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d9932-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d9932-152">AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d9932-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d9932-153">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d9932-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d9932-154">移除-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d9932-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


