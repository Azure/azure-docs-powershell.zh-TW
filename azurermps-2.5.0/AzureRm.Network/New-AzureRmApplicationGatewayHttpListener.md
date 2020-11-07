---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: f6b8e2a869ba6c59011241c5ebb7b1fe46ac2bc7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800089"
---
# <span data-ttu-id="6d2ef-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6d2ef-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6d2ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2ef-103">建立應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d2ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d2ef-104">SYNTAX</span></span>

### <span data-ttu-id="6d2ef-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d2ef-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d2ef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6d2ef-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d2ef-107">說明</span><span class="sxs-lookup"><span data-stu-id="6d2ef-107">DESCRIPTION</span></span>
<span data-ttu-id="6d2ef-108">**新的-AzureRmApplicationGatewayHttpListener** Cmdlet 會建立 Azure 應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="6d2ef-109">示例</span><span class="sxs-lookup"><span data-stu-id="6d2ef-109">EXAMPLES</span></span>

### <span data-ttu-id="6d2ef-110">範例1：建立 HTTP 監聽程式</span><span class="sxs-lookup"><span data-stu-id="6d2ef-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="6d2ef-111">這個命令會建立一個名為 Listener01 的 HTTP 偵聽程式，並將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="6d2ef-112">範例2：使用 SSL 建立 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="6d2ef-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="6d2ef-113">這個命令會建立使用 SSL 卸載的 HTTP 偵聽程式，並在 $SSLCert 01 變數中提供 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="6d2ef-114">該命令會將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="6d2ef-115">參數</span><span class="sxs-lookup"><span data-stu-id="6d2ef-115">PARAMETERS</span></span>

### <span data-ttu-id="6d2ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2ef-116">-DefaultProfile</span></span>
<span data-ttu-id="6d2ef-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d2ef-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d2ef-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="6d2ef-119">指定 HTTP 偵聽程式的前端 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="6d2ef-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6d2ef-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="6d2ef-121">指定 HTTP 偵聽程式的前端 IP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="6d2ef-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6d2ef-122">-FrontendPort</span></span>
<span data-ttu-id="6d2ef-123">指定 HTTP 偵聽程式的前端埠。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="6d2ef-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="6d2ef-124">-FrontendPortId</span></span>
<span data-ttu-id="6d2ef-125">指定 HTTP 偵聽程式前端埠物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="6d2ef-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="6d2ef-126">-HostName</span></span>
<span data-ttu-id="6d2ef-127">指定應用程式閘道 HTTP 監聽器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="6d2ef-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d2ef-128">-Name</span></span>
<span data-ttu-id="6d2ef-129">指定此 Cmdlet 所建立之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6d2ef-130">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="6d2ef-130">-Protocol</span></span>
<span data-ttu-id="6d2ef-131">指定 HTTP 偵聽程式使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="6d2ef-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="6d2ef-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="6d2ef-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6d2ef-133">-SslCertificate</span></span>
<span data-ttu-id="6d2ef-134">指定 HTTP 偵聽程式的 SSL 憑證物件。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="6d2ef-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="6d2ef-135">-SslCertificateId</span></span>
<span data-ttu-id="6d2ef-136">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="6d2ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2ef-137">CommonParameters</span></span>
<span data-ttu-id="6d2ef-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2ef-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d2ef-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2ef-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6d2ef-140">INPUTS</span></span>

### <span data-ttu-id="6d2ef-141">System.object</span><span class="sxs-lookup"><span data-stu-id="6d2ef-141">System.String</span></span>

## <span data-ttu-id="6d2ef-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6d2ef-142">OUTPUTS</span></span>

### <span data-ttu-id="6d2ef-143">PSHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6d2ef-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="6d2ef-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6d2ef-144">NOTES</span></span>

## <span data-ttu-id="6d2ef-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d2ef-145">RELATED LINKS</span></span>

[<span data-ttu-id="6d2ef-146">附加 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6d2ef-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6d2ef-147">AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6d2ef-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6d2ef-148">移除-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6d2ef-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6d2ef-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6d2ef-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


