---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140491"
---
# <span data-ttu-id="815c4-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="815c4-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="815c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="815c4-102">SYNOPSIS</span></span>
<span data-ttu-id="815c4-103">在金鑰保存庫中設定憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="815c4-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="815c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="815c4-104">SYNTAX</span></span>

### <span data-ttu-id="815c4-105">展開 (預設) </span><span class="sxs-lookup"><span data-stu-id="815c4-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="815c4-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="815c4-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="815c4-107">說明</span><span class="sxs-lookup"><span data-stu-id="815c4-107">DESCRIPTION</span></span>
<span data-ttu-id="815c4-108">Set-AzKeyVaultCertificateIssuer Cmdlet 會在金鑰保存庫中設定憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="815c4-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="815c4-109">示例</span><span class="sxs-lookup"><span data-stu-id="815c4-109">EXAMPLES</span></span>

### <span data-ttu-id="815c4-110">範例1：設定憑證簽發者</span><span class="sxs-lookup"><span data-stu-id="815c4-110">Example 1: Set a certificate issuer</span></span>
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

<span data-ttu-id="815c4-111">這個命令會設定憑證簽發者的屬性。</span><span class="sxs-lookup"><span data-stu-id="815c4-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="815c4-112">參數</span><span class="sxs-lookup"><span data-stu-id="815c4-112">PARAMETERS</span></span>

### <span data-ttu-id="815c4-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="815c4-113">-AccountId</span></span>
<span data-ttu-id="815c4-114">指定憑證簽發者的帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="815c4-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="815c4-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="815c4-115">-ApiKey</span></span>
<span data-ttu-id="815c4-116">指定憑證簽發者的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="815c4-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="815c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815c4-117">-DefaultProfile</span></span>
<span data-ttu-id="815c4-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="815c4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="815c4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="815c4-119">-InputObject</span></span>
<span data-ttu-id="815c4-120">指定要設定的憑證頒發者。</span><span class="sxs-lookup"><span data-stu-id="815c4-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="815c4-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="815c4-121">-IssuerProvider</span></span>
<span data-ttu-id="815c4-122">指定憑證頒發者的類型。</span><span class="sxs-lookup"><span data-stu-id="815c4-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="815c4-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="815c4-123">-Name</span></span>
<span data-ttu-id="815c4-124">指定頒發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="815c4-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="815c4-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="815c4-125">-OrganizationDetails</span></span>
<span data-ttu-id="815c4-126">要與頒發者搭配使用的組織詳細資料。</span><span class="sxs-lookup"><span data-stu-id="815c4-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="815c4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="815c4-127">-PassThru</span></span>
<span data-ttu-id="815c4-128">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="815c4-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="815c4-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="815c4-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="815c4-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="815c4-130">-VaultName</span></span>
<span data-ttu-id="815c4-131">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="815c4-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="815c4-132">-確認</span><span class="sxs-lookup"><span data-stu-id="815c4-132">-Confirm</span></span>
<span data-ttu-id="815c4-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="815c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="815c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815c4-134">-WhatIf</span></span>
<span data-ttu-id="815c4-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="815c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="815c4-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="815c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="815c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815c4-137">CommonParameters</span></span>
<span data-ttu-id="815c4-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="815c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815c4-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="815c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815c4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="815c4-140">INPUTS</span></span>

### <span data-ttu-id="815c4-141">PSKeyVaultCertificateOrganizationDetails 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="815c4-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="815c4-142">PSKeyVaultCertificateIssuerIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="815c4-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="815c4-143">輸出</span><span class="sxs-lookup"><span data-stu-id="815c4-143">OUTPUTS</span></span>

### <span data-ttu-id="815c4-144">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="815c4-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="815c4-145">筆記</span><span class="sxs-lookup"><span data-stu-id="815c4-145">NOTES</span></span>

## <span data-ttu-id="815c4-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="815c4-146">RELATED LINKS</span></span>

[<span data-ttu-id="815c4-147">AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="815c4-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="815c4-148">移除-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="815c4-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

