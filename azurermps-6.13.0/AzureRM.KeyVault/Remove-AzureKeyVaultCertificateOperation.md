---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 9bd02d11f0d8c6f60638b506fd09c953bc861b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449795"
---
# <span data-ttu-id="7d142-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d142-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d142-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d142-102">SYNOPSIS</span></span>
<span data-ttu-id="7d142-103">從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="7d142-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d142-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d142-104">SYNTAX</span></span>

### <span data-ttu-id="7d142-105">設置</span><span class="sxs-lookup"><span data-stu-id="7d142-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d142-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7d142-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d142-107">說明</span><span class="sxs-lookup"><span data-stu-id="7d142-107">DESCRIPTION</span></span>
<span data-ttu-id="7d142-108">**AzureKeyVaultCertificateOperation** Cmdlet 會從金鑰保存庫刪除憑證操作。</span><span class="sxs-lookup"><span data-stu-id="7d142-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="7d142-109">示例</span><span class="sxs-lookup"><span data-stu-id="7d142-109">EXAMPLES</span></span>

### <span data-ttu-id="7d142-110">範例1：移除憑證操作</span><span class="sxs-lookup"><span data-stu-id="7d142-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

Id                        : https://contosokv01.vault.azure.net/certificates/testcert01/pending
Status                    : completed
StatusDetails             :
RequestId                 : f5dfd2ae486149a594dc98e800dceaaa
Target                    : https://contosokv01.vault.azure.net/certificates/testcert01
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
                            ==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="7d142-111">這個命令會從 ContosoKV01 金鑰保存庫中移除名為 TestCert01 的憑證操作，而不需確認。</span><span class="sxs-lookup"><span data-stu-id="7d142-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="7d142-112">參數</span><span class="sxs-lookup"><span data-stu-id="7d142-112">PARAMETERS</span></span>

### <span data-ttu-id="7d142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d142-113">-DefaultProfile</span></span>
<span data-ttu-id="7d142-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7d142-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d142-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7d142-115">-Force</span></span>
<span data-ttu-id="7d142-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7d142-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d142-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d142-117">-InputObject</span></span>
<span data-ttu-id="7d142-118">Operation 物件</span><span class="sxs-lookup"><span data-stu-id="7d142-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d142-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d142-119">-Name</span></span>
<span data-ttu-id="7d142-120">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d142-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d142-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d142-121">-PassThru</span></span>
<span data-ttu-id="7d142-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7d142-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7d142-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7d142-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d142-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7d142-124">-VaultName</span></span>
<span data-ttu-id="7d142-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d142-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d142-126">-確認</span><span class="sxs-lookup"><span data-stu-id="7d142-126">-Confirm</span></span>
<span data-ttu-id="7d142-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d142-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d142-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d142-128">-WhatIf</span></span>
<span data-ttu-id="7d142-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d142-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d142-130">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d142-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d142-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d142-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d142-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d142-132">CommonParameters</span></span>
<span data-ttu-id="7d142-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d142-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d142-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d142-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d142-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7d142-135">INPUTS</span></span>

### <span data-ttu-id="7d142-136">PSKeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="7d142-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>
<span data-ttu-id="7d142-137">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="7d142-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7d142-138">輸出</span><span class="sxs-lookup"><span data-stu-id="7d142-138">OUTPUTS</span></span>

### <span data-ttu-id="7d142-139">PSKeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="7d142-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7d142-140">筆記</span><span class="sxs-lookup"><span data-stu-id="7d142-140">NOTES</span></span>

## <span data-ttu-id="7d142-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d142-141">RELATED LINKS</span></span>

[<span data-ttu-id="7d142-142">AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d142-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="7d142-143">停止 AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7d142-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

