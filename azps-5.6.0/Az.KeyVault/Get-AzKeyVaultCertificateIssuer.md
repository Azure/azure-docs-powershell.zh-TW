---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d9d77eaac735044091aacbce6f92ee51be1210ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915461"
---
# <span data-ttu-id="6893f-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6893f-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6893f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6893f-102">SYNOPSIS</span></span>
<span data-ttu-id="6893f-103">獲得金鑰庫的憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="6893f-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="6893f-104">語法</span><span class="sxs-lookup"><span data-stu-id="6893f-104">SYNTAX</span></span>

### <span data-ttu-id="6893f-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6893f-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6893f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6893f-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6893f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6893f-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6893f-108">描述</span><span class="sxs-lookup"><span data-stu-id="6893f-108">DESCRIPTION</span></span>
<span data-ttu-id="6893f-109">**Get-AzKeyVaultCertificateIssulet Cmdlet** 會取得 Azure 金鑰庫金鑰庫的指定憑證發行者或所有憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="6893f-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6893f-110">例子</span><span class="sxs-lookup"><span data-stu-id="6893f-110">EXAMPLES</span></span>

### <span data-ttu-id="6893f-111">範例 1：取得憑證發行者</span><span class="sxs-lookup"><span data-stu-id="6893f-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="6893f-112">此命令會獲得名為 TestIssuer01 的憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="6893f-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="6893f-113">範例 2：使用篩選列出憑證發行者</span><span class="sxs-lookup"><span data-stu-id="6893f-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="6893f-114">此命令會獲得以「測試」為開始的憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="6893f-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="6893f-115">參數</span><span class="sxs-lookup"><span data-stu-id="6893f-115">PARAMETERS</span></span>

### <span data-ttu-id="6893f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6893f-116">-DefaultProfile</span></span>
<span data-ttu-id="6893f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6893f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6893f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6893f-118">-InputObject</span></span>
<span data-ttu-id="6893f-119">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="6893f-119">KeyVault object.</span></span>

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

### <span data-ttu-id="6893f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6893f-120">-Name</span></span>
<span data-ttu-id="6893f-121">指定要取得之憑證發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="6893f-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="6893f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6893f-122">-ResourceId</span></span>
<span data-ttu-id="6893f-123">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6893f-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="6893f-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6893f-124">-VaultName</span></span>
<span data-ttu-id="6893f-125">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6893f-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6893f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6893f-126">CommonParameters</span></span>
<span data-ttu-id="6893f-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6893f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6893f-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6893f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6893f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6893f-129">INPUTS</span></span>

### <span data-ttu-id="6893f-130">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6893f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6893f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6893f-131">System.String</span></span>

## <span data-ttu-id="6893f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6893f-132">OUTPUTS</span></span>

### <span data-ttu-id="6893f-133">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6893f-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="6893f-134">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6893f-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6893f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6893f-135">NOTES</span></span>

## <span data-ttu-id="6893f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6893f-136">RELATED LINKS</span></span>

[<span data-ttu-id="6893f-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6893f-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="6893f-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6893f-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


