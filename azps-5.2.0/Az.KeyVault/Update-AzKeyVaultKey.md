---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276879"
---
# <span data-ttu-id="55c74-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="55c74-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="55c74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55c74-102">SYNOPSIS</span></span>
<span data-ttu-id="55c74-103">更新金鑰保存庫中金鑰的屬性。</span><span class="sxs-lookup"><span data-stu-id="55c74-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="55c74-104">句法</span><span class="sxs-lookup"><span data-stu-id="55c74-104">SYNTAX</span></span>

### <span data-ttu-id="55c74-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="55c74-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c74-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="55c74-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c74-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="55c74-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55c74-108">說明</span><span class="sxs-lookup"><span data-stu-id="55c74-108">DESCRIPTION</span></span>
<span data-ttu-id="55c74-109">**AzKeyVaultKey** Cmdlet 會更新金鑰保存庫中金鑰的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="55c74-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="55c74-110">示例</span><span class="sxs-lookup"><span data-stu-id="55c74-110">EXAMPLES</span></span>

### <span data-ttu-id="55c74-111">範例1：修改金鑰以啟用它，並設定到期日和標籤</span><span class="sxs-lookup"><span data-stu-id="55c74-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
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

<span data-ttu-id="55c74-112">第一個命令會使用 [**取得日期**] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="55c74-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="55c74-113">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="55c74-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="55c74-114">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="55c74-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="55c74-115">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="55c74-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="55c74-116">第二個命令會建立變數來儲存高嚴重性與會計的標記值。</span><span class="sxs-lookup"><span data-stu-id="55c74-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="55c74-117">最後一個命令會修改一個名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="55c74-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="55c74-118">該命令會啟用金鑰、將過期時間設定為儲存在 $Expires 的時間，並設定 $Tags 中儲存的標籤。</span><span class="sxs-lookup"><span data-stu-id="55c74-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="55c74-119">範例2：修改金鑰以刪除所有標記</span><span class="sxs-lookup"><span data-stu-id="55c74-119">Example 2: Modify a key to delete all tags</span></span>
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

<span data-ttu-id="55c74-120">這個命令會刪除名為 ITSoftware 之特定版本之金鑰的所有標記。</span><span class="sxs-lookup"><span data-stu-id="55c74-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="55c74-121">參數</span><span class="sxs-lookup"><span data-stu-id="55c74-121">PARAMETERS</span></span>

### <span data-ttu-id="55c74-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c74-122">-DefaultProfile</span></span>
<span data-ttu-id="55c74-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55c74-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c74-124">-啟用</span><span class="sxs-lookup"><span data-stu-id="55c74-124">-Enable</span></span>
<span data-ttu-id="55c74-125">True 的值會啟用索引鍵和 false 的值 disabless。</span><span class="sxs-lookup"><span data-stu-id="55c74-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="55c74-126">如果未指定，現有的啟用/停用狀態會保持不變。</span><span class="sxs-lookup"><span data-stu-id="55c74-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="55c74-127">-到期</span><span class="sxs-lookup"><span data-stu-id="55c74-127">-Expires</span></span>
<span data-ttu-id="55c74-128">以 UTC 時程表示之金鑰的到期時間。</span><span class="sxs-lookup"><span data-stu-id="55c74-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="55c74-129">如果沒有指定，則金鑰的現有到期時間會保持不變。</span><span class="sxs-lookup"><span data-stu-id="55c74-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="55c74-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="55c74-130">-HsmName</span></span>
<span data-ttu-id="55c74-131">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="55c74-131">HSM name.</span></span> <span data-ttu-id="55c74-132">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="55c74-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c74-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c74-133">-InputObject</span></span>
<span data-ttu-id="55c74-134">主要物件</span><span class="sxs-lookup"><span data-stu-id="55c74-134">Key object</span></span>

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

### <span data-ttu-id="55c74-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="55c74-135">-KeyOps</span></span>
<span data-ttu-id="55c74-136">可使用金鑰執行的作業。</span><span class="sxs-lookup"><span data-stu-id="55c74-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="55c74-137">如果沒有指定，則金鑰的現有按鍵動作會保持不變。</span><span class="sxs-lookup"><span data-stu-id="55c74-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="55c74-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="55c74-138">-Name</span></span>
<span data-ttu-id="55c74-139">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="55c74-139">Key name.</span></span>
<span data-ttu-id="55c74-140">Cmdlet 會從保存庫名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="55c74-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c74-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="55c74-141">-NotBefore</span></span>
<span data-ttu-id="55c74-142">在無法使用 key 之前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="55c74-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="55c74-143">如果未指定，索引鍵的現有 NotBefore 屬性會保持不變。</span><span class="sxs-lookup"><span data-stu-id="55c74-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="55c74-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55c74-144">-PassThru</span></span>
<span data-ttu-id="55c74-145">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="55c74-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="55c74-146">如果已指定此開關，則會傳回更新的金鑰束物件。</span><span class="sxs-lookup"><span data-stu-id="55c74-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="55c74-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="55c74-147">-Tag</span></span>
<span data-ttu-id="55c74-148">Hashtable 代表主要標記。</span><span class="sxs-lookup"><span data-stu-id="55c74-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="55c74-149">如果未指定，索引鍵的 existings 標記會保持不變。</span><span class="sxs-lookup"><span data-stu-id="55c74-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="55c74-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="55c74-150">-VaultName</span></span>
<span data-ttu-id="55c74-151">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="55c74-151">Vault name.</span></span>
<span data-ttu-id="55c74-152">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="55c74-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="55c74-153">-版本</span><span class="sxs-lookup"><span data-stu-id="55c74-153">-Version</span></span>
<span data-ttu-id="55c74-154">金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="55c74-154">Key version.</span></span>
<span data-ttu-id="55c74-155">Cmdlet 會從保存庫名稱、目前已選取的環境、金鑰名稱和金鑰版本構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="55c74-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="55c74-156">-確認</span><span class="sxs-lookup"><span data-stu-id="55c74-156">-Confirm</span></span>
<span data-ttu-id="55c74-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55c74-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c74-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c74-158">-WhatIf</span></span>
<span data-ttu-id="55c74-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55c74-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c74-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55c74-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c74-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c74-161">CommonParameters</span></span>
<span data-ttu-id="55c74-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55c74-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c74-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55c74-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c74-164">輸入</span><span class="sxs-lookup"><span data-stu-id="55c74-164">INPUTS</span></span>

### <span data-ttu-id="55c74-165">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="55c74-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="55c74-166">輸出</span><span class="sxs-lookup"><span data-stu-id="55c74-166">OUTPUTS</span></span>

### <span data-ttu-id="55c74-167">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="55c74-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="55c74-168">筆記</span><span class="sxs-lookup"><span data-stu-id="55c74-168">NOTES</span></span>

## <span data-ttu-id="55c74-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="55c74-169">RELATED LINKS</span></span>
