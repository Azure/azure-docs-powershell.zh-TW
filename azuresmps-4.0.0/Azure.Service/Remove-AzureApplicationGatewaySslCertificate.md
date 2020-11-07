---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967940"
---
# <span data-ttu-id="4b203-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b203-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4b203-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b203-102">SYNOPSIS</span></span>
<span data-ttu-id="4b203-103">從應用程式閘道移除 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="4b203-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="4b203-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b203-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b203-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b203-105">DESCRIPTION</span></span>
<span data-ttu-id="4b203-106">**AzureApplicationGatewaySslCertificate** Cmdlet 會從應用程式閘道 (SSL) 憑證中移除安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="4b203-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="4b203-107">示例</span><span class="sxs-lookup"><span data-stu-id="4b203-107">EXAMPLES</span></span>

### <span data-ttu-id="4b203-108">範例1：移除 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="4b203-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="4b203-109">這個命令會將名為 SslCertificate13 的 SSL 憑證從名為 ApplicationGateway08 的應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="4b203-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="4b203-110">參數</span><span class="sxs-lookup"><span data-stu-id="4b203-110">PARAMETERS</span></span>

### <span data-ttu-id="4b203-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4b203-111">-CertificateName</span></span>
<span data-ttu-id="4b203-112">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b203-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="4b203-113">這個 Cmdlet 會移除此參數指定的憑證。</span><span class="sxs-lookup"><span data-stu-id="4b203-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b203-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b203-114">-Name</span></span>
<span data-ttu-id="4b203-115">指定此 Cmdlet 移除 SSL 憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b203-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="4b203-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4b203-116">-Profile</span></span>
<span data-ttu-id="4b203-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b203-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b203-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4b203-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b203-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b203-119">CommonParameters</span></span>
<span data-ttu-id="4b203-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b203-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b203-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b203-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b203-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4b203-122">INPUTS</span></span>

### <span data-ttu-id="4b203-123">System.object</span><span class="sxs-lookup"><span data-stu-id="4b203-123">System.String</span></span>

## <span data-ttu-id="4b203-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4b203-124">OUTPUTS</span></span>

### <span data-ttu-id="4b203-125">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="4b203-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="4b203-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4b203-126">NOTES</span></span>

## <span data-ttu-id="4b203-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b203-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b203-128">附加 AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b203-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4b203-129">AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b203-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
