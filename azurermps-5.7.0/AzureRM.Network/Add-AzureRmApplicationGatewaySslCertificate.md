---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7cf1f52c8035adcb6dcb773106a77045525cf937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449311"
---
# <span data-ttu-id="1364a-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1364a-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1364a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1364a-102">SYNOPSIS</span></span>
<span data-ttu-id="1364a-103">將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1364a-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1364a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1364a-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1364a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1364a-105">DESCRIPTION</span></span>
<span data-ttu-id="1364a-106">**載入 AzureRmApplicationGatewaySslCertificate** Cmdlet 會將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1364a-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="1364a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1364a-107">EXAMPLES</span></span>

### <span data-ttu-id="1364a-108">範例1：將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1364a-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="1364a-109">這個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將名為 Cert01 的 SSL 憑證新增至它。</span><span class="sxs-lookup"><span data-stu-id="1364a-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="1364a-110">參數</span><span class="sxs-lookup"><span data-stu-id="1364a-110">PARAMETERS</span></span>

### <span data-ttu-id="1364a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1364a-111">-ApplicationGateway</span></span>
<span data-ttu-id="1364a-112">指定此 Cmdlet 新增 SSL 憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="1364a-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="1364a-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1364a-113">-CertificateFile</span></span>
<span data-ttu-id="1364a-114">指定此 Cmdlet 所新增之 SSL 憑證的 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="1364a-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1364a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1364a-115">-DefaultProfile</span></span>
<span data-ttu-id="1364a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1364a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1364a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1364a-117">-Name</span></span>
<span data-ttu-id="1364a-118">指定此 Cmdlet 所新增之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="1364a-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1364a-119">-Password</span><span class="sxs-lookup"><span data-stu-id="1364a-119">-Password</span></span>
<span data-ttu-id="1364a-120">指定此 Cmdlet 所新增之 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="1364a-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1364a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1364a-121">CommonParameters</span></span>
<span data-ttu-id="1364a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1364a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1364a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1364a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1364a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1364a-124">INPUTS</span></span>

### <span data-ttu-id="1364a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="1364a-125">System.String</span></span>

## <span data-ttu-id="1364a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1364a-126">OUTPUTS</span></span>

### <span data-ttu-id="1364a-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1364a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1364a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1364a-128">NOTES</span></span>

## <span data-ttu-id="1364a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1364a-129">RELATED LINKS</span></span>

[<span data-ttu-id="1364a-130">AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1364a-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1364a-131">新-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1364a-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1364a-132">移除-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1364a-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1364a-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1364a-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


