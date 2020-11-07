---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 56a3fb2d31e4f80b15c027945437ffdc78aa131a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795524"
---
# <span data-ttu-id="95cfb-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="95cfb-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="95cfb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="95cfb-103">在金鑰保存庫中建立或更新密碼。</span><span class="sxs-lookup"><span data-stu-id="95cfb-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="95cfb-104">句法</span><span class="sxs-lookup"><span data-stu-id="95cfb-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95cfb-105">說明</span><span class="sxs-lookup"><span data-stu-id="95cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="95cfb-106">**AzKeyVaultSecret** Cmdlet 會在 Azure 金鑰保存庫中建立或更新金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="95cfb-106">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="95cfb-107">如果該秘密不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="95cfb-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="95cfb-108">如果機密已存在，這個 Cmdlet 會建立該秘密的新版本。</span><span class="sxs-lookup"><span data-stu-id="95cfb-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="95cfb-109">示例</span><span class="sxs-lookup"><span data-stu-id="95cfb-109">EXAMPLES</span></span>

### <span data-ttu-id="95cfb-110">範例1：使用預設屬性修改機密值</span><span class="sxs-lookup"><span data-stu-id="95cfb-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="95cfb-111">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Secret 變數中。</span><span class="sxs-lookup"><span data-stu-id="95cfb-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="95cfb-112">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="95cfb-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="95cfb-113">第二個命令會修改名為 Contoso 的金鑰保存庫中名為 ITSecret 的密碼的值。</span><span class="sxs-lookup"><span data-stu-id="95cfb-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="95cfb-114">這個秘密值會變成儲存在 $Secret 中的值。</span><span class="sxs-lookup"><span data-stu-id="95cfb-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="95cfb-115">範例2：使用自訂屬性修改秘密的值</span><span class="sxs-lookup"><span data-stu-id="95cfb-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="95cfb-116">第一個命令會使用 **ConvertTo-SecureString** Cmdlet，將字串轉換成安全字串，然後將該字串儲存在 $Secret 變數中。</span><span class="sxs-lookup"><span data-stu-id="95cfb-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="95cfb-117">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="95cfb-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="95cfb-118">Next 命令會定義到期日期、標籤和內容類型的自訂屬性，並將屬性儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="95cfb-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="95cfb-119">最後一個命令會使用先前指定為變數的值，來修改名為 Contoso 之金鑰保存庫中名為 ITSecret 的密碼的值。</span><span class="sxs-lookup"><span data-stu-id="95cfb-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="95cfb-120">參數</span><span class="sxs-lookup"><span data-stu-id="95cfb-120">PARAMETERS</span></span>

### <span data-ttu-id="95cfb-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="95cfb-121">-ContentType</span></span>
<span data-ttu-id="95cfb-122">指定機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="95cfb-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="95cfb-123">若要刪除現有的內容類型，請指定空字串。</span><span class="sxs-lookup"><span data-stu-id="95cfb-123">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="95cfb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95cfb-124">-DefaultProfile</span></span>
<span data-ttu-id="95cfb-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="95cfb-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95cfb-126">-停用</span><span class="sxs-lookup"><span data-stu-id="95cfb-126">-Disable</span></span>
<span data-ttu-id="95cfb-127">表示此 Cmdlet 會停用密碼。</span><span class="sxs-lookup"><span data-stu-id="95cfb-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="95cfb-128">-到期</span><span class="sxs-lookup"><span data-stu-id="95cfb-128">-Expires</span></span>
<span data-ttu-id="95cfb-129">將過期時間指定為 **DateTime** 物件（針對此 Cmdlet 所更新的機密）。</span><span class="sxs-lookup"><span data-stu-id="95cfb-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="95cfb-130">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="95cfb-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="95cfb-131">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95cfb-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="95cfb-132">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="95cfb-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="95cfb-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="95cfb-133">-Name</span></span>
<span data-ttu-id="95cfb-134">指定要修改之密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="95cfb-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="95cfb-135">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造密碼的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="95cfb-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="95cfb-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="95cfb-136">-NotBefore</span></span>
<span data-ttu-id="95cfb-137">指定時間（作為 **DateTime** 物件），在此之前將無法使用該密碼。</span><span class="sxs-lookup"><span data-stu-id="95cfb-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="95cfb-138">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="95cfb-138">This parameter uses UTC.</span></span> <span data-ttu-id="95cfb-139">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95cfb-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="95cfb-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="95cfb-140">-SecretValue</span></span>
<span data-ttu-id="95cfb-141">將機密的值指定為 **SecureString** 物件。</span><span class="sxs-lookup"><span data-stu-id="95cfb-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="95cfb-142">若要取得 **SecureString** 物件，請使用 **ConvertTo-SecureString** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95cfb-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="95cfb-143">如需詳細資訊，請輸入 `Get-Help
ConvertTo-SecureString` 。</span><span class="sxs-lookup"><span data-stu-id="95cfb-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95cfb-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="95cfb-144">-Tag</span></span>
<span data-ttu-id="95cfb-145">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="95cfb-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="95cfb-146">例如：</span><span class="sxs-lookup"><span data-stu-id="95cfb-146">For example:</span></span>

<span data-ttu-id="95cfb-147">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="95cfb-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="95cfb-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="95cfb-148">-VaultName</span></span>
<span data-ttu-id="95cfb-149">指定此機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="95cfb-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="95cfb-150">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="95cfb-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="95cfb-151">-確認</span><span class="sxs-lookup"><span data-stu-id="95cfb-151">-Confirm</span></span>
<span data-ttu-id="95cfb-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95cfb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95cfb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95cfb-153">-WhatIf</span></span>
<span data-ttu-id="95cfb-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95cfb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95cfb-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95cfb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95cfb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95cfb-156">CommonParameters</span></span>
<span data-ttu-id="95cfb-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95cfb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95cfb-158">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95cfb-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95cfb-159">輸入</span><span class="sxs-lookup"><span data-stu-id="95cfb-159">INPUTS</span></span>

### <span data-ttu-id="95cfb-160">所有</span><span class="sxs-lookup"><span data-stu-id="95cfb-160">None</span></span>
<span data-ttu-id="95cfb-161">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="95cfb-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95cfb-162">輸出</span><span class="sxs-lookup"><span data-stu-id="95cfb-162">OUTPUTS</span></span>

### <span data-ttu-id="95cfb-163">KeyVault （密碼）。</span><span class="sxs-lookup"><span data-stu-id="95cfb-163">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="95cfb-164">筆記</span><span class="sxs-lookup"><span data-stu-id="95cfb-164">NOTES</span></span>

## <span data-ttu-id="95cfb-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="95cfb-165">RELATED LINKS</span></span>

[<span data-ttu-id="95cfb-166">AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="95cfb-166">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="95cfb-167">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="95cfb-167">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
