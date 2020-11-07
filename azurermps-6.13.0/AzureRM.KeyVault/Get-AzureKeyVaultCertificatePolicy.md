---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 8d03d93a374f2184a995d9cbcdb83050aa98a8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625294"
---
# <span data-ttu-id="fb852-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb852-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fb852-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb852-102">SYNOPSIS</span></span>
<span data-ttu-id="fb852-103">在金鑰保存庫中取得憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="fb852-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb852-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb852-104">SYNTAX</span></span>

### <span data-ttu-id="fb852-105">VaultAndCertName (預設) </span><span class="sxs-lookup"><span data-stu-id="fb852-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb852-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fb852-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb852-107">說明</span><span class="sxs-lookup"><span data-stu-id="fb852-107">DESCRIPTION</span></span>
<span data-ttu-id="fb852-108">**AzureKeyVaultCertificatePolicy** Cmdlet 會取得 Azure 金鑰保存庫中金鑰保存庫中憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="fb852-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="fb852-109">示例</span><span class="sxs-lookup"><span data-stu-id="fb852-109">EXAMPLES</span></span>

### <span data-ttu-id="fb852-110">範例1：取得證書原則</span><span class="sxs-lookup"><span data-stu-id="fb852-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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

<span data-ttu-id="fb852-111">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="fb852-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="fb852-112">參數</span><span class="sxs-lookup"><span data-stu-id="fb852-112">PARAMETERS</span></span>

### <span data-ttu-id="fb852-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb852-113">-DefaultProfile</span></span>
<span data-ttu-id="fb852-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fb852-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb852-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb852-115">-InputObject</span></span>
<span data-ttu-id="fb852-116">[憑證] 物件。</span><span class="sxs-lookup"><span data-stu-id="fb852-116">Certificate Object.</span></span>

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

### <span data-ttu-id="fb852-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb852-117">-Name</span></span>
<span data-ttu-id="fb852-118">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb852-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="fb852-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fb852-119">-VaultName</span></span>
<span data-ttu-id="fb852-120">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb852-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fb852-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb852-121">CommonParameters</span></span>
<span data-ttu-id="fb852-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb852-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb852-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb852-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb852-124">輸入</span><span class="sxs-lookup"><span data-stu-id="fb852-124">INPUTS</span></span>

### <span data-ttu-id="fb852-125">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fb852-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="fb852-126">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fb852-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fb852-127">輸出</span><span class="sxs-lookup"><span data-stu-id="fb852-127">OUTPUTS</span></span>

### <span data-ttu-id="fb852-128">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fb852-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fb852-129">筆記</span><span class="sxs-lookup"><span data-stu-id="fb852-129">NOTES</span></span>

## <span data-ttu-id="fb852-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb852-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb852-131">新-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb852-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="fb852-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb852-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

