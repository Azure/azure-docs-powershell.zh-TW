---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626151"
---
# <span data-ttu-id="5a003-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="5a003-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="5a003-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a003-102">SYNOPSIS</span></span>
<span data-ttu-id="5a003-103">更新金鑰保存庫中密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a003-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a003-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a003-104">SYNTAX</span></span>

### <span data-ttu-id="5a003-105">設置</span><span class="sxs-lookup"><span data-stu-id="5a003-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a003-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a003-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a003-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a003-107">DESCRIPTION</span></span>
<span data-ttu-id="5a003-108">**AzureKeyVaultSecretAttribute** Cmdlet 會更新金鑰保存庫中的秘密可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="5a003-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="5a003-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a003-109">EXAMPLES</span></span>

### <span data-ttu-id="5a003-110">範例1：修改密碼的屬性</span><span class="sxs-lookup"><span data-stu-id="5a003-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="5a003-111">前四個命令會定義到期日期、NotBefore 日期、標籤和內容類型的屬性，並將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="5a003-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="5a003-112">最後一個命令會使用儲存的變數，在名為 ContosoVault 的金鑰保存庫中修改名為 HR 的密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a003-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="5a003-113">範例2：刪除機密的標記與內容類型</span><span class="sxs-lookup"><span data-stu-id="5a003-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="5a003-114">這個命令會在名為 [Contoso] 的 [主要電子倉庫] 中，刪除名為「HR」之指定版本之密碼的標記和內容類型。</span><span class="sxs-lookup"><span data-stu-id="5a003-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="5a003-115">範例3：停用其名稱以其開頭的最新版本密碼</span><span class="sxs-lookup"><span data-stu-id="5a003-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="5a003-116">第一個命令會將字串值 Contoso 儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="5a003-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="5a003-117">第二個命令會將字串值儲存在 $Prefix 變數中。</span><span class="sxs-lookup"><span data-stu-id="5a003-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="5a003-118">第三個命令使用 Get-AzureKeyVaultSecret Cmdlet 在指定的金鑰保存庫中取得機密，然後將這些機密傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a003-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="5a003-119">**物件** Cmdlet 會篩選以字元開頭的名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="5a003-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="5a003-120">命令會將與篩選器相符的秘訣加入 Set-AzureKeyVaultSecretAttribute Cmdlet，從而停用。</span><span class="sxs-lookup"><span data-stu-id="5a003-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="5a003-121">範例4：為所有版本的機密設定 ContentType</span><span class="sxs-lookup"><span data-stu-id="5a003-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="5a003-122">前三個命令會定義要用於 *VaultName* 、 *名稱* 和 *ContentType* 參數的字串變數。</span><span class="sxs-lookup"><span data-stu-id="5a003-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="5a003-123">第四個命令使用 Get-AzureKeyVaultKey Cmdlet 來取得指定的金鑰，並將這些金鑰管道到 Set-AzureKeyVaultSecretAttribute Cmdlet，以將其內容類型設為 XML。</span><span class="sxs-lookup"><span data-stu-id="5a003-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="5a003-124">參數</span><span class="sxs-lookup"><span data-stu-id="5a003-124">PARAMETERS</span></span>

### <span data-ttu-id="5a003-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5a003-125">-ContentType</span></span>
<span data-ttu-id="5a003-126">指定機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="5a003-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="5a003-127">如果您沒有指定此參數，目前密碼的內容類型就不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="5a003-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="5a003-128">若要移除現有的內容類型，請指定一個空字串。</span><span class="sxs-lookup"><span data-stu-id="5a003-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a003-129">-DefaultProfile</span></span>
<span data-ttu-id="5a003-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5a003-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a003-131">-啟用</span><span class="sxs-lookup"><span data-stu-id="5a003-131">-Enable</span></span>
<span data-ttu-id="5a003-132">指出是否要啟用秘密。</span><span class="sxs-lookup"><span data-stu-id="5a003-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="5a003-133">指定 $False 以停用機密，或 $True 以啟用機密。</span><span class="sxs-lookup"><span data-stu-id="5a003-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="5a003-134">如果您沒有指定此參數，就不會變更目前機密的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="5a003-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-135">-到期</span><span class="sxs-lookup"><span data-stu-id="5a003-135">-Expires</span></span>
<span data-ttu-id="5a003-136">指定秘密到期的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5a003-136">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a003-137">-InputObject</span></span>
<span data-ttu-id="5a003-138">秘密物件</span><span class="sxs-lookup"><span data-stu-id="5a003-138">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a003-139">-Name</span></span>
<span data-ttu-id="5a003-140">指定秘密的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a003-140">Specifies the name of a secret.</span></span> <span data-ttu-id="5a003-141">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="5a003-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="5a003-142">-NotBefore</span></span>
<span data-ttu-id="5a003-143">指定在無法使用密碼前 (UTC) 的協調通用時間。</span><span class="sxs-lookup"><span data-stu-id="5a003-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="5a003-144">如果您沒有指定此參數，則目前密碼的 NotBefore 屬性不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="5a003-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a003-145">-PassThru</span></span>
<span data-ttu-id="5a003-146">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5a003-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a003-147">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5a003-147">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a003-148">-Tag</span></span>
<span data-ttu-id="5a003-149">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="5a003-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5a003-150">例如：</span><span class="sxs-lookup"><span data-stu-id="5a003-150">For example:</span></span>

<span data-ttu-id="5a003-151">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5a003-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5a003-152">-VaultName</span></span>
<span data-ttu-id="5a003-153">指定要修改的主要保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a003-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="5a003-154">這個 Cmdlet 會根據此參數指定的名稱，以及您目前所選的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5a003-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-155">-版本</span><span class="sxs-lookup"><span data-stu-id="5a003-155">-Version</span></span>
<span data-ttu-id="5a003-156">指定機密的版本。</span><span class="sxs-lookup"><span data-stu-id="5a003-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="5a003-157">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、密碼及機密版本來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5a003-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-158">-確認</span><span class="sxs-lookup"><span data-stu-id="5a003-158">-Confirm</span></span>
<span data-ttu-id="5a003-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a003-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a003-160">-WhatIf</span></span>
<span data-ttu-id="5a003-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a003-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a003-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a003-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a003-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a003-163">CommonParameters</span></span>
<span data-ttu-id="5a003-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a003-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a003-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a003-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a003-166">輸入</span><span class="sxs-lookup"><span data-stu-id="5a003-166">INPUTS</span></span>

### <span data-ttu-id="5a003-167">所有</span><span class="sxs-lookup"><span data-stu-id="5a003-167">None</span></span>
<span data-ttu-id="5a003-168">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5a003-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a003-169">輸出</span><span class="sxs-lookup"><span data-stu-id="5a003-169">OUTPUTS</span></span>

### <span data-ttu-id="5a003-170">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="5a003-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="5a003-171">如果已指定 PassThru，則會傳回 KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="5a003-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="5a003-172">否則，就不會傳回任何內容。</span><span class="sxs-lookup"><span data-stu-id="5a003-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="5a003-173">筆記</span><span class="sxs-lookup"><span data-stu-id="5a003-173">NOTES</span></span>

## <span data-ttu-id="5a003-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a003-174">RELATED LINKS</span></span>

[<span data-ttu-id="5a003-175">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a003-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="5a003-176">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a003-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="5a003-177">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a003-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
