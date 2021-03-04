---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: cace261f300dc63b9568413fb8a709c323349531
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911949"
---
# <span data-ttu-id="0beb9-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0beb9-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0beb9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0beb9-102">SYNOPSIS</span></span>
<span data-ttu-id="0beb9-103">在金鑰庫中獲取憑證的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="0beb9-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="0beb9-104">語法</span><span class="sxs-lookup"><span data-stu-id="0beb9-104">SYNTAX</span></span>

### <span data-ttu-id="0beb9-105">VaultAndCertName (預設) </span><span class="sxs-lookup"><span data-stu-id="0beb9-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0beb9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0beb9-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0beb9-107">描述</span><span class="sxs-lookup"><span data-stu-id="0beb9-107">DESCRIPTION</span></span>
<span data-ttu-id="0beb9-108">**Get-AzKeyVaultCertificatePolidlet** 會取得 Azure 金鑰庫金鑰庫中憑證的憑證之策略。</span><span class="sxs-lookup"><span data-stu-id="0beb9-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0beb9-109">例子</span><span class="sxs-lookup"><span data-stu-id="0beb9-109">EXAMPLES</span></span>

### <span data-ttu-id="0beb9-110">範例 1：取得憑證策略</span><span class="sxs-lookup"><span data-stu-id="0beb9-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="0beb9-111">此命令會獲得 ContosoKV01 金鑰庫中 TestCert01 憑證的憑證策略。</span><span class="sxs-lookup"><span data-stu-id="0beb9-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="0beb9-112">參數</span><span class="sxs-lookup"><span data-stu-id="0beb9-112">PARAMETERS</span></span>

### <span data-ttu-id="0beb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0beb9-113">-DefaultProfile</span></span>
<span data-ttu-id="0beb9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0beb9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0beb9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0beb9-115">-InputObject</span></span>
<span data-ttu-id="0beb9-116">憑證物件。</span><span class="sxs-lookup"><span data-stu-id="0beb9-116">Certificate Object.</span></span>

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

### <span data-ttu-id="0beb9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0beb9-117">-Name</span></span>
<span data-ttu-id="0beb9-118">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="0beb9-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="0beb9-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0beb9-119">-VaultName</span></span>
<span data-ttu-id="0beb9-120">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0beb9-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="0beb9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0beb9-121">CommonParameters</span></span>
<span data-ttu-id="0beb9-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0beb9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0beb9-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0beb9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0beb9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0beb9-124">INPUTS</span></span>

### <span data-ttu-id="0beb9-125">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0beb9-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="0beb9-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0beb9-126">OUTPUTS</span></span>

### <span data-ttu-id="0beb9-127">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0beb9-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0beb9-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0beb9-128">NOTES</span></span>

## <span data-ttu-id="0beb9-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0beb9-129">RELATED LINKS</span></span>

[<span data-ttu-id="0beb9-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0beb9-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0beb9-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0beb9-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

