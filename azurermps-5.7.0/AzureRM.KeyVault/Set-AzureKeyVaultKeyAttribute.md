---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449337"
---
# <span data-ttu-id="51fe4-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="51fe4-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="51fe4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="51fe4-103">更新金鑰保存庫中金鑰的屬性。</span><span class="sxs-lookup"><span data-stu-id="51fe4-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51fe4-104">句法</span><span class="sxs-lookup"><span data-stu-id="51fe4-104">SYNTAX</span></span>

### <span data-ttu-id="51fe4-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="51fe4-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51fe4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="51fe4-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51fe4-107">說明</span><span class="sxs-lookup"><span data-stu-id="51fe4-107">DESCRIPTION</span></span>
<span data-ttu-id="51fe4-108">**AzureKeyVaultKeyAttribute** Cmdlet 會更新金鑰保存庫中金鑰的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="51fe4-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="51fe4-109">示例</span><span class="sxs-lookup"><span data-stu-id="51fe4-109">EXAMPLES</span></span>

### <span data-ttu-id="51fe4-110">範例1：修改金鑰以啟用它，並設定到期日和標籤</span><span class="sxs-lookup"><span data-stu-id="51fe4-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="51fe4-111">第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="51fe4-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="51fe4-112">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="51fe4-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="51fe4-113">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="51fe4-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="51fe4-114">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="51fe4-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="51fe4-115">第二個命令會建立變數來儲存高嚴重性與會計的標記值。</span><span class="sxs-lookup"><span data-stu-id="51fe4-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="51fe4-116">最後一個命令會修改一個名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="51fe4-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="51fe4-117">該命令會啟用金鑰、將過期時間設定為儲存在 $Expires 的時間，並設定 $Tags 中儲存的標籤。</span><span class="sxs-lookup"><span data-stu-id="51fe4-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="51fe4-118">範例2：修改金鑰以刪除所有標記</span><span class="sxs-lookup"><span data-stu-id="51fe4-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="51fe4-119">這個命令會刪除名為 ITSoftware 之特定版本之金鑰的所有標記。</span><span class="sxs-lookup"><span data-stu-id="51fe4-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="51fe4-120">參數</span><span class="sxs-lookup"><span data-stu-id="51fe4-120">PARAMETERS</span></span>

### <span data-ttu-id="51fe4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fe4-121">-DefaultProfile</span></span>
<span data-ttu-id="51fe4-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="51fe4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51fe4-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="51fe4-123">-Enable</span></span>
<span data-ttu-id="51fe4-124">指定是否要啟用或停用金鑰。</span><span class="sxs-lookup"><span data-stu-id="51fe4-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="51fe4-125">$True 的值會啟用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="51fe4-125">A value of $True enables the key.</span></span> <span data-ttu-id="51fe4-126">$False 的值會停用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="51fe4-126">A value of $False disables the key.</span></span> <span data-ttu-id="51fe4-127">如果您沒有指定此參數，這個 Cmdlet 不會修改金鑰的狀態。</span><span class="sxs-lookup"><span data-stu-id="51fe4-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="51fe4-128">-到期</span><span class="sxs-lookup"><span data-stu-id="51fe4-128">-Expires</span></span>
<span data-ttu-id="51fe4-129">指定此 Cmdlet 更新之金鑰的到期時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="51fe4-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="51fe4-130">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="51fe4-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="51fe4-131">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51fe4-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="51fe4-132">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="51fe4-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="51fe4-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51fe4-133">-InputObject</span></span>
<span data-ttu-id="51fe4-134">主要物件</span><span class="sxs-lookup"><span data-stu-id="51fe4-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe4-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="51fe4-135">-KeyOps</span></span>
<span data-ttu-id="51fe4-136">指定可使用這個 Cmdlet 所新增之金鑰來執行的作業陣列。</span><span class="sxs-lookup"><span data-stu-id="51fe4-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="51fe4-137">如果您沒有指定此參數，則可以執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="51fe4-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="51fe4-138">此參數可接受的值為以逗號分隔的主要動作清單，如 JSON Web 金鑰規格所定義。</span><span class="sxs-lookup"><span data-stu-id="51fe4-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="51fe4-139">這些值 (區分大小寫的) 為：</span><span class="sxs-lookup"><span data-stu-id="51fe4-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="51fe4-140">進行</span><span class="sxs-lookup"><span data-stu-id="51fe4-140">encrypt</span></span>
- <span data-ttu-id="51fe4-141">對</span><span class="sxs-lookup"><span data-stu-id="51fe4-141">decrypt</span></span>
- <span data-ttu-id="51fe4-142">浮</span><span class="sxs-lookup"><span data-stu-id="51fe4-142">wrap</span></span>
- <span data-ttu-id="51fe4-143">解</span><span class="sxs-lookup"><span data-stu-id="51fe4-143">unwrap</span></span>
- <span data-ttu-id="51fe4-144">母音</span><span class="sxs-lookup"><span data-stu-id="51fe4-144">sign</span></span>
- <span data-ttu-id="51fe4-145">是否</span><span class="sxs-lookup"><span data-stu-id="51fe4-145">verify</span></span>
- <span data-ttu-id="51fe4-146">備份</span><span class="sxs-lookup"><span data-stu-id="51fe4-146">backup</span></span>
- <span data-ttu-id="51fe4-147">還原</span><span class="sxs-lookup"><span data-stu-id="51fe4-147">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe4-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="51fe4-148">-Name</span></span>
<span data-ttu-id="51fe4-149">指定要更新的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="51fe4-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="51fe4-150">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="51fe4-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe4-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="51fe4-151">-NotBefore</span></span>
<span data-ttu-id="51fe4-152">指定時間（作為 **DateTime** 物件），在此之後就不能使用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="51fe4-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="51fe4-153">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="51fe4-153">This parameter uses UTC.</span></span>
<span data-ttu-id="51fe4-154">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51fe4-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="51fe4-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51fe4-155">-PassThru</span></span>
<span data-ttu-id="51fe4-156">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="51fe4-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51fe4-157">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="51fe4-157">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51fe4-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="51fe4-158">-Tag</span></span>
<span data-ttu-id="51fe4-159">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="51fe4-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51fe4-160">例如：</span><span class="sxs-lookup"><span data-stu-id="51fe4-160">For example:</span></span>

<span data-ttu-id="51fe4-161">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="51fe4-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="51fe4-162">-VaultName</span><span class="sxs-lookup"><span data-stu-id="51fe4-162">-VaultName</span></span>
<span data-ttu-id="51fe4-163">指定此 Cmdlet 修改金鑰的主要保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="51fe4-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="51fe4-164">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="51fe4-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="51fe4-165">-版本</span><span class="sxs-lookup"><span data-stu-id="51fe4-165">-Version</span></span>
<span data-ttu-id="51fe4-166">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="51fe4-166">Specifies the key version.</span></span>
<span data-ttu-id="51fe4-167">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="51fe4-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fe4-168">-確認</span><span class="sxs-lookup"><span data-stu-id="51fe4-168">-Confirm</span></span>
<span data-ttu-id="51fe4-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="51fe4-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51fe4-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51fe4-170">-WhatIf</span></span>
<span data-ttu-id="51fe4-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51fe4-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51fe4-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51fe4-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51fe4-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fe4-173">CommonParameters</span></span>
<span data-ttu-id="51fe4-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51fe4-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fe4-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51fe4-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fe4-176">輸入</span><span class="sxs-lookup"><span data-stu-id="51fe4-176">INPUTS</span></span>

### <span data-ttu-id="51fe4-177">所有</span><span class="sxs-lookup"><span data-stu-id="51fe4-177">None</span></span>
<span data-ttu-id="51fe4-178">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="51fe4-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51fe4-179">輸出</span><span class="sxs-lookup"><span data-stu-id="51fe4-179">OUTPUTS</span></span>

### <span data-ttu-id="51fe4-180">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="51fe4-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="51fe4-181">筆記</span><span class="sxs-lookup"><span data-stu-id="51fe4-181">NOTES</span></span>

## <span data-ttu-id="51fe4-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="51fe4-182">RELATED LINKS</span></span>

[<span data-ttu-id="51fe4-183">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="51fe4-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="51fe4-184">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="51fe4-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="51fe4-185">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="51fe4-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
