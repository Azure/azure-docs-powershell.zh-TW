---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 1504d4f18c8ab3baee000c2cf8d873df1dd9a177
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141673"
---
# <span data-ttu-id="9a655-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9a655-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9a655-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a655-102">SYNOPSIS</span></span>
<span data-ttu-id="9a655-103">取得金鑰保存庫的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="9a655-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="9a655-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a655-104">SYNTAX</span></span>

### <span data-ttu-id="9a655-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="9a655-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a655-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a655-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a655-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a655-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a655-108">說明</span><span class="sxs-lookup"><span data-stu-id="9a655-108">DESCRIPTION</span></span>
<span data-ttu-id="9a655-109">**AzKeyVaultCertificateIssuer** Cmdlet 會針對 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證頒發者或所有憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="9a655-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="9a655-110">示例</span><span class="sxs-lookup"><span data-stu-id="9a655-110">EXAMPLES</span></span>

### <span data-ttu-id="9a655-111">範例1：取得憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="9a655-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="9a655-112">這個命令會取得名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="9a655-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="9a655-113">範例2：使用篩選列出憑證頒發者</span><span class="sxs-lookup"><span data-stu-id="9a655-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="9a655-114">這個命令會取得以「test」開頭的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="9a655-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="9a655-115">參數</span><span class="sxs-lookup"><span data-stu-id="9a655-115">PARAMETERS</span></span>

### <span data-ttu-id="9a655-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a655-116">-DefaultProfile</span></span>
<span data-ttu-id="9a655-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9a655-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a655-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a655-118">-InputObject</span></span>
<span data-ttu-id="9a655-119">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="9a655-119">KeyVault object.</span></span>

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

### <span data-ttu-id="9a655-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a655-120">-Name</span></span>
<span data-ttu-id="9a655-121">指定要取得的憑證頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="9a655-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="9a655-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a655-122">-ResourceId</span></span>
<span data-ttu-id="9a655-123">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a655-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="9a655-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9a655-124">-VaultName</span></span>
<span data-ttu-id="9a655-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a655-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9a655-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a655-126">CommonParameters</span></span>
<span data-ttu-id="9a655-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a655-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a655-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9a655-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a655-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9a655-129">INPUTS</span></span>

### <span data-ttu-id="9a655-130">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="9a655-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9a655-131">System.object</span><span class="sxs-lookup"><span data-stu-id="9a655-131">System.String</span></span>

## <span data-ttu-id="9a655-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9a655-132">OUTPUTS</span></span>

### <span data-ttu-id="9a655-133">PSKeyVaultCertificateIssuerIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="9a655-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="9a655-134">PSKeyVaultCertificateIssuer 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="9a655-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9a655-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9a655-135">NOTES</span></span>

## <span data-ttu-id="9a655-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a655-136">RELATED LINKS</span></span>

[<span data-ttu-id="9a655-137">移除-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9a655-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9a655-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9a655-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


