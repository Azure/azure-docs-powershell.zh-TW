---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 29df7c4ac7cb941e8826c3e1fb929d92cc626512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451867"
---
# <span data-ttu-id="a7933-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a7933-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a7933-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7933-102">SYNOPSIS</span></span>
<span data-ttu-id="a7933-103">建立應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a7933-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7933-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7933-104">SYNTAX</span></span>

### <span data-ttu-id="a7933-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7933-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7933-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a7933-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7933-107">說明</span><span class="sxs-lookup"><span data-stu-id="a7933-107">DESCRIPTION</span></span>
<span data-ttu-id="a7933-108">**新的-AzureRmApplicationGatewayHttpListener** Cmdlet 會建立 Azure 應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a7933-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a7933-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7933-109">EXAMPLES</span></span>

### <span data-ttu-id="a7933-110">範例1：建立 HTTP 監聽程式</span><span class="sxs-lookup"><span data-stu-id="a7933-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="a7933-111">這個命令會建立一個名為 Listener01 的 HTTP 偵聽程式，並將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="a7933-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="a7933-112">範例2：使用 SSL 建立 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="a7933-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="a7933-113">這個命令會建立使用 SSL 卸載的 HTTP 偵聽程式，並在 $SSLCert 01 變數中提供 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="a7933-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="a7933-114">該命令會將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="a7933-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="a7933-115">參數</span><span class="sxs-lookup"><span data-stu-id="a7933-115">PARAMETERS</span></span>

### <span data-ttu-id="a7933-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7933-116">-DefaultProfile</span></span>
<span data-ttu-id="a7933-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7933-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7933-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7933-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a7933-119">指定 HTTP 偵聽程式的前端 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="a7933-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a7933-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a7933-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a7933-121">指定 HTTP 偵聽程式的前端 IP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="a7933-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="a7933-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a7933-122">-FrontendPort</span></span>
<span data-ttu-id="a7933-123">指定 HTTP 偵聽程式的前端埠。</span><span class="sxs-lookup"><span data-stu-id="a7933-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="a7933-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a7933-124">-FrontendPortId</span></span>
<span data-ttu-id="a7933-125">指定 HTTP 偵聽程式前端埠物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7933-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a7933-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="a7933-126">-HostName</span></span>
<span data-ttu-id="a7933-127">指定應用程式閘道 HTTP 監聽器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="a7933-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="a7933-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7933-128">-Name</span></span>
<span data-ttu-id="a7933-129">指定此 Cmdlet 所建立之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7933-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a7933-130">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a7933-130">-Protocol</span></span>
<span data-ttu-id="a7933-131">指定 HTTP 偵聽程式使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a7933-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="a7933-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a7933-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="a7933-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a7933-133">-SslCertificate</span></span>
<span data-ttu-id="a7933-134">指定 HTTP 偵聽程式的 SSL 憑證物件。</span><span class="sxs-lookup"><span data-stu-id="a7933-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="a7933-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a7933-135">-SslCertificateId</span></span>
<span data-ttu-id="a7933-136">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="a7933-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="a7933-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7933-137">CommonParameters</span></span>
<span data-ttu-id="a7933-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7933-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7933-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7933-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7933-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a7933-140">INPUTS</span></span>

### <span data-ttu-id="a7933-141">所有</span><span class="sxs-lookup"><span data-stu-id="a7933-141">None</span></span>

## <span data-ttu-id="a7933-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a7933-142">OUTPUTS</span></span>

### <span data-ttu-id="a7933-143">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7933-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a7933-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a7933-144">NOTES</span></span>

## <span data-ttu-id="a7933-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7933-145">RELATED LINKS</span></span>

[<span data-ttu-id="a7933-146">附加 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a7933-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a7933-147">AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a7933-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a7933-148">移除-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a7933-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a7933-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a7933-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


