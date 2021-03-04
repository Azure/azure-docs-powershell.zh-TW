---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: 631cb05e15231bb4e695ad3047a7736177a785e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908165"
---
# <span data-ttu-id="327bb-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="327bb-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="327bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="327bb-102">SYNOPSIS</span></span>
<span data-ttu-id="327bb-103">更新金鑰庫中金鑰的屬性。</span><span class="sxs-lookup"><span data-stu-id="327bb-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="327bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="327bb-104">SYNTAX</span></span>

### <span data-ttu-id="327bb-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="327bb-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="327bb-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="327bb-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="327bb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="327bb-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="327bb-108">描述</span><span class="sxs-lookup"><span data-stu-id="327bb-108">DESCRIPTION</span></span>
<span data-ttu-id="327bb-109">**Update-AzKeyVaultKey** Cmdlet 會更新金鑰保存庫中金鑰的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="327bb-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="327bb-110">例子</span><span class="sxs-lookup"><span data-stu-id="327bb-110">EXAMPLES</span></span>

### <span data-ttu-id="327bb-111">範例 1：修改金鑰以啟用它，並設定到期日和標記</span><span class="sxs-lookup"><span data-stu-id="327bb-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
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

<span data-ttu-id="327bb-112">第一個命令會使用 **Get-Date** Cmdlet 建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="327bb-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="327bb-113">該物件會指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="327bb-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="327bb-114">命令會儲存該日期至$Expires變數。</span><span class="sxs-lookup"><span data-stu-id="327bb-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="327bb-115">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="327bb-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="327bb-116">第二個命令會建立變數來儲存高嚴重性和會計的標記值。</span><span class="sxs-lookup"><span data-stu-id="327bb-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="327bb-117">最後一個命令會修改名為 ITSoftware 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="327bb-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="327bb-118">命令會啟用金鑰、將到期日設定為 $Expires 中儲存的時間，以及設定儲存在 $Tags 中的標記。</span><span class="sxs-lookup"><span data-stu-id="327bb-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="327bb-119">範例 2：修改金鑰以刪除所有標記</span><span class="sxs-lookup"><span data-stu-id="327bb-119">Example 2: Modify a key to delete all tags</span></span>
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

<span data-ttu-id="327bb-120">這個命令會刪除名為 ITSoftware 之特定金鑰版本的所有標記。</span><span class="sxs-lookup"><span data-stu-id="327bb-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="327bb-121">參數</span><span class="sxs-lookup"><span data-stu-id="327bb-121">PARAMETERS</span></span>

### <span data-ttu-id="327bb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327bb-122">-DefaultProfile</span></span>
<span data-ttu-id="327bb-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="327bb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327bb-124">-啟用</span><span class="sxs-lookup"><span data-stu-id="327bb-124">-Enable</span></span>
<span data-ttu-id="327bb-125">true 的值會啟用該鍵，而 false 的值會停用該金鑰。</span><span class="sxs-lookup"><span data-stu-id="327bb-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="327bb-126">如果未指定，現有啟用/停用狀態會維持不變。</span><span class="sxs-lookup"><span data-stu-id="327bb-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="327bb-127">-到期</span><span class="sxs-lookup"><span data-stu-id="327bb-127">-Expires</span></span>
<span data-ttu-id="327bb-128">以 UTC 時程表示之金鑰的到期日。</span><span class="sxs-lookup"><span data-stu-id="327bb-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="327bb-129">如果未指定，則金鑰的現有到期時間會維持不變。</span><span class="sxs-lookup"><span data-stu-id="327bb-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="327bb-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="327bb-130">-HsmName</span></span>
<span data-ttu-id="327bb-131">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="327bb-131">HSM name.</span></span> <span data-ttu-id="327bb-132">Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="327bb-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="327bb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="327bb-133">-InputObject</span></span>
<span data-ttu-id="327bb-134">Key 物件</span><span class="sxs-lookup"><span data-stu-id="327bb-134">Key object</span></span>

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

### <span data-ttu-id="327bb-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="327bb-135">-KeyOps</span></span>
<span data-ttu-id="327bb-136">可以使用金鑰執行的作業。</span><span class="sxs-lookup"><span data-stu-id="327bb-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="327bb-137">如果未指定，則金鑰的現有金鑰操作會維持不變。</span><span class="sxs-lookup"><span data-stu-id="327bb-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="327bb-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="327bb-138">-Name</span></span>
<span data-ttu-id="327bb-139">金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="327bb-139">Key name.</span></span>
<span data-ttu-id="327bb-140">Cmdlet 會從儲存庫名稱、目前選取的環境和金鑰名稱建構金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="327bb-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="327bb-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="327bb-141">-NotBefore</span></span>
<span data-ttu-id="327bb-142">這是無法使用金鑰的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="327bb-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="327bb-143">如果未指定，則金鑰的現有 NotBefore 屬性會維持不變。</span><span class="sxs-lookup"><span data-stu-id="327bb-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="327bb-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="327bb-144">-PassThru</span></span>
<span data-ttu-id="327bb-145">Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="327bb-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="327bb-146">如果指定此參數，會返回更新的金鑰組合物件。</span><span class="sxs-lookup"><span data-stu-id="327bb-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="327bb-147">-標記</span><span class="sxs-lookup"><span data-stu-id="327bb-147">-Tag</span></span>
<span data-ttu-id="327bb-148">雜湊表代表金鑰標記。</span><span class="sxs-lookup"><span data-stu-id="327bb-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="327bb-149">如果未指定，則金鑰的現有標記會維持不變。</span><span class="sxs-lookup"><span data-stu-id="327bb-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="327bb-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="327bb-150">-VaultName</span></span>
<span data-ttu-id="327bb-151">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="327bb-151">Vault name.</span></span>
<span data-ttu-id="327bb-152">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="327bb-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="327bb-153">-版本</span><span class="sxs-lookup"><span data-stu-id="327bb-153">-Version</span></span>
<span data-ttu-id="327bb-154">金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="327bb-154">Key version.</span></span>
<span data-ttu-id="327bb-155">Cmdlet 會從儲存庫名稱、目前選取的環境、金鑰名稱和金鑰版本建構金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="327bb-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="327bb-156">-確認</span><span class="sxs-lookup"><span data-stu-id="327bb-156">-Confirm</span></span>
<span data-ttu-id="327bb-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="327bb-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="327bb-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="327bb-158">-WhatIf</span></span>
<span data-ttu-id="327bb-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="327bb-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="327bb-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="327bb-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="327bb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327bb-161">CommonParameters</span></span>
<span data-ttu-id="327bb-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="327bb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327bb-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="327bb-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327bb-164">輸入</span><span class="sxs-lookup"><span data-stu-id="327bb-164">INPUTS</span></span>

### <span data-ttu-id="327bb-165">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="327bb-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="327bb-166">輸出</span><span class="sxs-lookup"><span data-stu-id="327bb-166">OUTPUTS</span></span>

### <span data-ttu-id="327bb-167">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="327bb-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="327bb-168">筆記</span><span class="sxs-lookup"><span data-stu-id="327bb-168">NOTES</span></span>

## <span data-ttu-id="327bb-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="327bb-169">RELATED LINKS</span></span>
