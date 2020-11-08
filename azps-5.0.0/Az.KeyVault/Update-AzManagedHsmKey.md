---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140484"
---
# <span data-ttu-id="f1fd9-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f1fd9-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="f1fd9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fd9-103">更新受管理的 HSM 中之金鑰的屬性。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="f1fd9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1fd9-104">SYNTAX</span></span>

### <span data-ttu-id="f1fd9-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f1fd9-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1fd9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f1fd9-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1fd9-107">說明</span><span class="sxs-lookup"><span data-stu-id="f1fd9-107">DESCRIPTION</span></span>
<span data-ttu-id="f1fd9-108">**AzManagedHsmKey** Cmdlet 會更新受管理 HSM 中之金鑰的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="f1fd9-109">示例</span><span class="sxs-lookup"><span data-stu-id="f1fd9-109">EXAMPLES</span></span>

### <span data-ttu-id="f1fd9-110">範例1：修改金鑰以啟用它，並設定到期日和標籤</span><span class="sxs-lookup"><span data-stu-id="f1fd9-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="f1fd9-111">第一個命令會使用 [ **取得日期** ] Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="f1fd9-112">該物件指定未來兩年的時間。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="f1fd9-113">該命令會將該日期儲存在 $Expires 變數中。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="f1fd9-114">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f1fd9-115">第二個命令會建立變數來儲存高嚴重性與會計的標記值。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="f1fd9-116">最後一個命令會修改一個名為 testkey001 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="f1fd9-117">該命令會啟用金鑰、將過期時間設定為儲存在 $Expires 的時間，並設定 $Tags 中儲存的標籤。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="f1fd9-118">參數</span><span class="sxs-lookup"><span data-stu-id="f1fd9-118">PARAMETERS</span></span>

### <span data-ttu-id="f1fd9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fd9-119">-DefaultProfile</span></span>
<span data-ttu-id="f1fd9-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1fd9-121">-啟用</span><span class="sxs-lookup"><span data-stu-id="f1fd9-121">-Enable</span></span>
<span data-ttu-id="f1fd9-122">True 的值會啟用索引鍵和 false 的值 disabless。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="f1fd9-123">如果未指定，現有的啟用/停用狀態會保持不變。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="f1fd9-124">-到期</span><span class="sxs-lookup"><span data-stu-id="f1fd9-124">-Expires</span></span>
<span data-ttu-id="f1fd9-125">以 UTC 時程表示之金鑰的到期時間。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="f1fd9-126">如果沒有指定，則金鑰的現有到期時間會保持不變。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="f1fd9-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f1fd9-127">-HsmName</span></span>
<span data-ttu-id="f1fd9-128">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-128">HSM name.</span></span> <span data-ttu-id="f1fd9-129">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f1fd9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1fd9-130">-InputObject</span></span>
<span data-ttu-id="f1fd9-131">主要物件</span><span class="sxs-lookup"><span data-stu-id="f1fd9-131">Key object</span></span>

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

### <span data-ttu-id="f1fd9-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="f1fd9-132">-KeyOps</span></span>
<span data-ttu-id="f1fd9-133">可使用金鑰執行的作業。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="f1fd9-134">如果沒有指定，則金鑰的現有按鍵動作會保持不變。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="f1fd9-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1fd9-135">-Name</span></span>
<span data-ttu-id="f1fd9-136">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-136">Key name.</span></span>
<span data-ttu-id="f1fd9-137">Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="f1fd9-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f1fd9-138">-NotBefore</span></span>
<span data-ttu-id="f1fd9-139">在無法使用 key 之前的 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="f1fd9-140">如果未指定，索引鍵的現有 NotBefore 屬性會保持不變。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="f1fd9-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1fd9-141">-PassThru</span></span>
<span data-ttu-id="f1fd9-142">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f1fd9-143">如果已指定此開關，則會傳回更新的金鑰束物件。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="f1fd9-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1fd9-144">-Tag</span></span>
<span data-ttu-id="f1fd9-145">Hashtable 代表主要標記。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="f1fd9-146">如果未指定，索引鍵的 existings 標記會保持不變。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-146">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="f1fd9-147">-版本</span><span class="sxs-lookup"><span data-stu-id="f1fd9-147">-Version</span></span>
<span data-ttu-id="f1fd9-148">金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-148">Key version.</span></span>
<span data-ttu-id="f1fd9-149">Cmdlet 會從 managed HSM 名稱、目前已選取的環境、金鑰名稱和金鑰版本構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="f1fd9-150">-確認</span><span class="sxs-lookup"><span data-stu-id="f1fd9-150">-Confirm</span></span>
<span data-ttu-id="f1fd9-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1fd9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1fd9-152">-WhatIf</span></span>
<span data-ttu-id="f1fd9-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1fd9-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1fd9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fd9-155">CommonParameters</span></span>
<span data-ttu-id="f1fd9-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fd9-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fd9-158">輸入</span><span class="sxs-lookup"><span data-stu-id="f1fd9-158">INPUTS</span></span>

### <span data-ttu-id="f1fd9-159">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="f1fd9-160">輸出</span><span class="sxs-lookup"><span data-stu-id="f1fd9-160">OUTPUTS</span></span>

### <span data-ttu-id="f1fd9-161">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f1fd9-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f1fd9-162">筆記</span><span class="sxs-lookup"><span data-stu-id="f1fd9-162">NOTES</span></span>

## <span data-ttu-id="f1fd9-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1fd9-163">RELATED LINKS</span></span>

[<span data-ttu-id="f1fd9-164">附加 AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f1fd9-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="f1fd9-165">備份-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f1fd9-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="f1fd9-166">移除-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f1fd9-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="f1fd9-167">復原-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="f1fd9-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="f1fd9-168">AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f1fd9-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="f1fd9-169">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="f1fd9-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)