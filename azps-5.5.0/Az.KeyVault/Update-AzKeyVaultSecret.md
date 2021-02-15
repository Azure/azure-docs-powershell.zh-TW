---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131698"
---
# <span data-ttu-id="6779f-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6779f-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6779f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6779f-102">SYNOPSIS</span></span>
<span data-ttu-id="6779f-103">更新金鑰保存庫中密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="6779f-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="6779f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6779f-104">SYNTAX</span></span>

### <span data-ttu-id="6779f-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="6779f-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6779f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6779f-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6779f-107">說明</span><span class="sxs-lookup"><span data-stu-id="6779f-107">DESCRIPTION</span></span>
<span data-ttu-id="6779f-108">**AzKeyVaultSecret** Cmdlet 會更新金鑰保存庫中的秘密可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="6779f-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="6779f-109">示例</span><span class="sxs-lookup"><span data-stu-id="6779f-109">EXAMPLES</span></span>

### <span data-ttu-id="6779f-110">範例1：修改密碼的屬性</span><span class="sxs-lookup"><span data-stu-id="6779f-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="6779f-111">前四個命令會定義到期日期、NotBefore 日期、標籤和內容類型的屬性，並將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="6779f-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="6779f-112">最後一個命令會使用儲存的變數，在名為 ContosoVault 的金鑰保存庫中修改名為 HR 的密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="6779f-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="6779f-113">範例2：刪除機密的標記與內容類型</span><span class="sxs-lookup"><span data-stu-id="6779f-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="6779f-114">這個命令會在名為 [Contoso] 的 [主要電子倉庫] 中，刪除名為「HR」之指定版本之密碼的標記和內容類型。</span><span class="sxs-lookup"><span data-stu-id="6779f-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="6779f-115">範例3：停用其名稱以其開頭的最新版本密碼</span><span class="sxs-lookup"><span data-stu-id="6779f-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="6779f-116">第一個命令會將字串值 Contoso 儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="6779f-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="6779f-117">第二個命令會將字串值儲存在 $Prefix 變數中。</span><span class="sxs-lookup"><span data-stu-id="6779f-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="6779f-118">第三個命令使用 Get-AzKeyVaultSecret Cmdlet 在指定的金鑰保存庫中取得機密，然後將這些機密傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6779f-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="6779f-119">**物件** Cmdlet 會篩選以字元開頭的名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="6779f-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="6779f-120">命令會將與篩選器相符的秘訣加入 Update-AzKeyVaultSecret Cmdlet，從而停用。</span><span class="sxs-lookup"><span data-stu-id="6779f-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="6779f-121">範例4：為所有版本的機密設定 ContentType</span><span class="sxs-lookup"><span data-stu-id="6779f-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="6779f-122">前三個命令會定義要用於 *VaultName*、 *名稱* 和 *ContentType* 參數的字串變數。</span><span class="sxs-lookup"><span data-stu-id="6779f-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="6779f-123">第四個命令使用 Get-AzKeyVaultKey Cmdlet 來取得指定的金鑰，並將這些金鑰管道到 Update-AzKeyVaultSecret Cmdlet，以將其內容類型設為 XML。</span><span class="sxs-lookup"><span data-stu-id="6779f-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="6779f-124">參數</span><span class="sxs-lookup"><span data-stu-id="6779f-124">PARAMETERS</span></span>

### <span data-ttu-id="6779f-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6779f-125">-ContentType</span></span>
<span data-ttu-id="6779f-126">密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="6779f-126">Secret's content type.</span></span>
<span data-ttu-id="6779f-127">如果沒有指定，則秘密內容類型的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6779f-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="6779f-128">透過指定空字串來移除現有的內容類型值。</span><span class="sxs-lookup"><span data-stu-id="6779f-128">Remove the existing content type value by specifying an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6779f-129">-DefaultProfile</span></span>
<span data-ttu-id="6779f-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6779f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6779f-131">-啟用</span><span class="sxs-lookup"><span data-stu-id="6779f-131">-Enable</span></span>
<span data-ttu-id="6779f-132">如果有的話，請在值為 true 時啟用密碼。</span><span class="sxs-lookup"><span data-stu-id="6779f-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="6779f-133">如果值為 false，則停用密碼。</span><span class="sxs-lookup"><span data-stu-id="6779f-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="6779f-134">如果未指定，則機密的啟用/停用狀態的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6779f-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-135">-到期</span><span class="sxs-lookup"><span data-stu-id="6779f-135">-Expires</span></span>
<span data-ttu-id="6779f-136">以 UTC 時程表示的密碼到期時間。</span><span class="sxs-lookup"><span data-stu-id="6779f-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="6779f-137">如果未指定，密碼到期時間的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6779f-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6779f-138">-InputObject</span></span>
<span data-ttu-id="6779f-139">秘密物件</span><span class="sxs-lookup"><span data-stu-id="6779f-139">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="6779f-140">-Name</span></span>
<span data-ttu-id="6779f-141">[秘密名稱]。</span><span class="sxs-lookup"><span data-stu-id="6779f-141">Secret name.</span></span>
<span data-ttu-id="6779f-142">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6779f-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="6779f-143">-NotBefore</span></span>
<span data-ttu-id="6779f-144">無法使用密碼前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="6779f-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="6779f-145">如果沒有指定，則密碼的 NotBefore 屬性的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6779f-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6779f-146">-PassThru</span></span>
<span data-ttu-id="6779f-147">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="6779f-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="6779f-148">如果已指定此開關，請傳回機密物件。</span><span class="sxs-lookup"><span data-stu-id="6779f-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="6779f-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="6779f-149">-Tag</span></span>
<span data-ttu-id="6779f-150">代表秘密標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="6779f-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="6779f-151">如果沒有指定，則機密的現有標記會保持不變。</span><span class="sxs-lookup"><span data-stu-id="6779f-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="6779f-152">指定空的 Hashtable 來移除標記。</span><span class="sxs-lookup"><span data-stu-id="6779f-152">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6779f-153">-VaultName</span></span>
<span data-ttu-id="6779f-154">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6779f-154">Vault name.</span></span>
<span data-ttu-id="6779f-155">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6779f-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-156">-版本</span><span class="sxs-lookup"><span data-stu-id="6779f-156">-Version</span></span>
<span data-ttu-id="6779f-157">秘密版本。</span><span class="sxs-lookup"><span data-stu-id="6779f-157">Secret version.</span></span>
<span data-ttu-id="6779f-158">Cmdlet 會從保存庫名稱、目前已選取的環境、秘密名稱和密碼版本構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6779f-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6779f-159">-確認</span><span class="sxs-lookup"><span data-stu-id="6779f-159">-Confirm</span></span>
<span data-ttu-id="6779f-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6779f-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6779f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6779f-161">-WhatIf</span></span>
<span data-ttu-id="6779f-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6779f-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6779f-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6779f-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6779f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6779f-164">CommonParameters</span></span>
<span data-ttu-id="6779f-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6779f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6779f-166">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6779f-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6779f-167">輸入</span><span class="sxs-lookup"><span data-stu-id="6779f-167">INPUTS</span></span>

### <span data-ttu-id="6779f-168">PSKeyVaultSecretIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="6779f-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="6779f-169">輸出</span><span class="sxs-lookup"><span data-stu-id="6779f-169">OUTPUTS</span></span>

### <span data-ttu-id="6779f-170">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="6779f-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="6779f-171">筆記</span><span class="sxs-lookup"><span data-stu-id="6779f-171">NOTES</span></span>

## <span data-ttu-id="6779f-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="6779f-172">RELATED LINKS</span></span>
