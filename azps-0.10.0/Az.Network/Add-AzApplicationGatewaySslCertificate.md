---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 964e99912e4f21d48e89b725da1aa44ac32ea186
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794528"
---
# <span data-ttu-id="a63ee-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a63ee-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="a63ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a63ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a63ee-103">將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a63ee-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="a63ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="a63ee-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a63ee-105">說明</span><span class="sxs-lookup"><span data-stu-id="a63ee-105">DESCRIPTION</span></span>
<span data-ttu-id="a63ee-106">**載入 AzApplicationGatewaySslCertificate** Cmdlet 會將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a63ee-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="a63ee-107">示例</span><span class="sxs-lookup"><span data-stu-id="a63ee-107">EXAMPLES</span></span>

### <span data-ttu-id="a63ee-108">範例1：將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a63ee-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="a63ee-109">這個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將名為 Cert01 的 SSL 憑證新增至它。</span><span class="sxs-lookup"><span data-stu-id="a63ee-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="a63ee-110">參數</span><span class="sxs-lookup"><span data-stu-id="a63ee-110">PARAMETERS</span></span>

### <span data-ttu-id="a63ee-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a63ee-111">-ApplicationGateway</span></span>
<span data-ttu-id="a63ee-112">指定此 Cmdlet 新增 SSL 憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="a63ee-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="a63ee-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a63ee-113">-CertificateFile</span></span>
<span data-ttu-id="a63ee-114">指定此 Cmdlet 所新增之 SSL 憑證的 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="a63ee-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a63ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63ee-115">-DefaultProfile</span></span>
<span data-ttu-id="a63ee-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a63ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a63ee-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a63ee-117">-Name</span></span>
<span data-ttu-id="a63ee-118">指定此 Cmdlet 所新增之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="a63ee-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a63ee-119">-Password</span><span class="sxs-lookup"><span data-stu-id="a63ee-119">-Password</span></span>
<span data-ttu-id="a63ee-120">指定此 Cmdlet 所新增之 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="a63ee-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a63ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63ee-121">CommonParameters</span></span>
<span data-ttu-id="a63ee-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a63ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63ee-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a63ee-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63ee-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a63ee-124">INPUTS</span></span>

### <span data-ttu-id="a63ee-125">System.object</span><span class="sxs-lookup"><span data-stu-id="a63ee-125">System.String</span></span>

## <span data-ttu-id="a63ee-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a63ee-126">OUTPUTS</span></span>

### <span data-ttu-id="a63ee-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a63ee-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a63ee-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a63ee-128">NOTES</span></span>

## <span data-ttu-id="a63ee-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a63ee-129">RELATED LINKS</span></span>

[<span data-ttu-id="a63ee-130">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a63ee-130">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a63ee-131">新-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a63ee-131">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a63ee-132">移除-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a63ee-132">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a63ee-133">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a63ee-133">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


