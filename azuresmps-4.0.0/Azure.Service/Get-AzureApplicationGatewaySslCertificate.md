---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967110"
---
# <span data-ttu-id="ec70b-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec70b-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ec70b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec70b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec70b-103">取得應用程式閘道憑證。</span><span class="sxs-lookup"><span data-stu-id="ec70b-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="ec70b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec70b-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec70b-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec70b-105">DESCRIPTION</span></span>
<span data-ttu-id="ec70b-106">**AzureApplicationGatewaySslCertificate** Cmdlet 會針對 Azure 應用程式閘道 (SSL) 憑證取得安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="ec70b-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="ec70b-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec70b-107">EXAMPLES</span></span>

### <span data-ttu-id="ec70b-108">範例1：取得 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="ec70b-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="ec70b-109">這個命令會在名為 ApplicationGateway08 的應用程式閘道上，取得一個名為 SslCertificate13 的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="ec70b-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="ec70b-110">範例2：取得所有 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="ec70b-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="ec70b-111">這個命令會在名為 ApplicationGateway08 的應用程式閘道上取得所有 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="ec70b-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="ec70b-112">參數</span><span class="sxs-lookup"><span data-stu-id="ec70b-112">PARAMETERS</span></span>

### <span data-ttu-id="ec70b-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ec70b-113">-CertificateName</span></span>
<span data-ttu-id="ec70b-114">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec70b-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="ec70b-115">這個 Cmdlet 會取得此參數指定的憑證。</span><span class="sxs-lookup"><span data-stu-id="ec70b-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec70b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec70b-116">-Name</span></span>
<span data-ttu-id="ec70b-117">指定此 Cmdlet 取得 SSL 憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec70b-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

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

### <span data-ttu-id="ec70b-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ec70b-118">-Profile</span></span>
<span data-ttu-id="ec70b-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ec70b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec70b-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ec70b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec70b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec70b-121">CommonParameters</span></span>
<span data-ttu-id="ec70b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec70b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec70b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec70b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec70b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ec70b-124">INPUTS</span></span>

### <span data-ttu-id="ec70b-125">System.object</span><span class="sxs-lookup"><span data-stu-id="ec70b-125">System.String</span></span>

## <span data-ttu-id="ec70b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ec70b-126">OUTPUTS</span></span>

### <span data-ttu-id="ec70b-127">ApplicationGatewayObjectModel ApplicationGatewayCertificate、清單<ApplicationGatewayObjectModel. ApplicationGatewayCertificate 的.></span><span class="sxs-lookup"><span data-stu-id="ec70b-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="ec70b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ec70b-128">NOTES</span></span>

## <span data-ttu-id="ec70b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec70b-129">RELATED LINKS</span></span>

[<span data-ttu-id="ec70b-130">附加 AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec70b-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ec70b-131">移除-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ec70b-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
