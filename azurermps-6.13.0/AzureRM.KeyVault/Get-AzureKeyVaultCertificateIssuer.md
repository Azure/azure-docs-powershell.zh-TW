---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625298"
---
# <span data-ttu-id="87cb8-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="87cb8-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="87cb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="87cb8-103">取得金鑰保存庫的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="87cb8-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87cb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="87cb8-104">SYNTAX</span></span>

### <span data-ttu-id="87cb8-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="87cb8-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cb8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="87cb8-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cb8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="87cb8-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87cb8-108">說明</span><span class="sxs-lookup"><span data-stu-id="87cb8-108">DESCRIPTION</span></span>
<span data-ttu-id="87cb8-109">**AzureKeyVaultCertificateIssuer** Cmdlet 會針對 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證頒發者或所有憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="87cb8-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="87cb8-110">示例</span><span class="sxs-lookup"><span data-stu-id="87cb8-110">EXAMPLES</span></span>

### <span data-ttu-id="87cb8-111">範例1：取得憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="87cb8-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="87cb8-112">這個命令會取得名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="87cb8-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="87cb8-113">參數</span><span class="sxs-lookup"><span data-stu-id="87cb8-113">PARAMETERS</span></span>

### <span data-ttu-id="87cb8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cb8-114">-DefaultProfile</span></span>
<span data-ttu-id="87cb8-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="87cb8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87cb8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87cb8-116">-InputObject</span></span>
<span data-ttu-id="87cb8-117">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="87cb8-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87cb8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="87cb8-118">-Name</span></span>
<span data-ttu-id="87cb8-119">指定要取得的憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="87cb8-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cb8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87cb8-120">-ResourceId</span></span>
<span data-ttu-id="87cb8-121">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="87cb8-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cb8-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="87cb8-122">-VaultName</span></span>
<span data-ttu-id="87cb8-123">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="87cb8-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cb8-124">CommonParameters</span></span>
<span data-ttu-id="87cb8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87cb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cb8-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87cb8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cb8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="87cb8-127">INPUTS</span></span>

### <span data-ttu-id="87cb8-128">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="87cb8-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="87cb8-129">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="87cb8-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="87cb8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="87cb8-130">System.String</span></span>

## <span data-ttu-id="87cb8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="87cb8-131">OUTPUTS</span></span>

### <span data-ttu-id="87cb8-132">PSKeyVaultCertificateIssuerIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="87cb8-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="87cb8-133">PSKeyVaultCertificateIssuer 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="87cb8-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="87cb8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="87cb8-134">NOTES</span></span>

## <span data-ttu-id="87cb8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="87cb8-135">RELATED LINKS</span></span>

[<span data-ttu-id="87cb8-136">移除-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="87cb8-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="87cb8-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="87cb8-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


