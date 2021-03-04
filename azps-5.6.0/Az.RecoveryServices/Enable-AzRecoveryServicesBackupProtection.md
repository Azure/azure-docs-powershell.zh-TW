---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 0472a24e15a05d1ea07639ee5495efc5feaaba6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910934"
---
# <span data-ttu-id="25578-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="25578-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="25578-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25578-102">SYNOPSIS</span></span>
<span data-ttu-id="25578-103">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="25578-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="25578-104">語法</span><span class="sxs-lookup"><span data-stu-id="25578-104">SYNTAX</span></span>

### <span data-ttu-id="25578-105">AzureCOMPuteEnableProtection (預設) </span><span class="sxs-lookup"><span data-stu-id="25578-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25578-106">AzureCOMPClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="25578-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25578-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="25578-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25578-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="25578-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25578-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="25578-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25578-110">描述</span><span class="sxs-lookup"><span data-stu-id="25578-110">DESCRIPTION</span></span>
<span data-ttu-id="25578-111">**Enable-AzRecoveryServicesBackupProtection** Cmdlet 會建立保護原則與專案的關聯，以啟用備份。</span><span class="sxs-lookup"><span data-stu-id="25578-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="25578-112">如果沒有任何策略識別碼或備份專案未與任何策略相關聯，則此命令會預期有 policyID。</span><span class="sxs-lookup"><span data-stu-id="25578-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="25578-113">使用目前的 Cmdlet 之前，使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定庫內容。</span><span class="sxs-lookup"><span data-stu-id="25578-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="25578-114">例子</span><span class="sxs-lookup"><span data-stu-id="25578-114">EXAMPLES</span></span>

### <span data-ttu-id="25578-115">範例 1：啟用專案的備份保護</span><span class="sxs-lookup"><span data-stu-id="25578-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="25578-116">第一個 Cmdlet 會獲得預設策略物件，然後將它儲存在$Pol變數中。</span><span class="sxs-lookup"><span data-stu-id="25578-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="25578-117">第二個 Cmdlet 會指定要備份的磁片 LUN，並儲存在$inclusionDiskLUNS變數中。</span><span class="sxs-lookup"><span data-stu-id="25578-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="25578-118">第三個 Cmdlet 會使用 $Pol 中的策略，為名為 V2 VM 的 ARM 虛擬機器設定備份保護$Pol。</span><span class="sxs-lookup"><span data-stu-id="25578-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="25578-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="25578-119">Example 2</span></span>

<span data-ttu-id="25578-120">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="25578-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="25578-121"> (自動) </span><span class="sxs-lookup"><span data-stu-id="25578-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="25578-122">參數</span><span class="sxs-lookup"><span data-stu-id="25578-122">PARAMETERS</span></span>

### <span data-ttu-id="25578-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25578-123">-DefaultProfile</span></span>
<span data-ttu-id="25578-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25578-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25578-125">-ExcludeAllData至上</span><span class="sxs-lookup"><span data-stu-id="25578-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="25578-126">僅指定備份作業系統磁片的選項</span><span class="sxs-lookup"><span data-stu-id="25578-126">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25578-127">-Exclusion至上清單</span><span class="sxs-lookup"><span data-stu-id="25578-127">-ExclusionDisksList</span></span>
<span data-ttu-id="25578-128">備份中要排除的磁片 LUN 清單，其餘部分會自動包含在內。</span><span class="sxs-lookup"><span data-stu-id="25578-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25578-129">-Inclusion內容清單</span><span class="sxs-lookup"><span data-stu-id="25578-129">-InclusionDisksList</span></span>
<span data-ttu-id="25578-130">備份中要包含的磁片 PIN 清單，其餘部分會自動排除，作業系統磁片除外。</span><span class="sxs-lookup"><span data-stu-id="25578-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25578-131">-專案</span><span class="sxs-lookup"><span data-stu-id="25578-131">-Item</span></span>
<span data-ttu-id="25578-132">指定此 Cmdlet 啟用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="25578-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="25578-133">若要取得 **AzureRmRecoveryServicesBackupItem，** 請使用 Get-AzRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25578-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25578-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="25578-134">-Name</span></span>
<span data-ttu-id="25578-135">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="25578-135">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25578-136">-策略</span><span class="sxs-lookup"><span data-stu-id="25578-136">-Policy</span></span>
<span data-ttu-id="25578-137">指定此 Cmdlet 與專案建立關聯之保護政策。</span><span class="sxs-lookup"><span data-stu-id="25578-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="25578-138">若要取得 **AzureRmRecoveryServicesBackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25578-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25578-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="25578-139">-ProtectableItem</span></span>
<span data-ttu-id="25578-140">指定要以指定政策保護的專案。</span><span class="sxs-lookup"><span data-stu-id="25578-140">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25578-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="25578-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="25578-142">指定重設與專案相關聯的磁片排除設定</span><span class="sxs-lookup"><span data-stu-id="25578-142">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25578-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25578-143">-ResourceGroupName</span></span>
<span data-ttu-id="25578-144">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25578-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="25578-145">僅針對 ARM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="25578-145">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25578-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25578-146">-StorageAccountName</span></span>
<span data-ttu-id="25578-147">Azure 檔案共用儲存帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="25578-147">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25578-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="25578-148">-VaultId</span></span>
<span data-ttu-id="25578-149">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="25578-149">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25578-150">-確認</span><span class="sxs-lookup"><span data-stu-id="25578-150">-Confirm</span></span>
<span data-ttu-id="25578-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="25578-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25578-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25578-152">-WhatIf</span></span>
<span data-ttu-id="25578-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25578-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="25578-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25578-154">CommonParameters</span></span>
<span data-ttu-id="25578-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25578-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25578-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25578-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25578-157">輸入</span><span class="sxs-lookup"><span data-stu-id="25578-157">INPUTS</span></span>

### <span data-ttu-id="25578-158">System.String</span><span class="sxs-lookup"><span data-stu-id="25578-158">System.String</span></span>

### <span data-ttu-id="25578-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="25578-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="25578-160">輸出</span><span class="sxs-lookup"><span data-stu-id="25578-160">OUTPUTS</span></span>

### <span data-ttu-id="25578-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="25578-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="25578-162">筆記</span><span class="sxs-lookup"><span data-stu-id="25578-162">NOTES</span></span>

## <span data-ttu-id="25578-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="25578-163">RELATED LINKS</span></span>

[<span data-ttu-id="25578-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="25578-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="25578-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="25578-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


