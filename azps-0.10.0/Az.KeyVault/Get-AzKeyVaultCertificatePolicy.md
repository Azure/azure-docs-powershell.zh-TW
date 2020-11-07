---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794674"
---
# <span data-ttu-id="22db2-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="22db2-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="22db2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22db2-102">SYNOPSIS</span></span>
<span data-ttu-id="22db2-103">在金鑰保存庫中取得憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="22db2-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="22db2-104">句法</span><span class="sxs-lookup"><span data-stu-id="22db2-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22db2-105">說明</span><span class="sxs-lookup"><span data-stu-id="22db2-105">DESCRIPTION</span></span>
<span data-ttu-id="22db2-106">**AzKeyVaultCertificatePolicy** Cmdlet 會取得 Azure 金鑰保存庫中金鑰保存庫中憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="22db2-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="22db2-107">示例</span><span class="sxs-lookup"><span data-stu-id="22db2-107">EXAMPLES</span></span>

### <span data-ttu-id="22db2-108">範例1：取得證書原則</span><span class="sxs-lookup"><span data-stu-id="22db2-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="22db2-109">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="22db2-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="22db2-110">參數</span><span class="sxs-lookup"><span data-stu-id="22db2-110">PARAMETERS</span></span>

### <span data-ttu-id="22db2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22db2-111">-DefaultProfile</span></span>
<span data-ttu-id="22db2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="22db2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22db2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="22db2-113">-Name</span></span>
<span data-ttu-id="22db2-114">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="22db2-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="22db2-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="22db2-115">-VaultName</span></span>
<span data-ttu-id="22db2-116">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="22db2-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="22db2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22db2-117">CommonParameters</span></span>
<span data-ttu-id="22db2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22db2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22db2-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22db2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22db2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="22db2-120">INPUTS</span></span>

### <span data-ttu-id="22db2-121">所有</span><span class="sxs-lookup"><span data-stu-id="22db2-121">None</span></span>
<span data-ttu-id="22db2-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="22db2-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22db2-123">輸出</span><span class="sxs-lookup"><span data-stu-id="22db2-123">OUTPUTS</span></span>

### <span data-ttu-id="22db2-124">KeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="22db2-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="22db2-125">筆記</span><span class="sxs-lookup"><span data-stu-id="22db2-125">NOTES</span></span>

## <span data-ttu-id="22db2-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="22db2-126">RELATED LINKS</span></span>

[<span data-ttu-id="22db2-127">新-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="22db2-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="22db2-128">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="22db2-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

