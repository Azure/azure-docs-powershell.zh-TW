---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967182"
---
# <span data-ttu-id="be261-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="be261-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="be261-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be261-102">SYNOPSIS</span></span>
<span data-ttu-id="be261-103">將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="be261-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="be261-104">句法</span><span class="sxs-lookup"><span data-stu-id="be261-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="be261-105">說明</span><span class="sxs-lookup"><span data-stu-id="be261-105">DESCRIPTION</span></span>
<span data-ttu-id="be261-106">**AzureApplicationGatewaySslCertificate** Cmdlet 會將安全通訊端層 (SSL) 憑證新增至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="be261-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="be261-107">示例</span><span class="sxs-lookup"><span data-stu-id="be261-107">EXAMPLES</span></span>

### <span data-ttu-id="be261-108">範例1：新增 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="be261-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="be261-109">這個命令會將一個名為 SslCertificate13 的 SSL 憑證新增到名為 ApplicationGateway08 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="be261-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="be261-110">此命令會指定憑證檔案的路徑和憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="be261-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="be261-111">參數</span><span class="sxs-lookup"><span data-stu-id="be261-111">PARAMETERS</span></span>

### <span data-ttu-id="be261-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="be261-112">-CertificateFile</span></span>
<span data-ttu-id="be261-113">指定 SSL 憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="be261-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="be261-114">這個 Cmdlet 會將憑證新增到此參數指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="be261-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be261-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="be261-115">-CertificateName</span></span>
<span data-ttu-id="be261-116">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="be261-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="be261-117">這個 Cmdlet 會新增此參數指定的憑證。</span><span class="sxs-lookup"><span data-stu-id="be261-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be261-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="be261-118">-Name</span></span>
<span data-ttu-id="be261-119">指定此 Cmdlet 新增 SSL 憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="be261-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be261-120">-Password</span><span class="sxs-lookup"><span data-stu-id="be261-120">-Password</span></span>
<span data-ttu-id="be261-121">指定此 Cmdlet 所新增之 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="be261-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be261-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="be261-122">-Profile</span></span>
<span data-ttu-id="be261-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="be261-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be261-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="be261-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be261-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be261-125">CommonParameters</span></span>
<span data-ttu-id="be261-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be261-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be261-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be261-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be261-128">輸入</span><span class="sxs-lookup"><span data-stu-id="be261-128">INPUTS</span></span>

### <span data-ttu-id="be261-129">System.object</span><span class="sxs-lookup"><span data-stu-id="be261-129">System.String</span></span>

## <span data-ttu-id="be261-130">輸出</span><span class="sxs-lookup"><span data-stu-id="be261-130">OUTPUTS</span></span>

### <span data-ttu-id="be261-131">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="be261-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="be261-132">筆記</span><span class="sxs-lookup"><span data-stu-id="be261-132">NOTES</span></span>

## <span data-ttu-id="be261-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="be261-133">RELATED LINKS</span></span>

[<span data-ttu-id="be261-134">AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="be261-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="be261-135">移除-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="be261-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
