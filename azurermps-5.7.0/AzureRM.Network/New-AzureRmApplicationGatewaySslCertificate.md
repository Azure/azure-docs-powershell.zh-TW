---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7e75a74b99cc6a7e3da6a5f2ae2a2c3280efbfbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625883"
---
# <span data-ttu-id="f6bf5-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f6bf5-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f6bf5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bf5-103">建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6bf5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6bf5-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6bf5-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="f6bf5-106">**新的 AzureRmApplicationGatewaySslCertificate** Cmdlet 會建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f6bf5-107">示例</span><span class="sxs-lookup"><span data-stu-id="f6bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="f6bf5-108">範例1：建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="f6bf5-109">這個命令會建立名為 Cert01 的 SSL 憑證，以用於預設的應用程式閘道，並將結果儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="f6bf5-110">參數</span><span class="sxs-lookup"><span data-stu-id="f6bf5-110">PARAMETERS</span></span>

### <span data-ttu-id="f6bf5-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f6bf5-111">-CertificateFile</span></span>
<span data-ttu-id="f6bf5-112">指定此 Cmdlet 建立之 SSL 憑證之 .pfx 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f6bf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bf5-113">-DefaultProfile</span></span>
<span data-ttu-id="f6bf5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6bf5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6bf5-115">-Name</span></span>
<span data-ttu-id="f6bf5-116">指定此 Cmdlet 所建立之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f6bf5-117">-Password</span><span class="sxs-lookup"><span data-stu-id="f6bf5-117">-Password</span></span>
<span data-ttu-id="f6bf5-118">指定此 Cmdlet 所建立之 SSL 的密碼。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f6bf5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bf5-119">CommonParameters</span></span>
<span data-ttu-id="f6bf5-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bf5-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6bf5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bf5-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f6bf5-122">INPUTS</span></span>

### <span data-ttu-id="f6bf5-123">System.object</span><span class="sxs-lookup"><span data-stu-id="f6bf5-123">System.String</span></span>

## <span data-ttu-id="f6bf5-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f6bf5-124">OUTPUTS</span></span>

### <span data-ttu-id="f6bf5-125">PSApplicationGatewaySslCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6bf5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f6bf5-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f6bf5-126">NOTES</span></span>

## <span data-ttu-id="f6bf5-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6bf5-127">RELATED LINKS</span></span>

[<span data-ttu-id="f6bf5-128">附加 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f6bf5-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f6bf5-129">AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f6bf5-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f6bf5-130">移除-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f6bf5-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f6bf5-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f6bf5-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


