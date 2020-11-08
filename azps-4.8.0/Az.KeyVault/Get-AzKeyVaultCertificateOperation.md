---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: f1b46162124214cfca3db2fefa1f3d02227bb0f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971041"
---
# <span data-ttu-id="4ad37-101">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="4ad37-101">Get-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="4ad37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ad37-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad37-103">取得憑證操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad37-103">Gets the status of a certificate operation.</span></span>

## <span data-ttu-id="4ad37-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ad37-104">SYNTAX</span></span>

### <span data-ttu-id="4ad37-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="4ad37-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ad37-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ad37-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ad37-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ad37-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad37-108">**AzKeyVaultCertificateOperation** Cmdlet 會取得憑證操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad37-108">The **Get-AzKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="4ad37-109">示例</span><span class="sxs-lookup"><span data-stu-id="4ad37-109">EXAMPLES</span></span>

### <span data-ttu-id="4ad37-110">範例1：取得憑證操作的狀態</span><span class="sxs-lookup"><span data-stu-id="4ad37-110">Example 1: Get the status of a certificate operation</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateOperation -VaultName "contosoKV01" -Name "TestCert01"

Id                        : https://contosoKV01.vault.azure.net/certificates/TestCert01/pending
Status                    : inProgress
StatusDetails             : Pending certificate created. Certificate request is in progress. This may take some time
                            based on the issuer provider. Please check again later.
RequestId                 : 32a63e80568442a2892dafb9f7cf366t
Target                    :
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="4ad37-111">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad37-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="4ad37-112">參數</span><span class="sxs-lookup"><span data-stu-id="4ad37-112">PARAMETERS</span></span>

### <span data-ttu-id="4ad37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad37-113">-DefaultProfile</span></span>
<span data-ttu-id="4ad37-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4ad37-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad37-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ad37-115">-InputObject</span></span>
<span data-ttu-id="4ad37-116">[憑證] 物件。</span><span class="sxs-lookup"><span data-stu-id="4ad37-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad37-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ad37-117">-Name</span></span>
<span data-ttu-id="4ad37-118">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad37-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad37-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ad37-119">-VaultName</span></span>
<span data-ttu-id="4ad37-120">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad37-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad37-121">CommonParameters</span></span>
<span data-ttu-id="4ad37-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ad37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad37-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ad37-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad37-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4ad37-124">INPUTS</span></span>

### <span data-ttu-id="4ad37-125">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="4ad37-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="4ad37-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4ad37-126">OUTPUTS</span></span>

### <span data-ttu-id="4ad37-127">PSKeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="4ad37-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="4ad37-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4ad37-128">NOTES</span></span>

## <span data-ttu-id="4ad37-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ad37-129">RELATED LINKS</span></span>

[<span data-ttu-id="4ad37-130">移除-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="4ad37-130">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="4ad37-131">停止 AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="4ad37-131">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)
