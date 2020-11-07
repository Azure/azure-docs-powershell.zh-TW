---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801330"
---
# <span data-ttu-id="d3640-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d3640-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d3640-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3640-102">SYNOPSIS</span></span>
<span data-ttu-id="d3640-103">取得金鑰保存庫的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="d3640-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3640-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3640-104">SYNTAX</span></span>

### <span data-ttu-id="d3640-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="d3640-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3640-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d3640-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3640-107">說明</span><span class="sxs-lookup"><span data-stu-id="d3640-107">DESCRIPTION</span></span>
<span data-ttu-id="d3640-108">**AzureKeyVaultCertificateIssuer** Cmdlet 會針對 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證頒發者或所有憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="d3640-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d3640-109">示例</span><span class="sxs-lookup"><span data-stu-id="d3640-109">EXAMPLES</span></span>

### <span data-ttu-id="d3640-110">範例1：取得憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="d3640-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="d3640-111">這個命令會取得名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="d3640-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="d3640-112">參數</span><span class="sxs-lookup"><span data-stu-id="d3640-112">PARAMETERS</span></span>

### <span data-ttu-id="d3640-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3640-113">-DefaultProfile</span></span>
<span data-ttu-id="d3640-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d3640-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3640-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3640-115">-Name</span></span>
<span data-ttu-id="d3640-116">指定要取得的憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="d3640-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="d3640-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d3640-117">-VaultName</span></span>
<span data-ttu-id="d3640-118">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3640-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d3640-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3640-119">CommonParameters</span></span>
<span data-ttu-id="d3640-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3640-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3640-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3640-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3640-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d3640-122">INPUTS</span></span>

## <span data-ttu-id="d3640-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d3640-123">OUTPUTS</span></span>

### <span data-ttu-id="d3640-124">KeyVault CertificateIssuerIdentityItem>，KeyVault...... KeyVaultCertificateIssuer<</span><span class="sxs-lookup"><span data-stu-id="d3640-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d3640-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d3640-125">NOTES</span></span>

## <span data-ttu-id="d3640-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3640-126">RELATED LINKS</span></span>

[<span data-ttu-id="d3640-127">移除-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d3640-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="d3640-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d3640-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


