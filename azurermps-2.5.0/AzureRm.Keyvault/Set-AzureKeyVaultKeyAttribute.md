---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
ms.openlocfilehash: e7daafc147775b128351a7fa9ffb7b4d807bfe17
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801298"
---
# <span data-ttu-id="fae17-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="fae17-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="fae17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fae17-102">SYNOPSIS</span></span>
<span data-ttu-id="fae17-103">更新金鑰保存庫中金鑰的屬性。</span><span class="sxs-lookup"><span data-stu-id="fae17-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae17-104">句法</span><span class="sxs-lookup"><span data-stu-id="fae17-104">SYNTAX</span></span>

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae17-105">說明</span><span class="sxs-lookup"><span data-stu-id="fae17-105">DESCRIPTION</span></span>
<span data-ttu-id="fae17-106">**AzureKeyVaultKeyAttribute** Cmdlet 會更新金鑰保存庫中金鑰的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="fae17-106">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="fae17-107">示例</span><span class="sxs-lookup"><span data-stu-id="fae17-107">EXAMPLES</span></span>

### <span data-ttu-id="fae17-108">範例1：修改金鑰以啟用它，並設定到期日和標籤</span><span class="sxs-lookup"><span data-stu-id="fae17-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="fae17-109">第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="fae17-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="fae17-110">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="fae17-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="fae17-111">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="fae17-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="fae17-112">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="fae17-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="fae17-113">第二個命令會建立變數來儲存高嚴重性與會計的標記值。</span><span class="sxs-lookup"><span data-stu-id="fae17-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="fae17-114">最後一個命令會修改一個名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="fae17-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="fae17-115">該命令會啟用金鑰、將過期時間設定為儲存在 $Expires 的時間，並設定 $Tags 中儲存的標籤。</span><span class="sxs-lookup"><span data-stu-id="fae17-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="fae17-116">範例2：修改金鑰以刪除所有標記</span><span class="sxs-lookup"><span data-stu-id="fae17-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="fae17-117">這個命令會刪除名為 ITSoftware 之特定版本之金鑰的所有標記。</span><span class="sxs-lookup"><span data-stu-id="fae17-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="fae17-118">參數</span><span class="sxs-lookup"><span data-stu-id="fae17-118">PARAMETERS</span></span>

### <span data-ttu-id="fae17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae17-119">-DefaultProfile</span></span>
<span data-ttu-id="fae17-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fae17-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fae17-121">-啟用</span><span class="sxs-lookup"><span data-stu-id="fae17-121">-Enable</span></span>
<span data-ttu-id="fae17-122">指定是否要啟用或停用金鑰。</span><span class="sxs-lookup"><span data-stu-id="fae17-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="fae17-123">$True 的值會啟用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fae17-123">A value of $True enables the key.</span></span> <span data-ttu-id="fae17-124">$False 的值會停用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fae17-124">A value of $False disables the key.</span></span> <span data-ttu-id="fae17-125">如果您沒有指定此參數，這個 Cmdlet 不會修改金鑰的狀態。</span><span class="sxs-lookup"><span data-stu-id="fae17-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="fae17-126">-到期</span><span class="sxs-lookup"><span data-stu-id="fae17-126">-Expires</span></span>
<span data-ttu-id="fae17-127">指定此 Cmdlet 更新之金鑰的到期時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="fae17-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="fae17-128">此參數使用協調通用時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="fae17-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fae17-129">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fae17-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="fae17-130">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="fae17-130">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="fae17-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="fae17-131">-KeyOps</span></span>
<span data-ttu-id="fae17-132">指定可使用這個 Cmdlet 所新增之金鑰來執行的作業陣列。</span><span class="sxs-lookup"><span data-stu-id="fae17-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="fae17-133">如果您沒有指定此參數，則可以執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="fae17-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="fae17-134">此參數可接受的值為以逗號分隔的主要動作清單，如 JSON Web 金鑰規格所定義。</span><span class="sxs-lookup"><span data-stu-id="fae17-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="fae17-135">這些值 (區分大小寫的) 為：</span><span class="sxs-lookup"><span data-stu-id="fae17-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="fae17-136">進行</span><span class="sxs-lookup"><span data-stu-id="fae17-136">encrypt</span></span>
- <span data-ttu-id="fae17-137">對</span><span class="sxs-lookup"><span data-stu-id="fae17-137">decrypt</span></span>
- <span data-ttu-id="fae17-138">浮</span><span class="sxs-lookup"><span data-stu-id="fae17-138">wrap</span></span>
- <span data-ttu-id="fae17-139">解</span><span class="sxs-lookup"><span data-stu-id="fae17-139">unwrap</span></span>
- <span data-ttu-id="fae17-140">母音</span><span class="sxs-lookup"><span data-stu-id="fae17-140">sign</span></span>
- <span data-ttu-id="fae17-141">是否</span><span class="sxs-lookup"><span data-stu-id="fae17-141">verify</span></span>
- <span data-ttu-id="fae17-142">備份</span><span class="sxs-lookup"><span data-stu-id="fae17-142">backup</span></span>
- <span data-ttu-id="fae17-143">還原</span><span class="sxs-lookup"><span data-stu-id="fae17-143">restore</span></span>

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

### <span data-ttu-id="fae17-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="fae17-144">-Name</span></span>
<span data-ttu-id="fae17-145">指定要更新的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="fae17-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="fae17-146">這個 Cmdlet 會根據此參數指定的名稱、主要電子倉庫的名稱和您目前的環境，來構造金鑰的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="fae17-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae17-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="fae17-147">-NotBefore</span></span>
<span data-ttu-id="fae17-148">指定時間（作為 **DateTime** 物件），在此之後就不能使用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fae17-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="fae17-149">此參數使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="fae17-149">This parameter uses UTC.</span></span>
<span data-ttu-id="fae17-150">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fae17-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="fae17-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fae17-151">-PassThru</span></span>
<span data-ttu-id="fae17-152">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fae17-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fae17-153">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fae17-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fae17-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="fae17-154">-Tag</span></span>
<span data-ttu-id="fae17-155">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="fae17-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fae17-156">例如：</span><span class="sxs-lookup"><span data-stu-id="fae17-156">For example:</span></span>

<span data-ttu-id="fae17-157">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fae17-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fae17-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fae17-158">-VaultName</span></span>
<span data-ttu-id="fae17-159">指定此 Cmdlet 修改金鑰的主要保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fae17-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="fae17-160">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fae17-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="fae17-161">-版本</span><span class="sxs-lookup"><span data-stu-id="fae17-161">-Version</span></span>
<span data-ttu-id="fae17-162">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="fae17-162">Specifies the key version.</span></span>
<span data-ttu-id="fae17-163">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fae17-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="fae17-164">-確認</span><span class="sxs-lookup"><span data-stu-id="fae17-164">-Confirm</span></span>
<span data-ttu-id="fae17-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fae17-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae17-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae17-166">-WhatIf</span></span>
<span data-ttu-id="fae17-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fae17-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae17-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fae17-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae17-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae17-169">CommonParameters</span></span>
<span data-ttu-id="fae17-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fae17-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae17-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fae17-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae17-172">輸入</span><span class="sxs-lookup"><span data-stu-id="fae17-172">INPUTS</span></span>

## <span data-ttu-id="fae17-173">輸出</span><span class="sxs-lookup"><span data-stu-id="fae17-173">OUTPUTS</span></span>

### <span data-ttu-id="fae17-174">KeyBundle 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fae17-174">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="fae17-175">筆記</span><span class="sxs-lookup"><span data-stu-id="fae17-175">NOTES</span></span>

## <span data-ttu-id="fae17-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="fae17-176">RELATED LINKS</span></span>

[<span data-ttu-id="fae17-177">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fae17-177">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="fae17-178">AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fae17-178">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="fae17-179">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fae17-179">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
