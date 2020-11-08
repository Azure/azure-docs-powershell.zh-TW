---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136735"
---
# <span data-ttu-id="e964b-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e964b-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="e964b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e964b-102">SYNOPSIS</span></span>
<span data-ttu-id="e964b-103">刪除受管理的 HSM 中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e964b-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="e964b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e964b-104">SYNTAX</span></span>

### <span data-ttu-id="e964b-105">RemoveByKeyNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e964b-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e964b-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e964b-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e964b-107">說明</span><span class="sxs-lookup"><span data-stu-id="e964b-107">DESCRIPTION</span></span>
<span data-ttu-id="e964b-108">Remove-AzManagedHsmKey Cmdlet 會刪除受管理的 HSM 中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e964b-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="e964b-109">如果不小心刪除了金鑰，則可以使用具有特殊「復原」許可權的使用者 Undo-AzManagedHsmKeyRemoval 來復原金鑰。</span><span class="sxs-lookup"><span data-stu-id="e964b-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="e964b-110">這個 Cmdlet 的值為 high，用於 **ConfirmImpact** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e964b-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="e964b-111">示例</span><span class="sxs-lookup"><span data-stu-id="e964b-111">EXAMPLES</span></span>

### <span data-ttu-id="e964b-112">範例1：從受管理的 HSM 移除金鑰</span><span class="sxs-lookup"><span data-stu-id="e964b-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="e964b-113">這個命令會從受管理的 HSM （名為 testmhsm）移除名為 testkey 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e964b-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="e964b-114">範例2：在未確認使用者的情況下移除金鑰</span><span class="sxs-lookup"><span data-stu-id="e964b-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="e964b-115">這個命令會從受管理的 HSM （名為 testmhsm）移除名為 testkey 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e964b-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="e964b-116">此命令會指定 *Force* 參數，因此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e964b-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e964b-117">範例3：永久清除受管理的 HSM 中的已刪除金鑰</span><span class="sxs-lookup"><span data-stu-id="e964b-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="e964b-118">這個命令會將名為 testkey 的金鑰從已 testmhsm 的 managed HSM 中永久移除。</span><span class="sxs-lookup"><span data-stu-id="e964b-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="e964b-119">執行此 Cmdlet 需要「清除」許可權，此許可權必須事先已明確地授予此受管理 HSM 的使用者。</span><span class="sxs-lookup"><span data-stu-id="e964b-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="e964b-120">範例4：使用管線運算子移除按鍵</span><span class="sxs-lookup"><span data-stu-id="e964b-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="e964b-121">這個命令會取得名為 testmhsm 的受管理 HSM 中的所有金鑰，並使用管線運算子將它們傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e964b-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e964b-122">這個 Cmdlet 會將已 **啟用** 屬性的值 $False 的金鑰傳遞給目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e964b-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="e964b-123">該 Cmdlet 會移除這些索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e964b-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="e964b-124">參數</span><span class="sxs-lookup"><span data-stu-id="e964b-124">PARAMETERS</span></span>

### <span data-ttu-id="e964b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e964b-125">-DefaultProfile</span></span>
<span data-ttu-id="e964b-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e964b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e964b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e964b-127">-Force</span></span>
<span data-ttu-id="e964b-128">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="e964b-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e964b-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e964b-129">-HsmName</span></span>
<span data-ttu-id="e964b-130">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="e964b-130">HSM name.</span></span> <span data-ttu-id="e964b-131">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e964b-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e964b-132">-InputObject</span></span>
<span data-ttu-id="e964b-133">主要物件</span><span class="sxs-lookup"><span data-stu-id="e964b-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e964b-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e964b-134">-InRemovedState</span></span>
<span data-ttu-id="e964b-135">永久移除先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e964b-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="e964b-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="e964b-136">-Name</span></span>
<span data-ttu-id="e964b-137">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="e964b-137">Key name.</span></span>
<span data-ttu-id="e964b-138">Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e964b-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964b-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e964b-139">-PassThru</span></span>
<span data-ttu-id="e964b-140">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="e964b-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e964b-141">如果指定此開關，則 Cmdlet 會傳回已刪除的金鑰組象。</span><span class="sxs-lookup"><span data-stu-id="e964b-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="e964b-142">-確認</span><span class="sxs-lookup"><span data-stu-id="e964b-142">-Confirm</span></span>
<span data-ttu-id="e964b-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e964b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e964b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e964b-144">-WhatIf</span></span>
<span data-ttu-id="e964b-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e964b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e964b-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e964b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e964b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e964b-147">CommonParameters</span></span>
<span data-ttu-id="e964b-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e964b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e964b-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e964b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e964b-150">輸入</span><span class="sxs-lookup"><span data-stu-id="e964b-150">INPUTS</span></span>

### <span data-ttu-id="e964b-151">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e964b-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="e964b-152">輸出</span><span class="sxs-lookup"><span data-stu-id="e964b-152">OUTPUTS</span></span>

### <span data-ttu-id="e964b-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e964b-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="e964b-154">筆記</span><span class="sxs-lookup"><span data-stu-id="e964b-154">NOTES</span></span>

## <span data-ttu-id="e964b-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="e964b-155">RELATED LINKS</span></span>

[<span data-ttu-id="e964b-156">附加 AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e964b-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="e964b-157">備份-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e964b-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="e964b-158">AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e964b-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="e964b-159">復原-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="e964b-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="e964b-160">更新-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e964b-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="e964b-161">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e964b-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)