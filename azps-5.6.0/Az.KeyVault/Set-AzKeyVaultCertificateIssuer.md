---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 33c274154e122c0bb0925b8381d2dd51cad18264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904105"
---
# <span data-ttu-id="ff008-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ff008-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="ff008-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff008-102">SYNOPSIS</span></span>
<span data-ttu-id="ff008-103">在金鑰庫中設定憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="ff008-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="ff008-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff008-104">SYNTAX</span></span>

### <span data-ttu-id="ff008-105">展開 (預設) </span><span class="sxs-lookup"><span data-stu-id="ff008-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff008-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="ff008-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff008-107">描述</span><span class="sxs-lookup"><span data-stu-id="ff008-107">DESCRIPTION</span></span>
<span data-ttu-id="ff008-108">Cmdlet Set-AzKeyVaultCertificateIssuer在金鑰庫中設定憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="ff008-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="ff008-109">例子</span><span class="sxs-lookup"><span data-stu-id="ff008-109">EXAMPLES</span></span>

### <span data-ttu-id="ff008-110">範例 1：設定憑證發行者</span><span class="sxs-lookup"><span data-stu-id="ff008-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="ff008-111">此命令會設定憑證發行者的屬性。</span><span class="sxs-lookup"><span data-stu-id="ff008-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="ff008-112">參數</span><span class="sxs-lookup"><span data-stu-id="ff008-112">PARAMETERS</span></span>

### <span data-ttu-id="ff008-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ff008-113">-AccountId</span></span>
<span data-ttu-id="ff008-114">指定憑證發行者的帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff008-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="ff008-115">-ApiKey</span></span>
<span data-ttu-id="ff008-116">指定憑證發行者 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ff008-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff008-117">-DefaultProfile</span></span>
<span data-ttu-id="ff008-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ff008-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff008-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff008-119">-InputObject</span></span>
<span data-ttu-id="ff008-120">指定要設定憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="ff008-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="ff008-121">-IssuerProvider</span></span>
<span data-ttu-id="ff008-122">指定憑證發行者的類型。</span><span class="sxs-lookup"><span data-stu-id="ff008-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff008-123">-Name</span></span>
<span data-ttu-id="ff008-124">指定發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff008-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-125">-組織詳細資料</span><span class="sxs-lookup"><span data-stu-id="ff008-125">-OrganizationDetails</span></span>
<span data-ttu-id="ff008-126">要與發行者一起使用的組織詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ff008-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff008-127">-PassThru</span></span>
<span data-ttu-id="ff008-128">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ff008-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ff008-129">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ff008-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ff008-130">-VaultName</span></span>
<span data-ttu-id="ff008-131">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff008-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ff008-132">-Confirm</span></span>
<span data-ttu-id="ff008-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ff008-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff008-134">-WhatIf</span></span>
<span data-ttu-id="ff008-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff008-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff008-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff008-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff008-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff008-137">CommonParameters</span></span>
<span data-ttu-id="ff008-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff008-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff008-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff008-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff008-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ff008-140">INPUTS</span></span>

### <span data-ttu-id="ff008-141">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="ff008-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="ff008-142">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ff008-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="ff008-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ff008-143">OUTPUTS</span></span>

### <span data-ttu-id="ff008-144">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ff008-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ff008-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ff008-145">NOTES</span></span>

## <span data-ttu-id="ff008-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff008-146">RELATED LINKS</span></span>

[<span data-ttu-id="ff008-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ff008-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="ff008-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ff008-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

