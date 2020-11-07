---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956634"
---
# <span data-ttu-id="c3ded-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c3ded-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c3ded-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3ded-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ded-103">在金鑰保存庫中取得憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="c3ded-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="c3ded-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3ded-104">SYNTAX</span></span>

### <span data-ttu-id="c3ded-105">VaultAndCertName (預設) </span><span class="sxs-lookup"><span data-stu-id="c3ded-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3ded-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c3ded-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3ded-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3ded-107">DESCRIPTION</span></span>
<span data-ttu-id="c3ded-108">**AzKeyVaultCertificatePolicy** Cmdlet 會取得 Azure 金鑰保存庫中金鑰保存庫中憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="c3ded-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c3ded-109">示例</span><span class="sxs-lookup"><span data-stu-id="c3ded-109">EXAMPLES</span></span>

### <span data-ttu-id="c3ded-110">範例1：取得證書原則</span><span class="sxs-lookup"><span data-stu-id="c3ded-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="c3ded-111">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="c3ded-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c3ded-112">參數</span><span class="sxs-lookup"><span data-stu-id="c3ded-112">PARAMETERS</span></span>

### <span data-ttu-id="c3ded-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ded-113">-DefaultProfile</span></span>
<span data-ttu-id="c3ded-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c3ded-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3ded-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3ded-115">-InputObject</span></span>
<span data-ttu-id="c3ded-116">[憑證] 物件。</span><span class="sxs-lookup"><span data-stu-id="c3ded-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ded-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3ded-117">-Name</span></span>
<span data-ttu-id="c3ded-118">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ded-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ded-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c3ded-119">-VaultName</span></span>
<span data-ttu-id="c3ded-120">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ded-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ded-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ded-121">CommonParameters</span></span>
<span data-ttu-id="c3ded-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3ded-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ded-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3ded-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ded-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c3ded-124">INPUTS</span></span>

### <span data-ttu-id="c3ded-125">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c3ded-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c3ded-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c3ded-126">OUTPUTS</span></span>

### <span data-ttu-id="c3ded-127">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c3ded-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c3ded-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c3ded-128">NOTES</span></span>

## <span data-ttu-id="c3ded-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3ded-129">RELATED LINKS</span></span>

[<span data-ttu-id="c3ded-130">新-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c3ded-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c3ded-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c3ded-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

