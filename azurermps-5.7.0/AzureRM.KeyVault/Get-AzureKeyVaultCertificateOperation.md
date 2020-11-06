---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 1f61207afbdf4c6553f6db4050775577d72c5eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447787"
---
# <span data-ttu-id="e2630-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e2630-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e2630-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2630-102">SYNOPSIS</span></span>
<span data-ttu-id="e2630-103">取得憑證操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e2630-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2630-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2630-104">SYNTAX</span></span>

### <span data-ttu-id="e2630-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e2630-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2630-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2630-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2630-107">說明</span><span class="sxs-lookup"><span data-stu-id="e2630-107">DESCRIPTION</span></span>
<span data-ttu-id="e2630-108">**AzureKeyVaultCertificateOperation** Cmdlet 會取得憑證操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e2630-108">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="e2630-109">示例</span><span class="sxs-lookup"><span data-stu-id="e2630-109">EXAMPLES</span></span>

### <span data-ttu-id="e2630-110">範例1：取得憑證操作的狀態</span><span class="sxs-lookup"><span data-stu-id="e2630-110">Example 1: Get the status of a certificate operation</span></span>
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

<span data-ttu-id="e2630-111">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e2630-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="e2630-112">參數</span><span class="sxs-lookup"><span data-stu-id="e2630-112">PARAMETERS</span></span>

### <span data-ttu-id="e2630-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2630-113">-DefaultProfile</span></span>
<span data-ttu-id="e2630-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e2630-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2630-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2630-115">-InputObject</span></span>
<span data-ttu-id="e2630-116">[憑證] 物件。</span><span class="sxs-lookup"><span data-stu-id="e2630-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2630-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2630-117">-Name</span></span>
<span data-ttu-id="e2630-118">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2630-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2630-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e2630-119">-VaultName</span></span>
<span data-ttu-id="e2630-120">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2630-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2630-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2630-121">CommonParameters</span></span>
<span data-ttu-id="e2630-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2630-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2630-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2630-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2630-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e2630-124">INPUTS</span></span>

### <span data-ttu-id="e2630-125">所有</span><span class="sxs-lookup"><span data-stu-id="e2630-125">None</span></span>
<span data-ttu-id="e2630-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e2630-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2630-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e2630-127">OUTPUTS</span></span>

### <span data-ttu-id="e2630-128">PSKeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e2630-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e2630-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e2630-129">NOTES</span></span>

## <span data-ttu-id="e2630-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2630-130">RELATED LINKS</span></span>

[<span data-ttu-id="e2630-131">移除-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e2630-131">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="e2630-132">停止 AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e2630-132">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

