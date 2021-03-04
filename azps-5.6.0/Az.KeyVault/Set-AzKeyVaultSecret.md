---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: a9c104bfc1935f65969e11af8de0abdb4f46c3e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909022"
---
# <span data-ttu-id="630a9-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="630a9-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="630a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="630a9-102">SYNOPSIS</span></span>
<span data-ttu-id="630a9-103">在金鑰庫中建立或更新密碼。</span><span class="sxs-lookup"><span data-stu-id="630a9-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="630a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="630a9-104">SYNTAX</span></span>

### <span data-ttu-id="630a9-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="630a9-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="630a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="630a9-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="630a9-107">描述</span><span class="sxs-lookup"><span data-stu-id="630a9-107">DESCRIPTION</span></span>
<span data-ttu-id="630a9-108">**Set-AzKeyVaultSecret** Cmdlet 在 Azure 金鑰庫的金鑰庫中建立或更新金鑰庫的機密。</span><span class="sxs-lookup"><span data-stu-id="630a9-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="630a9-109">如果密碼不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="630a9-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="630a9-110">如果密碼已存在，此 Cmdlet 會建立該機密的新版本。</span><span class="sxs-lookup"><span data-stu-id="630a9-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="630a9-111">例子</span><span class="sxs-lookup"><span data-stu-id="630a9-111">EXAMPLES</span></span>

### <span data-ttu-id="630a9-112">範例 1：使用預設屬性修改機密的值</span><span class="sxs-lookup"><span data-stu-id="630a9-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="630a9-113">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Secret 變數中。</span><span class="sxs-lookup"><span data-stu-id="630a9-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="630a9-114">如需要詳細資訊，請鍵入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="630a9-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="630a9-115">第二個命令會修改名稱為 Contoso 之金鑰庫中名為 ITSecret 的機密值。</span><span class="sxs-lookup"><span data-stu-id="630a9-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="630a9-116">機密值會變成儲存在 $Secret。</span><span class="sxs-lookup"><span data-stu-id="630a9-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="630a9-117">範例 2：使用自訂屬性修改機密值</span><span class="sxs-lookup"><span data-stu-id="630a9-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="630a9-118">第一個命令會使用 **ConvertTo-SecureString** Cmdlet 將字串轉換為安全字串，然後將該字串儲存在 $Secret 變數中。</span><span class="sxs-lookup"><span data-stu-id="630a9-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="630a9-119">如需要詳細資訊，請鍵入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="630a9-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="630a9-120">下一個命令會定義到期日、標記和上下文類型的自訂屬性，並且將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="630a9-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="630a9-121">最後一個命令會使用先前指定為變數的值，修改名稱為 Contoso 之金鑰庫中名為 ITSecret 的機密值。</span><span class="sxs-lookup"><span data-stu-id="630a9-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="630a9-122">參數</span><span class="sxs-lookup"><span data-stu-id="630a9-122">PARAMETERS</span></span>

### <span data-ttu-id="630a9-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="630a9-123">-ContentType</span></span>
<span data-ttu-id="630a9-124">指定機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="630a9-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="630a9-125">若要刪除現有的內容類型，請指定空白字串。</span><span class="sxs-lookup"><span data-stu-id="630a9-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="630a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="630a9-126">-DefaultProfile</span></span>
<span data-ttu-id="630a9-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="630a9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="630a9-128">-停用</span><span class="sxs-lookup"><span data-stu-id="630a9-128">-Disable</span></span>
<span data-ttu-id="630a9-129">表示此 Cmdlet 會停用一個機密。</span><span class="sxs-lookup"><span data-stu-id="630a9-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="630a9-130">-到期</span><span class="sxs-lookup"><span data-stu-id="630a9-130">-Expires</span></span>
<span data-ttu-id="630a9-131">指定此 Cmdlet 更新之機密的到期日 ，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="630a9-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="630a9-132">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="630a9-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="630a9-133">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="630a9-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="630a9-134">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="630a9-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="630a9-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="630a9-135">-InputObject</span></span>
<span data-ttu-id="630a9-136">機密物件</span><span class="sxs-lookup"><span data-stu-id="630a9-136">Secret object</span></span>

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

### <span data-ttu-id="630a9-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="630a9-137">-Name</span></span>
<span data-ttu-id="630a9-138">指定要修改的機密名稱。</span><span class="sxs-lookup"><span data-stu-id="630a9-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="630a9-139">此 Cmdlet 會根據此參數指定的名稱、金鑰庫的名稱，以及您目前的環境，建構完整功能變數名稱 (FQDN) 的機密。</span><span class="sxs-lookup"><span data-stu-id="630a9-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="630a9-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="630a9-140">-NotBefore</span></span>
<span data-ttu-id="630a9-141">指定時間 ，做為 **DateTime** 物件，在該物件之前無法使用該機密。</span><span class="sxs-lookup"><span data-stu-id="630a9-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="630a9-142">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="630a9-142">This parameter uses UTC.</span></span> <span data-ttu-id="630a9-143">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="630a9-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="630a9-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="630a9-144">-SecretValue</span></span>
<span data-ttu-id="630a9-145">將機密的值指定為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="630a9-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="630a9-146">若要取得 **SecureString 物件** ，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="630a9-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="630a9-147">如需要詳細資訊，請鍵入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="630a9-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="630a9-148">-標記</span><span class="sxs-lookup"><span data-stu-id="630a9-148">-Tag</span></span>
<span data-ttu-id="630a9-149">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="630a9-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="630a9-150">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="630a9-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="630a9-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="630a9-151">-VaultName</span></span>
<span data-ttu-id="630a9-152">指定此機密所屬的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="630a9-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="630a9-153">此 Cmdlet 會依據此參數指定的名稱和您目前的環境，建構金鑰庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="630a9-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="630a9-154">-確認</span><span class="sxs-lookup"><span data-stu-id="630a9-154">-Confirm</span></span>
<span data-ttu-id="630a9-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="630a9-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="630a9-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="630a9-156">-WhatIf</span></span>
<span data-ttu-id="630a9-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="630a9-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="630a9-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="630a9-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="630a9-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630a9-159">CommonParameters</span></span>
<span data-ttu-id="630a9-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="630a9-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630a9-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="630a9-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630a9-162">輸入</span><span class="sxs-lookup"><span data-stu-id="630a9-162">INPUTS</span></span>

### <span data-ttu-id="630a9-163">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="630a9-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="630a9-164">輸出</span><span class="sxs-lookup"><span data-stu-id="630a9-164">OUTPUTS</span></span>

### <span data-ttu-id="630a9-165">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="630a9-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="630a9-166">筆記</span><span class="sxs-lookup"><span data-stu-id="630a9-166">NOTES</span></span>

## <span data-ttu-id="630a9-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="630a9-167">RELATED LINKS</span></span>

[<span data-ttu-id="630a9-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="630a9-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="630a9-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="630a9-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
