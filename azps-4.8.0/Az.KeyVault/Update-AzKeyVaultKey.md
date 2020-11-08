---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: cae763eedd98a98c7e09855a295791ddc96d5339
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127642"
---
# <span data-ttu-id="079bf-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="079bf-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="079bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="079bf-102">SYNOPSIS</span></span>
<span data-ttu-id="079bf-103">更新金鑰保存庫中金鑰的屬性。</span><span class="sxs-lookup"><span data-stu-id="079bf-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="079bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="079bf-104">SYNTAX</span></span>

### <span data-ttu-id="079bf-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="079bf-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="079bf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="079bf-106">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="079bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="079bf-107">DESCRIPTION</span></span>
<span data-ttu-id="079bf-108">**AzKeyVaultKey** Cmdlet 會更新金鑰保存庫中金鑰的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="079bf-108">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="079bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="079bf-109">EXAMPLES</span></span>

### <span data-ttu-id="079bf-110">範例1：修改金鑰以啟用它，並設定到期日和標籤</span><span class="sxs-lookup"><span data-stu-id="079bf-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="079bf-111">第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="079bf-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="079bf-112">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="079bf-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="079bf-113">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="079bf-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="079bf-114">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="079bf-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="079bf-115">第二個命令會建立變數來儲存高嚴重性與會計的標記值。</span><span class="sxs-lookup"><span data-stu-id="079bf-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="079bf-116">最後一個命令會修改一個名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="079bf-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="079bf-117">該命令會啟用金鑰、將過期時間設定為儲存在 $Expires 的時間，並設定 $Tags 中儲存的標籤。</span><span class="sxs-lookup"><span data-stu-id="079bf-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="079bf-118">範例2：修改金鑰以刪除所有標記</span><span class="sxs-lookup"><span data-stu-id="079bf-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="079bf-119">這個命令會刪除名為 ITSoftware 之特定版本之金鑰的所有標記。</span><span class="sxs-lookup"><span data-stu-id="079bf-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="079bf-120">參數</span><span class="sxs-lookup"><span data-stu-id="079bf-120">PARAMETERS</span></span>

### <span data-ttu-id="079bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="079bf-121">-DefaultProfile</span></span>
<span data-ttu-id="079bf-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="079bf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="079bf-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="079bf-123">-Enable</span></span>
<span data-ttu-id="079bf-124">True 的值會啟用索引鍵和 false 的值 disabless。</span><span class="sxs-lookup"><span data-stu-id="079bf-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="079bf-125">如果未指定，現有的啟用/停用狀態會保持不變。</span><span class="sxs-lookup"><span data-stu-id="079bf-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="079bf-126">-到期</span><span class="sxs-lookup"><span data-stu-id="079bf-126">-Expires</span></span>
<span data-ttu-id="079bf-127">以 UTC 時程表示之金鑰的到期時間。</span><span class="sxs-lookup"><span data-stu-id="079bf-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="079bf-128">如果沒有指定，則金鑰的現有到期時間會保持不變。</span><span class="sxs-lookup"><span data-stu-id="079bf-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="079bf-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="079bf-129">-InputObject</span></span>
<span data-ttu-id="079bf-130">主要物件</span><span class="sxs-lookup"><span data-stu-id="079bf-130">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="079bf-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="079bf-131">-KeyOps</span></span>
<span data-ttu-id="079bf-132">可使用金鑰執行的作業。</span><span class="sxs-lookup"><span data-stu-id="079bf-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="079bf-133">如果沒有指定，則金鑰的現有按鍵動作會保持不變。</span><span class="sxs-lookup"><span data-stu-id="079bf-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="079bf-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="079bf-134">-Name</span></span>
<span data-ttu-id="079bf-135">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="079bf-135">Key name.</span></span>
<span data-ttu-id="079bf-136">Cmdlet 會從保存庫名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="079bf-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="079bf-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="079bf-137">-NotBefore</span></span>
<span data-ttu-id="079bf-138">在無法使用 key 之前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="079bf-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="079bf-139">如果未指定，索引鍵的現有 NotBefore 屬性會保持不變。</span><span class="sxs-lookup"><span data-stu-id="079bf-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="079bf-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="079bf-140">-PassThru</span></span>
<span data-ttu-id="079bf-141">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="079bf-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="079bf-142">如果已指定此開關，則會傳回更新的金鑰束物件。</span><span class="sxs-lookup"><span data-stu-id="079bf-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="079bf-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="079bf-143">-Tag</span></span>
<span data-ttu-id="079bf-144">Hashtable 代表主要標記。</span><span class="sxs-lookup"><span data-stu-id="079bf-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="079bf-145">如果未指定，索引鍵的 existings 標記會保持不變。</span><span class="sxs-lookup"><span data-stu-id="079bf-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="079bf-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="079bf-146">-VaultName</span></span>
<span data-ttu-id="079bf-147">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="079bf-147">Vault name.</span></span>
<span data-ttu-id="079bf-148">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="079bf-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="079bf-149">-版本</span><span class="sxs-lookup"><span data-stu-id="079bf-149">-Version</span></span>
<span data-ttu-id="079bf-150">金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="079bf-150">Key version.</span></span>
<span data-ttu-id="079bf-151">Cmdlet 會從保存庫名稱、目前已選取的環境、金鑰名稱和金鑰版本構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="079bf-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="079bf-152">-確認</span><span class="sxs-lookup"><span data-stu-id="079bf-152">-Confirm</span></span>
<span data-ttu-id="079bf-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="079bf-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="079bf-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="079bf-154">-WhatIf</span></span>
<span data-ttu-id="079bf-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="079bf-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="079bf-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="079bf-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="079bf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="079bf-157">CommonParameters</span></span>
<span data-ttu-id="079bf-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="079bf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="079bf-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="079bf-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="079bf-160">輸入</span><span class="sxs-lookup"><span data-stu-id="079bf-160">INPUTS</span></span>

### <span data-ttu-id="079bf-161">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="079bf-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="079bf-162">輸出</span><span class="sxs-lookup"><span data-stu-id="079bf-162">OUTPUTS</span></span>

### <span data-ttu-id="079bf-163">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="079bf-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="079bf-164">筆記</span><span class="sxs-lookup"><span data-stu-id="079bf-164">NOTES</span></span>

## <span data-ttu-id="079bf-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="079bf-165">RELATED LINKS</span></span>
