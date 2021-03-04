---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
ms.openlocfilehash: 9aedcab47f98b82e707d907bcf8a1706bdeabf11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910489"
---
# <span data-ttu-id="793d3-101">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="793d3-101">Add-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="793d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="793d3-102">SYNOPSIS</span></span>
<span data-ttu-id="793d3-103">將憑證新增到金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="793d3-103">Adds a certificate to a key vault.</span></span>

## <span data-ttu-id="793d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="793d3-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificatePolicy] <PSKeyVaultCertificatePolicy> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="793d3-105">描述</span><span class="sxs-lookup"><span data-stu-id="793d3-105">DESCRIPTION</span></span>
<span data-ttu-id="793d3-106">**Add-AzKeyVaultCertificate Cmdlet** 會啟動在 Azure 金鑰庫金鑰庫註冊憑證的過程。</span><span class="sxs-lookup"><span data-stu-id="793d3-106">The **Add-AzKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="793d3-107">例子</span><span class="sxs-lookup"><span data-stu-id="793d3-107">EXAMPLES</span></span>

### <span data-ttu-id="793d3-108">範例 1：新增憑證</span><span class="sxs-lookup"><span data-stu-id="793d3-108">Example 1: Add a certificate</span></span>
```powershell
PS C:\> $Policy = New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

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

PS C:\> Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"

Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="793d3-109">第一個命令使用 New-AzKeyVaultCertificatePolicy Cmdlet 建立憑證策略，然後將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="793d3-109">The first command uses the New-AzKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>
<span data-ttu-id="793d3-110">第二個命令使用 **Add-AzKeyVaultCertificate** 來啟動建立憑證的過程。</span><span class="sxs-lookup"><span data-stu-id="793d3-110">The second command uses **Add-AzKeyVaultCertificate** to start the process to create a certificate.</span></span>
<span data-ttu-id="793d3-111">第三個命令Get-AzKeyVaultCertificateOperation Cmdlet 來輪詢作業，以確認作業已完成。</span><span class="sxs-lookup"><span data-stu-id="793d3-111">The third command uses the Get-AzKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>
<span data-ttu-id="793d3-112">最後一個命令會使用 Get-AzKeyVaultCertificate Cmdlet 取得憑證。</span><span class="sxs-lookup"><span data-stu-id="793d3-112">The final command uses the Get-AzKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="793d3-113">參數</span><span class="sxs-lookup"><span data-stu-id="793d3-113">PARAMETERS</span></span>

### <span data-ttu-id="793d3-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="793d3-114">-CertificatePolicy</span></span>
<span data-ttu-id="793d3-115">指定 **KeyVaultCertificatePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="793d3-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="793d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793d3-116">-DefaultProfile</span></span>
<span data-ttu-id="793d3-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="793d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="793d3-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="793d3-118">-Name</span></span>
<span data-ttu-id="793d3-119">指定要新增的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="793d3-119">Specifies the name of the certificate to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793d3-120">-標記</span><span class="sxs-lookup"><span data-stu-id="793d3-120">-Tag</span></span>
<span data-ttu-id="793d3-121">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="793d3-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="793d3-122">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="793d3-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793d3-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="793d3-123">-VaultName</span></span>
<span data-ttu-id="793d3-124">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="793d3-124">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793d3-125">-確認</span><span class="sxs-lookup"><span data-stu-id="793d3-125">-Confirm</span></span>
<span data-ttu-id="793d3-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="793d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="793d3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="793d3-127">-WhatIf</span></span>
<span data-ttu-id="793d3-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="793d3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="793d3-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="793d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="793d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793d3-130">CommonParameters</span></span>
<span data-ttu-id="793d3-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="793d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793d3-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="793d3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793d3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="793d3-133">INPUTS</span></span>

### <span data-ttu-id="793d3-134">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="793d3-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="793d3-135">輸出</span><span class="sxs-lookup"><span data-stu-id="793d3-135">OUTPUTS</span></span>

### <span data-ttu-id="793d3-136">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="793d3-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="793d3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="793d3-137">NOTES</span></span>

## <span data-ttu-id="793d3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="793d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="793d3-139">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="793d3-139">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="793d3-140">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="793d3-140">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="793d3-141">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="793d3-141">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
