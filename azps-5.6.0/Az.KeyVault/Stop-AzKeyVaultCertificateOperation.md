---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: c5b5b924968d444890338d8110f0a9cb9e416253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916941"
---
# <span data-ttu-id="2a07b-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2a07b-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="2a07b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2a07b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a07b-103">取消金鑰庫中的憑證作業。</span><span class="sxs-lookup"><span data-stu-id="2a07b-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="2a07b-104">語法</span><span class="sxs-lookup"><span data-stu-id="2a07b-104">SYNTAX</span></span>

### <span data-ttu-id="2a07b-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="2a07b-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a07b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a07b-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a07b-107">描述</span><span class="sxs-lookup"><span data-stu-id="2a07b-107">DESCRIPTION</span></span>
<span data-ttu-id="2a07b-108">**Stop-AzKeyVaultCertificateOperation Cmdlet** 會取消 Azure 金鑰庫服務中的憑證作業。</span><span class="sxs-lookup"><span data-stu-id="2a07b-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="2a07b-109">例子</span><span class="sxs-lookup"><span data-stu-id="2a07b-109">EXAMPLES</span></span>

### <span data-ttu-id="2a07b-110">範例 1：取消憑證作業</span><span class="sxs-lookup"><span data-stu-id="2a07b-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

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

<span data-ttu-id="2a07b-111">此命令會取消 TestCert02 憑證作業。</span><span class="sxs-lookup"><span data-stu-id="2a07b-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="2a07b-112">參數</span><span class="sxs-lookup"><span data-stu-id="2a07b-112">PARAMETERS</span></span>

### <span data-ttu-id="2a07b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a07b-113">-DefaultProfile</span></span>
<span data-ttu-id="2a07b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2a07b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a07b-115">-強制</span><span class="sxs-lookup"><span data-stu-id="2a07b-115">-Force</span></span>
<span data-ttu-id="2a07b-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2a07b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a07b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a07b-117">-InputObject</span></span>
<span data-ttu-id="2a07b-118">運算物件</span><span class="sxs-lookup"><span data-stu-id="2a07b-118">Operation object</span></span>

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

### <span data-ttu-id="2a07b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a07b-119">-Name</span></span>
<span data-ttu-id="2a07b-120">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a07b-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="2a07b-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2a07b-121">-VaultName</span></span>
<span data-ttu-id="2a07b-122">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a07b-122">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="2a07b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2a07b-123">-Confirm</span></span>
<span data-ttu-id="2a07b-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2a07b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a07b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a07b-125">-WhatIf</span></span>
<span data-ttu-id="2a07b-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a07b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a07b-127">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a07b-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a07b-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a07b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a07b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a07b-129">CommonParameters</span></span>
<span data-ttu-id="2a07b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2a07b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a07b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a07b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a07b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2a07b-132">INPUTS</span></span>

### <span data-ttu-id="2a07b-133">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2a07b-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="2a07b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2a07b-134">OUTPUTS</span></span>

### <span data-ttu-id="2a07b-135">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2a07b-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="2a07b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2a07b-136">NOTES</span></span>

## <span data-ttu-id="2a07b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a07b-137">RELATED LINKS</span></span>

[<span data-ttu-id="2a07b-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2a07b-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="2a07b-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2a07b-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

