---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127827"
---
# <span data-ttu-id="160b0-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="160b0-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="160b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="160b0-102">SYNOPSIS</span></span>
<span data-ttu-id="160b0-103">在金鑰保存庫中建立或更新密碼。</span><span class="sxs-lookup"><span data-stu-id="160b0-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="160b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="160b0-104">SYNTAX</span></span>

### <span data-ttu-id="160b0-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="160b0-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="160b0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="160b0-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="160b0-107">說明</span><span class="sxs-lookup"><span data-stu-id="160b0-107">DESCRIPTION</span></span>
<span data-ttu-id="160b0-108">**AzKeyVaultSecret** Cmdlet 會在 Azure 金鑰保存庫中建立或更新金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="160b0-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="160b0-109">如果該秘密不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="160b0-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="160b0-110">如果機密已存在，這個 Cmdlet 會建立該秘密的新版本。</span><span class="sxs-lookup"><span data-stu-id="160b0-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="160b0-111">示例</span><span class="sxs-lookup"><span data-stu-id="160b0-111">EXAMPLES</span></span>

### <span data-ttu-id="160b0-112">範例1：使用預設屬性修改機密值</span><span class="sxs-lookup"><span data-stu-id="160b0-112">Example 1: Modify the value of a secret using default attributes</span></span>
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

<span data-ttu-id="160b0-113">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Secret 變數中。</span><span class="sxs-lookup"><span data-stu-id="160b0-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="160b0-114">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="160b0-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="160b0-115">第二個命令會修改名為 Contoso 的金鑰保存庫中名為 ITSecret 的密碼的值。</span><span class="sxs-lookup"><span data-stu-id="160b0-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="160b0-116">這個秘密值會變成儲存在 $Secret 中的值。</span><span class="sxs-lookup"><span data-stu-id="160b0-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="160b0-117">範例2：使用自訂屬性修改秘密的值</span><span class="sxs-lookup"><span data-stu-id="160b0-117">Example 2: Modify the value of a secret using custom attributes</span></span>
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

<span data-ttu-id="160b0-118">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Secret 變數中。</span><span class="sxs-lookup"><span data-stu-id="160b0-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="160b0-119">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="160b0-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="160b0-120">Next 命令會定義到期日期、標籤和內容類型的自訂屬性，並將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="160b0-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="160b0-121">最後一個命令會使用先前指定為變數的值，來修改名為 Contoso 之金鑰保存庫中名為 ITSecret 的密碼的值。</span><span class="sxs-lookup"><span data-stu-id="160b0-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="160b0-122">參數</span><span class="sxs-lookup"><span data-stu-id="160b0-122">PARAMETERS</span></span>

### <span data-ttu-id="160b0-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="160b0-123">-ContentType</span></span>
<span data-ttu-id="160b0-124">指定機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="160b0-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="160b0-125">若要刪除現有的內容類型，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="160b0-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="160b0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160b0-126">-DefaultProfile</span></span>
<span data-ttu-id="160b0-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="160b0-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="160b0-128">-停用</span><span class="sxs-lookup"><span data-stu-id="160b0-128">-Disable</span></span>
<span data-ttu-id="160b0-129">表示此 Cmdlet 會停用密碼。</span><span class="sxs-lookup"><span data-stu-id="160b0-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="160b0-130">-到期</span><span class="sxs-lookup"><span data-stu-id="160b0-130">-Expires</span></span>
<span data-ttu-id="160b0-131">將過期時間指定為 **DateTime** 物件（針對此 Cmdlet 所更新的機密）。</span><span class="sxs-lookup"><span data-stu-id="160b0-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="160b0-132">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="160b0-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="160b0-133">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="160b0-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="160b0-134">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="160b0-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="160b0-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="160b0-135">-InputObject</span></span>
<span data-ttu-id="160b0-136">秘密物件</span><span class="sxs-lookup"><span data-stu-id="160b0-136">Secret object</span></span>

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

### <span data-ttu-id="160b0-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="160b0-137">-Name</span></span>
<span data-ttu-id="160b0-138">指定要修改之密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="160b0-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="160b0-139">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="160b0-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="160b0-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="160b0-140">-NotBefore</span></span>
<span data-ttu-id="160b0-141">指定時間（作為 **DateTime** 物件），在此之前將無法使用該密碼。</span><span class="sxs-lookup"><span data-stu-id="160b0-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="160b0-142">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="160b0-142">This parameter uses UTC.</span></span> <span data-ttu-id="160b0-143">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="160b0-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="160b0-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="160b0-144">-SecretValue</span></span>
<span data-ttu-id="160b0-145">將機密的值指定為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="160b0-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="160b0-146">若要取得 **SecureString** 物件，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="160b0-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="160b0-147">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="160b0-147">For more information, type `Get-Help
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

### <span data-ttu-id="160b0-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="160b0-148">-Tag</span></span>
<span data-ttu-id="160b0-149">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="160b0-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="160b0-150">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="160b0-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="160b0-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="160b0-151">-VaultName</span></span>
<span data-ttu-id="160b0-152">指定此機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="160b0-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="160b0-153">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="160b0-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="160b0-154">-確認</span><span class="sxs-lookup"><span data-stu-id="160b0-154">-Confirm</span></span>
<span data-ttu-id="160b0-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="160b0-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160b0-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160b0-156">-WhatIf</span></span>
<span data-ttu-id="160b0-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="160b0-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160b0-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="160b0-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160b0-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160b0-159">CommonParameters</span></span>
<span data-ttu-id="160b0-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="160b0-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160b0-161">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="160b0-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160b0-162">輸入</span><span class="sxs-lookup"><span data-stu-id="160b0-162">INPUTS</span></span>

### <span data-ttu-id="160b0-163">PSKeyVaultSecretIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="160b0-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="160b0-164">輸出</span><span class="sxs-lookup"><span data-stu-id="160b0-164">OUTPUTS</span></span>

### <span data-ttu-id="160b0-165">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="160b0-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="160b0-166">筆記</span><span class="sxs-lookup"><span data-stu-id="160b0-166">NOTES</span></span>

## <span data-ttu-id="160b0-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="160b0-167">RELATED LINKS</span></span>

[<span data-ttu-id="160b0-168">AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="160b0-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="160b0-169">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="160b0-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
