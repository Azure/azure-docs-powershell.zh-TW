---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794680"
---
# <span data-ttu-id="3c4d1-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c4d1-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3c4d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4d1-103">取得金鑰保存庫的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="3c4d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c4d1-104">SYNTAX</span></span>

### <span data-ttu-id="3c4d1-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="3c4d1-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c4d1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3c4d1-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c4d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="3c4d1-107">DESCRIPTION</span></span>
<span data-ttu-id="3c4d1-108">**AzKeyVaultCertificateIssuer** Cmdlet 會針對 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證頒發者或所有憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="3c4d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="3c4d1-109">EXAMPLES</span></span>

### <span data-ttu-id="3c4d1-110">範例1：取得憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="3c4d1-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="3c4d1-111">這個命令會取得名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="3c4d1-112">參數</span><span class="sxs-lookup"><span data-stu-id="3c4d1-112">PARAMETERS</span></span>

### <span data-ttu-id="3c4d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4d1-113">-DefaultProfile</span></span>
<span data-ttu-id="3c4d1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3c4d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c4d1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c4d1-115">-Name</span></span>
<span data-ttu-id="3c4d1-116">指定要取得的憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c4d1-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3c4d1-117">-VaultName</span></span>
<span data-ttu-id="3c4d1-118">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3c4d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4d1-119">CommonParameters</span></span>
<span data-ttu-id="3c4d1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4d1-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4d1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3c4d1-122">INPUTS</span></span>

### <span data-ttu-id="3c4d1-123">所有</span><span class="sxs-lookup"><span data-stu-id="3c4d1-123">None</span></span>
<span data-ttu-id="3c4d1-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3c4d1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c4d1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="3c4d1-125">OUTPUTS</span></span>

### <span data-ttu-id="3c4d1-126">KeyVault CertificateIssuerIdentityItem>，KeyVault...... KeyVaultCertificateIssuer<</span><span class="sxs-lookup"><span data-stu-id="3c4d1-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3c4d1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="3c4d1-127">NOTES</span></span>

## <span data-ttu-id="3c4d1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c4d1-128">RELATED LINKS</span></span>

[<span data-ttu-id="3c4d1-129">移除-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c4d1-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3c4d1-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3c4d1-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


