---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/stop-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: e1a4efc9709b7168e5de46ea0e19e2059f15243c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795526"
---
# <span data-ttu-id="6734d-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6734d-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="6734d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6734d-102">SYNOPSIS</span></span>
<span data-ttu-id="6734d-103">在金鑰保存庫中取消憑證操作。</span><span class="sxs-lookup"><span data-stu-id="6734d-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="6734d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6734d-104">SYNTAX</span></span>

```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6734d-105">說明</span><span class="sxs-lookup"><span data-stu-id="6734d-105">DESCRIPTION</span></span>
<span data-ttu-id="6734d-106">**AzKeyVaultCertificateOperation** Cmdlet 會取消 Azure 金鑰保存庫服務中的憑證操作。</span><span class="sxs-lookup"><span data-stu-id="6734d-106">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="6734d-107">示例</span><span class="sxs-lookup"><span data-stu-id="6734d-107">EXAMPLES</span></span>

### <span data-ttu-id="6734d-108">範例1：取消憑證操作</span><span class="sxs-lookup"><span data-stu-id="6734d-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="6734d-109">這個命令會取消 TestCert02 憑證操作。</span><span class="sxs-lookup"><span data-stu-id="6734d-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="6734d-110">參數</span><span class="sxs-lookup"><span data-stu-id="6734d-110">PARAMETERS</span></span>

### <span data-ttu-id="6734d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6734d-111">-DefaultProfile</span></span>
<span data-ttu-id="6734d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6734d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6734d-113">-Force</span></span>
<span data-ttu-id="6734d-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6734d-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6734d-115">-Name</span></span>
<span data-ttu-id="6734d-116">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="6734d-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6734d-117">-VaultName</span></span>
<span data-ttu-id="6734d-118">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6734d-118">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6734d-119">-Confirm</span></span>
<span data-ttu-id="6734d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6734d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6734d-121">-WhatIf</span></span>
<span data-ttu-id="6734d-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6734d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6734d-123">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6734d-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6734d-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6734d-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6734d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6734d-125">CommonParameters</span></span>
<span data-ttu-id="6734d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6734d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6734d-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6734d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6734d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="6734d-128">INPUTS</span></span>

### <span data-ttu-id="6734d-129">所有</span><span class="sxs-lookup"><span data-stu-id="6734d-129">None</span></span>
<span data-ttu-id="6734d-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6734d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6734d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6734d-131">OUTPUTS</span></span>

### <span data-ttu-id="6734d-132">KeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="6734d-132">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="6734d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6734d-133">NOTES</span></span>

## <span data-ttu-id="6734d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6734d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6734d-135">AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6734d-135">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="6734d-136">移除-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6734d-136">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

