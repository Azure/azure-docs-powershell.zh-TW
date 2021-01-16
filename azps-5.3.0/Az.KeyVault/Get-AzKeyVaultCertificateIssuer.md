---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438215"
---
# <span data-ttu-id="c3d08-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c3d08-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c3d08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3d08-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d08-103">取得金鑰保存庫的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="c3d08-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="c3d08-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3d08-104">SYNTAX</span></span>

### <span data-ttu-id="c3d08-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="c3d08-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d08-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3d08-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d08-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d08-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d08-108">說明</span><span class="sxs-lookup"><span data-stu-id="c3d08-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d08-109">**AzKeyVaultCertificateIssuer** Cmdlet 會針對 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證頒發者或所有憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="c3d08-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c3d08-110">示例</span><span class="sxs-lookup"><span data-stu-id="c3d08-110">EXAMPLES</span></span>

### <span data-ttu-id="c3d08-111">範例1：取得憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="c3d08-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="c3d08-112">這個命令會取得名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="c3d08-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="c3d08-113">範例2：使用篩選列出憑證頒發者</span><span class="sxs-lookup"><span data-stu-id="c3d08-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="c3d08-114">這個命令會取得以「test」開頭的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="c3d08-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="c3d08-115">參數</span><span class="sxs-lookup"><span data-stu-id="c3d08-115">PARAMETERS</span></span>

### <span data-ttu-id="c3d08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d08-116">-DefaultProfile</span></span>
<span data-ttu-id="c3d08-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c3d08-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3d08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d08-118">-InputObject</span></span>
<span data-ttu-id="c3d08-119">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="c3d08-119">KeyVault object.</span></span>

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

### <span data-ttu-id="c3d08-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3d08-120">-Name</span></span>
<span data-ttu-id="c3d08-121">指定要取得的憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="c3d08-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c3d08-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3d08-122">-ResourceId</span></span>
<span data-ttu-id="c3d08-123">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3d08-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="c3d08-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c3d08-124">-VaultName</span></span>
<span data-ttu-id="c3d08-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3d08-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c3d08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d08-126">CommonParameters</span></span>
<span data-ttu-id="c3d08-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3d08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d08-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3d08-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d08-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c3d08-129">INPUTS</span></span>

### <span data-ttu-id="c3d08-130">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c3d08-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c3d08-131">System.object</span><span class="sxs-lookup"><span data-stu-id="c3d08-131">System.String</span></span>

## <span data-ttu-id="c3d08-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c3d08-132">OUTPUTS</span></span>

### <span data-ttu-id="c3d08-133">PSKeyVaultCertificateIssuerIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c3d08-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="c3d08-134">PSKeyVaultCertificateIssuer 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c3d08-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c3d08-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c3d08-135">NOTES</span></span>

## <span data-ttu-id="c3d08-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3d08-136">RELATED LINKS</span></span>

[<span data-ttu-id="c3d08-137">移除-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c3d08-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="c3d08-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c3d08-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


