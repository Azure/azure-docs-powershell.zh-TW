---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: dd9260fa833a09736aaba4b63f56f5b5c894662d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446800"
---
# <span data-ttu-id="77818-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="77818-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="77818-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77818-102">SYNOPSIS</span></span>
<span data-ttu-id="77818-103">取得憑證操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="77818-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77818-104">句法</span><span class="sxs-lookup"><span data-stu-id="77818-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77818-105">說明</span><span class="sxs-lookup"><span data-stu-id="77818-105">DESCRIPTION</span></span>
<span data-ttu-id="77818-106">**AzureKeyVaultCertificateOperation** Cmdlet 會取得憑證操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="77818-106">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="77818-107">示例</span><span class="sxs-lookup"><span data-stu-id="77818-107">EXAMPLES</span></span>

### <span data-ttu-id="77818-108">範例1：取得憑證操作的狀態</span><span class="sxs-lookup"><span data-stu-id="77818-108">Example 1: Get the status of a certificate operation</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="77818-109">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="77818-109">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="77818-110">參數</span><span class="sxs-lookup"><span data-stu-id="77818-110">PARAMETERS</span></span>

### <span data-ttu-id="77818-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="77818-111">-Name</span></span>
<span data-ttu-id="77818-112">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="77818-112">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77818-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="77818-113">-VaultName</span></span>
<span data-ttu-id="77818-114">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="77818-114">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77818-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77818-115">-DefaultProfile</span></span>
<span data-ttu-id="77818-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77818-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77818-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77818-117">CommonParameters</span></span>
<span data-ttu-id="77818-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77818-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77818-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77818-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77818-120">輸入</span><span class="sxs-lookup"><span data-stu-id="77818-120">INPUTS</span></span>

## <span data-ttu-id="77818-121">輸出</span><span class="sxs-lookup"><span data-stu-id="77818-121">OUTPUTS</span></span>

### <span data-ttu-id="77818-122">KeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="77818-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="77818-123">筆記</span><span class="sxs-lookup"><span data-stu-id="77818-123">NOTES</span></span>

## <span data-ttu-id="77818-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="77818-124">RELATED LINKS</span></span>

[<span data-ttu-id="77818-125">移除-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="77818-125">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="77818-126">停止 AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="77818-126">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)
