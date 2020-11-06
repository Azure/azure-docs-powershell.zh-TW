---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454375"
---
# <span data-ttu-id="3dd7d-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3dd7d-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3dd7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd7d-103">取得金鑰保存庫的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dd7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dd7d-104">SYNTAX</span></span>

### <span data-ttu-id="3dd7d-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="3dd7d-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3dd7d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3dd7d-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dd7d-107">說明</span><span class="sxs-lookup"><span data-stu-id="3dd7d-107">DESCRIPTION</span></span>
<span data-ttu-id="3dd7d-108">**AzureKeyVaultCertificateIssuer** Cmdlet 會針對 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證頒發者或所有憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="3dd7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="3dd7d-109">EXAMPLES</span></span>

### <span data-ttu-id="3dd7d-110">範例1：取得憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="3dd7d-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="3dd7d-111">這個命令會取得名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="3dd7d-112">參數</span><span class="sxs-lookup"><span data-stu-id="3dd7d-112">PARAMETERS</span></span>

### <span data-ttu-id="3dd7d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3dd7d-113">-Name</span></span>
<span data-ttu-id="3dd7d-114">指定要取得的憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd7d-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3dd7d-115">-VaultName</span></span>
<span data-ttu-id="3dd7d-116">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3dd7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd7d-117">-DefaultProfile</span></span>
<span data-ttu-id="3dd7d-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd7d-119">CommonParameters</span></span>
<span data-ttu-id="3dd7d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd7d-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dd7d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd7d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3dd7d-122">INPUTS</span></span>

## <span data-ttu-id="3dd7d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3dd7d-123">OUTPUTS</span></span>

### <span data-ttu-id="3dd7d-124">KeyVault CertificateIssuerIdentityItem>，KeyVault...... KeyVaultCertificateIssuer<</span><span class="sxs-lookup"><span data-stu-id="3dd7d-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3dd7d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3dd7d-125">NOTES</span></span>

## <span data-ttu-id="3dd7d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dd7d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3dd7d-127">移除-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3dd7d-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3dd7d-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3dd7d-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


