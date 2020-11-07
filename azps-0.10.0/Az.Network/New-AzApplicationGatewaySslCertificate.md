---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794294"
---
# <span data-ttu-id="2ad41-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ad41-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2ad41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ad41-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad41-103">建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="2ad41-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="2ad41-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ad41-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ad41-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ad41-105">DESCRIPTION</span></span>
<span data-ttu-id="2ad41-106">**新的 AzApplicationGatewaySslCertificate** Cmdlet 會建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="2ad41-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="2ad41-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ad41-107">EXAMPLES</span></span>

### <span data-ttu-id="2ad41-108">範例1：建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="2ad41-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="2ad41-109">這個命令會建立名為 Cert01 的 SSL 憑證，以用於預設的應用程式閘道，並將結果儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="2ad41-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="2ad41-110">參數</span><span class="sxs-lookup"><span data-stu-id="2ad41-110">PARAMETERS</span></span>

### <span data-ttu-id="2ad41-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2ad41-111">-CertificateFile</span></span>
<span data-ttu-id="2ad41-112">指定此 Cmdlet 建立之 SSL 憑證之 .pfx 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2ad41-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2ad41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad41-113">-DefaultProfile</span></span>
<span data-ttu-id="2ad41-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ad41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ad41-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ad41-115">-Name</span></span>
<span data-ttu-id="2ad41-116">指定此 Cmdlet 所建立之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad41-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2ad41-117">-Password</span><span class="sxs-lookup"><span data-stu-id="2ad41-117">-Password</span></span>
<span data-ttu-id="2ad41-118">指定此 Cmdlet 所建立之 SSL 的密碼。</span><span class="sxs-lookup"><span data-stu-id="2ad41-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2ad41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad41-119">CommonParameters</span></span>
<span data-ttu-id="2ad41-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ad41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad41-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ad41-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad41-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2ad41-122">INPUTS</span></span>

### <span data-ttu-id="2ad41-123">System.object</span><span class="sxs-lookup"><span data-stu-id="2ad41-123">System.String</span></span>

## <span data-ttu-id="2ad41-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2ad41-124">OUTPUTS</span></span>

### <span data-ttu-id="2ad41-125">PSApplicationGatewaySslCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ad41-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2ad41-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2ad41-126">NOTES</span></span>

## <span data-ttu-id="2ad41-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ad41-127">RELATED LINKS</span></span>

[<span data-ttu-id="2ad41-128">附加 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ad41-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2ad41-129">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ad41-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2ad41-130">移除-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ad41-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2ad41-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2ad41-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


