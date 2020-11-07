---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
ms.openlocfilehash: f8463533f8a153b74df1863ba251950f16f9e19a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799830"
---
# <span data-ttu-id="6eb19-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="6eb19-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="6eb19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6eb19-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb19-103">更新金鑰保存庫中密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb19-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eb19-104">句法</span><span class="sxs-lookup"><span data-stu-id="6eb19-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eb19-105">說明</span><span class="sxs-lookup"><span data-stu-id="6eb19-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb19-106">**AzureKeyVaultSecretAttribute** Cmdlet 會更新金鑰保存庫中的秘密可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb19-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="6eb19-107">示例</span><span class="sxs-lookup"><span data-stu-id="6eb19-107">EXAMPLES</span></span>

### <span data-ttu-id="6eb19-108">範例1：修改密碼的屬性</span><span class="sxs-lookup"><span data-stu-id="6eb19-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="6eb19-109">前四個命令會定義到期日期、NotBefore 日期、標籤和內容類型的屬性，並將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="6eb19-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="6eb19-110">最後一個命令會使用儲存的變數，在名為 ContosoVault 的金鑰保存庫中修改名為 HR 的密碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="6eb19-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="6eb19-111">範例2：刪除機密的標記與內容類型</span><span class="sxs-lookup"><span data-stu-id="6eb19-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="6eb19-112">這個命令會在名為 [Contoso] 的 [主要電子倉庫] 中，刪除名為「HR」之指定版本之密碼的標記和內容類型。</span><span class="sxs-lookup"><span data-stu-id="6eb19-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="6eb19-113">範例3：停用其名稱以其開頭的最新版本密碼</span><span class="sxs-lookup"><span data-stu-id="6eb19-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="6eb19-114">第一個命令會將字串值 Contoso 儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="6eb19-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="6eb19-115">第二個命令會將字串值儲存在 $Prefix 變數中。</span><span class="sxs-lookup"><span data-stu-id="6eb19-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="6eb19-116">第三個命令使用 Get-AzureKeyVaultSecret Cmdlet 在指定的金鑰保存庫中取得機密，然後將這些機密傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb19-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="6eb19-117">**物件** Cmdlet 會篩選以字元開頭的名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="6eb19-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="6eb19-118">命令會將與篩選器相符的秘訣加入 Set-AzureKeyVaultSecretAttribute Cmdlet，從而停用。</span><span class="sxs-lookup"><span data-stu-id="6eb19-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="6eb19-119">範例4：為所有版本的機密設定 ContentType</span><span class="sxs-lookup"><span data-stu-id="6eb19-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="6eb19-120">前三個命令會定義要用於 *VaultName* 、 *名稱* 和 *ContentType* 參數的字串變數。</span><span class="sxs-lookup"><span data-stu-id="6eb19-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="6eb19-121">第四個命令使用 Get-AzureKeyVaultKey Cmdlet 來取得指定的金鑰，並將這些金鑰管道到 Set-AzureKeyVaultSecretAttribute Cmdlet，以將其內容類型設為 XML。</span><span class="sxs-lookup"><span data-stu-id="6eb19-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="6eb19-122">參數</span><span class="sxs-lookup"><span data-stu-id="6eb19-122">PARAMETERS</span></span>

### <span data-ttu-id="6eb19-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6eb19-123">-ContentType</span></span>
<span data-ttu-id="6eb19-124">指定機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="6eb19-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="6eb19-125">如果您沒有指定此參數，目前密碼的內容類型就不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="6eb19-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="6eb19-126">若要移除現有的內容類型，請指定一個空字串。</span><span class="sxs-lookup"><span data-stu-id="6eb19-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="6eb19-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb19-127">-DefaultProfile</span></span>
<span data-ttu-id="6eb19-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6eb19-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6eb19-129">-啟用</span><span class="sxs-lookup"><span data-stu-id="6eb19-129">-Enable</span></span>
<span data-ttu-id="6eb19-130">指出是否要啟用秘密。</span><span class="sxs-lookup"><span data-stu-id="6eb19-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="6eb19-131">指定 $False 以停用機密，或 $True 以啟用機密。</span><span class="sxs-lookup"><span data-stu-id="6eb19-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="6eb19-132">如果您沒有指定此參數，就不會變更目前機密的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="6eb19-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="6eb19-133">-到期</span><span class="sxs-lookup"><span data-stu-id="6eb19-133">-Expires</span></span>
<span data-ttu-id="6eb19-134">指定秘密到期的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6eb19-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="6eb19-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="6eb19-135">-Name</span></span>
<span data-ttu-id="6eb19-136">指定秘密的名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb19-136">Specifies the name of a secret.</span></span> <span data-ttu-id="6eb19-137">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="6eb19-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb19-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="6eb19-138">-NotBefore</span></span>
<span data-ttu-id="6eb19-139">指定在無法使用密碼前 (UTC) 的協調通用時間。</span><span class="sxs-lookup"><span data-stu-id="6eb19-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="6eb19-140">如果您沒有指定此參數，則目前密碼的 NotBefore 屬性不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="6eb19-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="6eb19-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6eb19-141">-PassThru</span></span>
<span data-ttu-id="6eb19-142">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6eb19-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6eb19-143">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6eb19-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6eb19-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="6eb19-144">-Tag</span></span>
<span data-ttu-id="6eb19-145">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6eb19-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6eb19-146">例如：</span><span class="sxs-lookup"><span data-stu-id="6eb19-146">For example:</span></span>

<span data-ttu-id="6eb19-147">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6eb19-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6eb19-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6eb19-148">-VaultName</span></span>
<span data-ttu-id="6eb19-149">指定要修改的主要保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb19-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="6eb19-150">這個 Cmdlet 會根據此參數指定的名稱，以及您目前所選的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6eb19-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb19-151">-版本</span><span class="sxs-lookup"><span data-stu-id="6eb19-151">-Version</span></span>
<span data-ttu-id="6eb19-152">指定機密的版本。</span><span class="sxs-lookup"><span data-stu-id="6eb19-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="6eb19-153">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、密碼及機密版本來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6eb19-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="6eb19-154">-確認</span><span class="sxs-lookup"><span data-stu-id="6eb19-154">-Confirm</span></span>
<span data-ttu-id="6eb19-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6eb19-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb19-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb19-156">-WhatIf</span></span>
<span data-ttu-id="6eb19-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6eb19-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eb19-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eb19-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb19-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb19-159">CommonParameters</span></span>
<span data-ttu-id="6eb19-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6eb19-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb19-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6eb19-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb19-162">輸入</span><span class="sxs-lookup"><span data-stu-id="6eb19-162">INPUTS</span></span>

## <span data-ttu-id="6eb19-163">輸出</span><span class="sxs-lookup"><span data-stu-id="6eb19-163">OUTPUTS</span></span>

### <span data-ttu-id="6eb19-164">KeyVault （密碼）。</span><span class="sxs-lookup"><span data-stu-id="6eb19-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="6eb19-165">如果已指定 PassThru，則會傳回 KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="6eb19-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="6eb19-166">否則，就不會傳回任何內容。</span><span class="sxs-lookup"><span data-stu-id="6eb19-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="6eb19-167">筆記</span><span class="sxs-lookup"><span data-stu-id="6eb19-167">NOTES</span></span>

## <span data-ttu-id="6eb19-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eb19-168">RELATED LINKS</span></span>

[<span data-ttu-id="6eb19-169">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6eb19-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="6eb19-170">AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6eb19-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="6eb19-171">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6eb19-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
