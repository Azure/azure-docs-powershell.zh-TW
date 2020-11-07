---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
ms.openlocfilehash: d895485354c33daa4eac57b699358ee0335905be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626094"
---
# <span data-ttu-id="97af6-101">Update-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="97af6-101">Update-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="97af6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97af6-102">SYNOPSIS</span></span>
<span data-ttu-id="97af6-103">更新金鑰保存庫中密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="97af6-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97af6-104">句法</span><span class="sxs-lookup"><span data-stu-id="97af6-104">SYNTAX</span></span>

### <span data-ttu-id="97af6-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="97af6-105">Default (Default)</span></span>
```
Update-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97af6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="97af6-106">InputObject</span></span>
```
Update-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97af6-107">說明</span><span class="sxs-lookup"><span data-stu-id="97af6-107">DESCRIPTION</span></span>
<span data-ttu-id="97af6-108">**AzureKeyVaultSecret** Cmdlet 會更新金鑰保存庫中的秘密可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="97af6-108">The **Update-AzureKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="97af6-109">示例</span><span class="sxs-lookup"><span data-stu-id="97af6-109">EXAMPLES</span></span>

### <span data-ttu-id="97af6-110">範例1：修改密碼的屬性</span><span class="sxs-lookup"><span data-stu-id="97af6-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="97af6-111">前四個命令會定義到期日期、NotBefore 日期、標籤和內容類型的屬性，並將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="97af6-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="97af6-112">最後一個命令會使用儲存的變數，在名為 ContosoVault 的金鑰保存庫中修改名為 HR 的密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="97af6-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="97af6-113">範例2：刪除機密的標記與內容類型</span><span class="sxs-lookup"><span data-stu-id="97af6-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="97af6-114">這個命令會在名為 [Contoso] 的 [主要電子倉庫] 中，刪除名為「HR」之指定版本之密碼的標記和內容類型。</span><span class="sxs-lookup"><span data-stu-id="97af6-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="97af6-115">範例3：停用其名稱以其開頭的最新版本密碼</span><span class="sxs-lookup"><span data-stu-id="97af6-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzureKeyVaultSecret -Enable $False
```

<span data-ttu-id="97af6-116">第一個命令會將字串值 Contoso 儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="97af6-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="97af6-117">第二個命令會將字串值儲存在 $Prefix 變數中。</span><span class="sxs-lookup"><span data-stu-id="97af6-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="97af6-118">第三個命令使用 Get-AzureKeyVaultSecret Cmdlet 在指定的金鑰保存庫中取得機密，然後將這些機密傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97af6-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="97af6-119">**物件** Cmdlet 會篩選以字元開頭的名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="97af6-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="97af6-120">命令會將與篩選器相符的秘訣加入 Update-AzureKeyVaultSecret Cmdlet，從而停用。</span><span class="sxs-lookup"><span data-stu-id="97af6-120">The command pipes the secrets that match the filter to the Update-AzureKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="97af6-121">範例4：為所有版本的機密設定 ContentType</span><span class="sxs-lookup"><span data-stu-id="97af6-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzureKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="97af6-122">前三個命令會定義要用於 *VaultName* 、 *名稱* 和 *ContentType* 參數的字串變數。</span><span class="sxs-lookup"><span data-stu-id="97af6-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="97af6-123">第四個命令使用 Get-AzureKeyVaultKey Cmdlet 來取得指定的金鑰，並將這些金鑰管道到 Update-AzureKeyVaultSecret Cmdlet，以將其內容類型設為 XML。</span><span class="sxs-lookup"><span data-stu-id="97af6-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzureKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="97af6-124">參數</span><span class="sxs-lookup"><span data-stu-id="97af6-124">PARAMETERS</span></span>

### <span data-ttu-id="97af6-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="97af6-125">-ContentType</span></span>
<span data-ttu-id="97af6-126">密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="97af6-126">Secret's content type.</span></span>
<span data-ttu-id="97af6-127">如果沒有指定，則秘密內容類型的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="97af6-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="97af6-128">透過指定空字串來移除現有的內容類型值。</span><span class="sxs-lookup"><span data-stu-id="97af6-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="97af6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97af6-129">-DefaultProfile</span></span>
<span data-ttu-id="97af6-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97af6-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97af6-131">-啟用</span><span class="sxs-lookup"><span data-stu-id="97af6-131">-Enable</span></span>
<span data-ttu-id="97af6-132">如果有的話，請在值為 true 時啟用密碼。</span><span class="sxs-lookup"><span data-stu-id="97af6-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="97af6-133">如果值為 false，則停用密碼。</span><span class="sxs-lookup"><span data-stu-id="97af6-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="97af6-134">如果未指定，則機密的啟用/停用狀態的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="97af6-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="97af6-135">-到期</span><span class="sxs-lookup"><span data-stu-id="97af6-135">-Expires</span></span>
<span data-ttu-id="97af6-136">以 UTC 時程表示的密碼到期時間。</span><span class="sxs-lookup"><span data-stu-id="97af6-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="97af6-137">如果未指定，密碼到期時間的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="97af6-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="97af6-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97af6-138">-InputObject</span></span>
<span data-ttu-id="97af6-139">秘密物件</span><span class="sxs-lookup"><span data-stu-id="97af6-139">Secret object</span></span>

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

### <span data-ttu-id="97af6-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="97af6-140">-Name</span></span>
<span data-ttu-id="97af6-141">[秘密名稱]。</span><span class="sxs-lookup"><span data-stu-id="97af6-141">Secret name.</span></span>
<span data-ttu-id="97af6-142">Cmdlet 會從保存庫名稱、目前已選取的環境和密碼來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="97af6-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="97af6-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="97af6-143">-NotBefore</span></span>
<span data-ttu-id="97af6-144">無法使用密碼前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="97af6-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="97af6-145">如果沒有指定，則密碼的 NotBefore 屬性的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="97af6-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="97af6-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97af6-146">-PassThru</span></span>
<span data-ttu-id="97af6-147">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="97af6-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="97af6-148">如果已指定此開關，請傳回機密物件。</span><span class="sxs-lookup"><span data-stu-id="97af6-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="97af6-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="97af6-149">-Tag</span></span>
<span data-ttu-id="97af6-150">代表秘密標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="97af6-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="97af6-151">如果沒有指定，則機密的現有標記會保持不變。</span><span class="sxs-lookup"><span data-stu-id="97af6-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="97af6-152">指定空的 Hashtable 來移除標記。</span><span class="sxs-lookup"><span data-stu-id="97af6-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="97af6-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="97af6-153">-VaultName</span></span>
<span data-ttu-id="97af6-154">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="97af6-154">Vault name.</span></span>
<span data-ttu-id="97af6-155">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="97af6-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="97af6-156">-版本</span><span class="sxs-lookup"><span data-stu-id="97af6-156">-Version</span></span>
<span data-ttu-id="97af6-157">秘密版本。</span><span class="sxs-lookup"><span data-stu-id="97af6-157">Secret version.</span></span>
<span data-ttu-id="97af6-158">Cmdlet 會從保存庫名稱、目前已選取的環境、秘密名稱和密碼版本構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="97af6-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="97af6-159">-確認</span><span class="sxs-lookup"><span data-stu-id="97af6-159">-Confirm</span></span>
<span data-ttu-id="97af6-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97af6-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97af6-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97af6-161">-WhatIf</span></span>
<span data-ttu-id="97af6-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97af6-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97af6-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97af6-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97af6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97af6-164">CommonParameters</span></span>
<span data-ttu-id="97af6-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97af6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97af6-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97af6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97af6-167">輸入</span><span class="sxs-lookup"><span data-stu-id="97af6-167">INPUTS</span></span>

### <span data-ttu-id="97af6-168">PSKeyVaultSecretIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="97af6-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="97af6-169">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="97af6-169">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="97af6-170">輸出</span><span class="sxs-lookup"><span data-stu-id="97af6-170">OUTPUTS</span></span>

### <span data-ttu-id="97af6-171">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="97af6-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="97af6-172">筆記</span><span class="sxs-lookup"><span data-stu-id="97af6-172">NOTES</span></span>

## <span data-ttu-id="97af6-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="97af6-173">RELATED LINKS</span></span>
