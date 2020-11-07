---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/stop-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7018dc8d6951be8d1a08f4f1d1f5d615810dafab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800945"
---
# <span data-ttu-id="57c6c-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="57c6c-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="57c6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="57c6c-103">在金鑰保存庫中取消憑證操作。</span><span class="sxs-lookup"><span data-stu-id="57c6c-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57c6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="57c6c-104">SYNTAX</span></span>

```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57c6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="57c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="57c6c-106">**AzureKeyVaultCertificateOperation** Cmdlet 會取消 Azure 金鑰保存庫服務中的憑證操作。</span><span class="sxs-lookup"><span data-stu-id="57c6c-106">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="57c6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="57c6c-107">EXAMPLES</span></span>

### <span data-ttu-id="57c6c-108">範例1：取消憑證操作</span><span class="sxs-lookup"><span data-stu-id="57c6c-108">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzureKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
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

<span data-ttu-id="57c6c-109">這個命令會取消 TestCert02 憑證操作。</span><span class="sxs-lookup"><span data-stu-id="57c6c-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="57c6c-110">參數</span><span class="sxs-lookup"><span data-stu-id="57c6c-110">PARAMETERS</span></span>

### <span data-ttu-id="57c6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c6c-111">-DefaultProfile</span></span>
<span data-ttu-id="57c6c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="57c6c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57c6c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="57c6c-113">-Force</span></span>
<span data-ttu-id="57c6c-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="57c6c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57c6c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="57c6c-115">-Name</span></span>
<span data-ttu-id="57c6c-116">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="57c6c-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="57c6c-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="57c6c-117">-VaultName</span></span>
<span data-ttu-id="57c6c-118">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="57c6c-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="57c6c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="57c6c-119">-Confirm</span></span>
<span data-ttu-id="57c6c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57c6c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c6c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c6c-121">-WhatIf</span></span>
<span data-ttu-id="57c6c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57c6c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c6c-123">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57c6c-123">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c6c-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57c6c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c6c-125">CommonParameters</span></span>
<span data-ttu-id="57c6c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57c6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c6c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57c6c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c6c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="57c6c-128">INPUTS</span></span>

## <span data-ttu-id="57c6c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="57c6c-129">OUTPUTS</span></span>

### <span data-ttu-id="57c6c-130">KeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="57c6c-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="57c6c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="57c6c-131">NOTES</span></span>

## <span data-ttu-id="57c6c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="57c6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="57c6c-133">AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="57c6c-133">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="57c6c-134">移除-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="57c6c-134">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

