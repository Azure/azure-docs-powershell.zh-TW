---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6b8b4f07d4ac589a0bb700e6303c384e38966fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625999"
---
# <span data-ttu-id="63f13-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="63f13-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="63f13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="63f13-102">SYNOPSIS</span></span>
<span data-ttu-id="63f13-103">在金鑰保存庫中取得憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="63f13-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f13-104">句法</span><span class="sxs-lookup"><span data-stu-id="63f13-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f13-105">說明</span><span class="sxs-lookup"><span data-stu-id="63f13-105">DESCRIPTION</span></span>
<span data-ttu-id="63f13-106">**AzureKeyVaultCertificatePolicy** Cmdlet 會取得 Azure 金鑰保存庫中金鑰保存庫中憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="63f13-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="63f13-107">示例</span><span class="sxs-lookup"><span data-stu-id="63f13-107">EXAMPLES</span></span>

### <span data-ttu-id="63f13-108">範例1：取得證書原則</span><span class="sxs-lookup"><span data-stu-id="63f13-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="63f13-109">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="63f13-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="63f13-110">參數</span><span class="sxs-lookup"><span data-stu-id="63f13-110">PARAMETERS</span></span>

### <span data-ttu-id="63f13-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="63f13-111">-Name</span></span>
<span data-ttu-id="63f13-112">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="63f13-112">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="63f13-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="63f13-113">-VaultName</span></span>
<span data-ttu-id="63f13-114">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="63f13-114">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="63f13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f13-115">-DefaultProfile</span></span>
<span data-ttu-id="63f13-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="63f13-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63f13-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f13-117">CommonParameters</span></span>
<span data-ttu-id="63f13-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="63f13-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f13-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="63f13-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f13-120">輸入</span><span class="sxs-lookup"><span data-stu-id="63f13-120">INPUTS</span></span>

## <span data-ttu-id="63f13-121">輸出</span><span class="sxs-lookup"><span data-stu-id="63f13-121">OUTPUTS</span></span>

### <span data-ttu-id="63f13-122">KeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="63f13-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="63f13-123">筆記</span><span class="sxs-lookup"><span data-stu-id="63f13-123">NOTES</span></span>

## <span data-ttu-id="63f13-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="63f13-124">RELATED LINKS</span></span>

[<span data-ttu-id="63f13-125">新-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="63f13-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="63f13-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="63f13-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

