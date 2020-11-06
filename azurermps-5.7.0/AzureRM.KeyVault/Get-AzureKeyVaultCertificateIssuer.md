---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447788"
---
# <span data-ttu-id="eafe5-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="eafe5-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="eafe5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eafe5-102">SYNOPSIS</span></span>
<span data-ttu-id="eafe5-103">取得金鑰保存庫的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="eafe5-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafe5-104">句法</span><span class="sxs-lookup"><span data-stu-id="eafe5-104">SYNTAX</span></span>

### <span data-ttu-id="eafe5-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="eafe5-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eafe5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eafe5-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eafe5-107">說明</span><span class="sxs-lookup"><span data-stu-id="eafe5-107">DESCRIPTION</span></span>
<span data-ttu-id="eafe5-108">**AzureKeyVaultCertificateIssuer** Cmdlet 會針對 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證頒發者或所有憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="eafe5-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="eafe5-109">示例</span><span class="sxs-lookup"><span data-stu-id="eafe5-109">EXAMPLES</span></span>

### <span data-ttu-id="eafe5-110">範例1：取得憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="eafe5-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="eafe5-111">這個命令會取得名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="eafe5-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="eafe5-112">參數</span><span class="sxs-lookup"><span data-stu-id="eafe5-112">PARAMETERS</span></span>

### <span data-ttu-id="eafe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafe5-113">-DefaultProfile</span></span>
<span data-ttu-id="eafe5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eafe5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eafe5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eafe5-115">-InputObject</span></span>
<span data-ttu-id="eafe5-116">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="eafe5-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eafe5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="eafe5-117">-Name</span></span>
<span data-ttu-id="eafe5-118">指定要取得的憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="eafe5-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eafe5-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eafe5-119">-VaultName</span></span>
<span data-ttu-id="eafe5-120">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="eafe5-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eafe5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafe5-121">CommonParameters</span></span>
<span data-ttu-id="eafe5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eafe5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafe5-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eafe5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafe5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="eafe5-124">INPUTS</span></span>

### <span data-ttu-id="eafe5-125">所有</span><span class="sxs-lookup"><span data-stu-id="eafe5-125">None</span></span>
<span data-ttu-id="eafe5-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="eafe5-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eafe5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="eafe5-127">OUTPUTS</span></span>

### <span data-ttu-id="eafe5-128">KeyVault PSKeyVaultCertificateIssuerIdentityItem>，KeyVault...... PSKeyVaultCertificateIssuer<</span><span class="sxs-lookup"><span data-stu-id="eafe5-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="eafe5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="eafe5-129">NOTES</span></span>

## <span data-ttu-id="eafe5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="eafe5-130">RELATED LINKS</span></span>

[<span data-ttu-id="eafe5-131">移除-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="eafe5-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="eafe5-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="eafe5-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


