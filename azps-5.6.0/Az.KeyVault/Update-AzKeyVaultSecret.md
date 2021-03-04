---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 975395c471a08eac745bd8a9ab07cec826d5c038
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908137"
---
# <span data-ttu-id="ffe59-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ffe59-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="ffe59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ffe59-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe59-103">更新金鑰庫中之機密的屬性。</span><span class="sxs-lookup"><span data-stu-id="ffe59-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ffe59-104">語法</span><span class="sxs-lookup"><span data-stu-id="ffe59-104">SYNTAX</span></span>

### <span data-ttu-id="ffe59-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ffe59-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffe59-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ffe59-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffe59-107">描述</span><span class="sxs-lookup"><span data-stu-id="ffe59-107">DESCRIPTION</span></span>
<span data-ttu-id="ffe59-108">**Update-AzKeyVaultSecret** Cmdlet 會更新金鑰保存庫中機密的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="ffe59-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ffe59-109">例子</span><span class="sxs-lookup"><span data-stu-id="ffe59-109">EXAMPLES</span></span>

### <span data-ttu-id="ffe59-110">範例 1：修改機密的屬性</span><span class="sxs-lookup"><span data-stu-id="ffe59-110">Example 1: Modify the attributes of a secret</span></span>
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

<span data-ttu-id="ffe59-111">前四個命令會定義到期日的屬性、NotBefore 日期、標記和上下文類型，以及將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="ffe59-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="ffe59-112">最後一個命令會使用儲存的變數，修改名稱為 ContosoVault 之金鑰保存庫中名為 HR 的機密屬性。</span><span class="sxs-lookup"><span data-stu-id="ffe59-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="ffe59-113">範例 2：刪除機密的標記和內容類型</span><span class="sxs-lookup"><span data-stu-id="ffe59-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="ffe59-114">此命令會刪除名稱為 Contoso 之金鑰庫中指定 HR 之指定版本的標籤和內容類型。</span><span class="sxs-lookup"><span data-stu-id="ffe59-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="ffe59-115">範例 3：停用名稱以 IT 開頭的目前版本的秘訣</span><span class="sxs-lookup"><span data-stu-id="ffe59-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="ffe59-116">第一個命令將字串值 Contoso 儲存在$Vault變數。</span><span class="sxs-lookup"><span data-stu-id="ffe59-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="ffe59-117">第二個命令將字串值 IT 儲存在$Prefix變數中。</span><span class="sxs-lookup"><span data-stu-id="ffe59-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="ffe59-118">第三個命令使用 Get-AzKeyVaultSecret Cmdlet 取得指定金鑰庫中的機密，然後將這些秘訣傳遞給 **Where-Object** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffe59-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="ffe59-119">**Where-Object** Cmdlet 會篩選以 IT 字元開頭的名稱之秘訣。</span><span class="sxs-lookup"><span data-stu-id="ffe59-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="ffe59-120">這個命令會篩選出與 Cmdlet 相符的Update-AzKeyVaultSecret，因此會停用它們。</span><span class="sxs-lookup"><span data-stu-id="ffe59-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="ffe59-121">範例 4：針對所有版本的機密設定 ContentType</span><span class="sxs-lookup"><span data-stu-id="ffe59-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="ffe59-122">前三個命令會定義要用於 *VaultName、Name* 和 *ContentType 參數的字串* 變數。</span><span class="sxs-lookup"><span data-stu-id="ffe59-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="ffe59-123">第四個命令使用 Get-AzKeyVaultKey Cmdlet 取得指定的按鍵，然後將按鍵Update-AzKeyVaultSecret Cmdlet，以將內容類型設定為 XML。</span><span class="sxs-lookup"><span data-stu-id="ffe59-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="ffe59-124">參數</span><span class="sxs-lookup"><span data-stu-id="ffe59-124">PARAMETERS</span></span>

### <span data-ttu-id="ffe59-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ffe59-125">-ContentType</span></span>
<span data-ttu-id="ffe59-126">機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="ffe59-126">Secret's content type.</span></span>
<span data-ttu-id="ffe59-127">如果未指定，則機密內容類型的現有值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="ffe59-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="ffe59-128">指定空白字串以移除現有的內容類型值。</span><span class="sxs-lookup"><span data-stu-id="ffe59-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="ffe59-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe59-129">-DefaultProfile</span></span>
<span data-ttu-id="ffe59-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffe59-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffe59-131">-啟用</span><span class="sxs-lookup"><span data-stu-id="ffe59-131">-Enable</span></span>
<span data-ttu-id="ffe59-132">如果有，如果值為 True，請啟用一個機密。</span><span class="sxs-lookup"><span data-stu-id="ffe59-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="ffe59-133">如果值為 False，請停用密碼。</span><span class="sxs-lookup"><span data-stu-id="ffe59-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="ffe59-134">如果未指定，則密碼啟用/停用狀態的現有值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="ffe59-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="ffe59-135">-到期</span><span class="sxs-lookup"><span data-stu-id="ffe59-135">-Expires</span></span>
<span data-ttu-id="ffe59-136">以 UTC 時程表示之機密的到期日。</span><span class="sxs-lookup"><span data-stu-id="ffe59-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="ffe59-137">如果未指定，則密碼到期時間的現有值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="ffe59-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="ffe59-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffe59-138">-InputObject</span></span>
<span data-ttu-id="ffe59-139">機密物件</span><span class="sxs-lookup"><span data-stu-id="ffe59-139">Secret object</span></span>

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

### <span data-ttu-id="ffe59-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffe59-140">-Name</span></span>
<span data-ttu-id="ffe59-141">機密名稱。</span><span class="sxs-lookup"><span data-stu-id="ffe59-141">Secret name.</span></span>
<span data-ttu-id="ffe59-142">Cmdlet 會從儲存庫名稱、目前選取的環境和機密名稱建構一個機密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ffe59-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="ffe59-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ffe59-143">-NotBefore</span></span>
<span data-ttu-id="ffe59-144">無法使用機密的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="ffe59-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="ffe59-145">如果未指定，則機密 NotBefore 屬性的現有值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="ffe59-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="ffe59-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffe59-146">-PassThru</span></span>
<span data-ttu-id="ffe59-147">Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="ffe59-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="ffe59-148">如果指定此參數，請返回機密物件。</span><span class="sxs-lookup"><span data-stu-id="ffe59-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="ffe59-149">-標記</span><span class="sxs-lookup"><span data-stu-id="ffe59-149">-Tag</span></span>
<span data-ttu-id="ffe59-150">代表機密標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ffe59-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="ffe59-151">如果未指定，則密碼的現有標記會維持不變。</span><span class="sxs-lookup"><span data-stu-id="ffe59-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="ffe59-152">指定空白雜湊表以移除標記。</span><span class="sxs-lookup"><span data-stu-id="ffe59-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="ffe59-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ffe59-153">-VaultName</span></span>
<span data-ttu-id="ffe59-154">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ffe59-154">Vault name.</span></span>
<span data-ttu-id="ffe59-155">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ffe59-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ffe59-156">-版本</span><span class="sxs-lookup"><span data-stu-id="ffe59-156">-Version</span></span>
<span data-ttu-id="ffe59-157">機密版本。</span><span class="sxs-lookup"><span data-stu-id="ffe59-157">Secret version.</span></span>
<span data-ttu-id="ffe59-158">Cmdlet 會從儲存庫名稱、目前選取的環境、密碼和機密版本建構一個機密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ffe59-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="ffe59-159">-確認</span><span class="sxs-lookup"><span data-stu-id="ffe59-159">-Confirm</span></span>
<span data-ttu-id="ffe59-160">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ffe59-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffe59-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffe59-161">-WhatIf</span></span>
<span data-ttu-id="ffe59-162">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffe59-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffe59-163">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffe59-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffe59-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe59-164">CommonParameters</span></span>
<span data-ttu-id="ffe59-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ffe59-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe59-166">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffe59-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe59-167">輸入</span><span class="sxs-lookup"><span data-stu-id="ffe59-167">INPUTS</span></span>

### <span data-ttu-id="ffe59-168">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ffe59-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="ffe59-169">輸出</span><span class="sxs-lookup"><span data-stu-id="ffe59-169">OUTPUTS</span></span>

### <span data-ttu-id="ffe59-170">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ffe59-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ffe59-171">筆記</span><span class="sxs-lookup"><span data-stu-id="ffe59-171">NOTES</span></span>

## <span data-ttu-id="ffe59-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffe59-172">RELATED LINKS</span></span>
