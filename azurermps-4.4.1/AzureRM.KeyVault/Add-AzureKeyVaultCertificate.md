---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
ms.openlocfilehash: 97b6e34029b4eaac7d2157c2cf224398e8b253f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455780"
---
# <span data-ttu-id="e8a62-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a62-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="e8a62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8a62-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a62-103">將憑證新增到金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="e8a62-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a62-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8a62-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8a62-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8a62-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a62-106">**AzureKeyVaultCertificate** Cmdlet 會啟動在 Azure 金鑰保存庫中，在金鑰電子倉庫中註冊憑證的程式。</span><span class="sxs-lookup"><span data-stu-id="e8a62-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e8a62-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8a62-107">EXAMPLES</span></span>

### <span data-ttu-id="e8a62-108">範例1：新增憑證</span><span class="sxs-lookup"><span data-stu-id="e8a62-108">Example 1: Add a certificate</span></span>
```
PS C:\>$Policy = New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="e8a62-109">第一個命令使用 New-AzureKeyVaultCertificatePolicy Cmdlet 來建立證書原則，然後將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="e8a62-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="e8a62-110">第二個命令使用 [ **載入 AzureKeyVaultCertificate** ] 來啟動程式來建立證書。</span><span class="sxs-lookup"><span data-stu-id="e8a62-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="e8a62-111">第三個命令使用 Get-AzureKeyVaultCertificateOperation Cmdlet 來輪詢操作，以確認該作業已完成。</span><span class="sxs-lookup"><span data-stu-id="e8a62-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="e8a62-112">最後一個命令會使用 Get-AzureKeyVaultCertificate Cmdlet 來取得憑證。</span><span class="sxs-lookup"><span data-stu-id="e8a62-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="e8a62-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8a62-113">PARAMETERS</span></span>

### <span data-ttu-id="e8a62-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e8a62-114">-CertificatePolicy</span></span>
<span data-ttu-id="e8a62-115">指定 **KeyVaultCertificatePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="e8a62-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a62-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8a62-116">-Name</span></span>
<span data-ttu-id="e8a62-117">指定要新增的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="e8a62-117">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="e8a62-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8a62-118">-Tag</span></span>
<span data-ttu-id="e8a62-119">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e8a62-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e8a62-120">例如：</span><span class="sxs-lookup"><span data-stu-id="e8a62-120">For example:</span></span>

<span data-ttu-id="e8a62-121">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e8a62-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a62-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e8a62-122">-VaultName</span></span>
<span data-ttu-id="e8a62-123">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8a62-123">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="e8a62-124">-確認</span><span class="sxs-lookup"><span data-stu-id="e8a62-124">-Confirm</span></span>
<span data-ttu-id="e8a62-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8a62-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a62-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8a62-126">-WhatIf</span></span>
<span data-ttu-id="e8a62-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8a62-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8a62-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8a62-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a62-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a62-129">-DefaultProfile</span></span>
<span data-ttu-id="e8a62-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8a62-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8a62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a62-131">CommonParameters</span></span>
<span data-ttu-id="e8a62-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8a62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a62-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8a62-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a62-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e8a62-134">INPUTS</span></span>

## <span data-ttu-id="e8a62-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e8a62-135">OUTPUTS</span></span>

### <span data-ttu-id="e8a62-136">KeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e8a62-136">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e8a62-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e8a62-137">NOTES</span></span>

## <span data-ttu-id="e8a62-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8a62-138">RELATED LINKS</span></span>

[<span data-ttu-id="e8a62-139">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a62-139">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e8a62-140">匯入-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a62-140">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e8a62-141">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e8a62-141">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)