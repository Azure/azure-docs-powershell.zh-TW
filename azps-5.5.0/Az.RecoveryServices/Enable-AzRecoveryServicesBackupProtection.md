---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 41ee67359d4545a5b69ec1f9c44ff8e37302837e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135542"
---
# <span data-ttu-id="588cb-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="588cb-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="588cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="588cb-102">SYNOPSIS</span></span>
<span data-ttu-id="588cb-103">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="588cb-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="588cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="588cb-104">SYNTAX</span></span>

### <span data-ttu-id="588cb-105">AzureVMComputeEnableProtection (預設) </span><span class="sxs-lookup"><span data-stu-id="588cb-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="588cb-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="588cb-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588cb-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="588cb-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588cb-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="588cb-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588cb-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="588cb-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="588cb-110">說明</span><span class="sxs-lookup"><span data-stu-id="588cb-110">DESCRIPTION</span></span>
<span data-ttu-id="588cb-111">**Enable-AzRecoveryServicesBackupProtection** Cmdlet 會將保護原則與專案建立關聯，以啟用備份。</span><span class="sxs-lookup"><span data-stu-id="588cb-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="588cb-112">如果原則識別碼不存在，或備份專案未與任何原則相關聯，則此命令會預期 policyID。</span><span class="sxs-lookup"><span data-stu-id="588cb-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="588cb-113">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="588cb-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="588cb-114">示例</span><span class="sxs-lookup"><span data-stu-id="588cb-114">EXAMPLES</span></span>

### <span data-ttu-id="588cb-115">範例1：為專案啟用備份保護</span><span class="sxs-lookup"><span data-stu-id="588cb-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="588cb-116">第一個 Cmdlet 會取得預設原則物件，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="588cb-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="588cb-117">第二個 Cmdlet 會指定要備份的磁片 Lun，並將其儲存在 $inclusionDiskLUNS 變數中。</span><span class="sxs-lookup"><span data-stu-id="588cb-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="588cb-118">第三個 Cmdlet 會使用 $Pol 中的原則，為名為 V2VM 的 ARM 虛擬機器設定備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="588cb-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="588cb-119">範例2</span><span class="sxs-lookup"><span data-stu-id="588cb-119">Example 2</span></span>

<span data-ttu-id="588cb-120">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="588cb-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="588cb-121"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="588cb-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="588cb-122">參數</span><span class="sxs-lookup"><span data-stu-id="588cb-122">PARAMETERS</span></span>

### <span data-ttu-id="588cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588cb-123">-DefaultProfile</span></span>
<span data-ttu-id="588cb-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="588cb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="588cb-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="588cb-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="588cb-126">僅指定備份 OS 磁片的選項</span><span class="sxs-lookup"><span data-stu-id="588cb-126">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="588cb-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="588cb-127">-ExclusionDisksList</span></span>
<span data-ttu-id="588cb-128">要在備份中排除的磁片 Lun 清單，其餘部分會自動包含在其中。</span><span class="sxs-lookup"><span data-stu-id="588cb-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="588cb-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="588cb-129">-InclusionDisksList</span></span>
<span data-ttu-id="588cb-130">在 [備份] 中包含的磁片 Lun 清單，其餘部分會自動排除在作業系統磁片以外。</span><span class="sxs-lookup"><span data-stu-id="588cb-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="588cb-131">-專案</span><span class="sxs-lookup"><span data-stu-id="588cb-131">-Item</span></span>
<span data-ttu-id="588cb-132">指定此 Cmdlet 針對其啟用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="588cb-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="588cb-133">若要取得 **AzureRmRecoveryServicesBackupItem**，請使用 Get-AzRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="588cb-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="588cb-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="588cb-134">-Name</span></span>
<span data-ttu-id="588cb-135">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="588cb-135">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="588cb-136">-原則</span><span class="sxs-lookup"><span data-stu-id="588cb-136">-Policy</span></span>
<span data-ttu-id="588cb-137">指定此 Cmdlet 與專案相關聯的保護原則。</span><span class="sxs-lookup"><span data-stu-id="588cb-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="588cb-138">若要取得 **AzureRmRecoveryServicesBackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="588cb-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="588cb-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="588cb-139">-ProtectableItem</span></span>
<span data-ttu-id="588cb-140">指定要使用指定原則保護的專案。</span><span class="sxs-lookup"><span data-stu-id="588cb-140">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="588cb-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="588cb-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="588cb-142">指定重設與專案相關聯的磁片排除設定</span><span class="sxs-lookup"><span data-stu-id="588cb-142">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="588cb-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="588cb-143">-ResourceGroupName</span></span>
<span data-ttu-id="588cb-144">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="588cb-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="588cb-145">請僅針對 ARM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="588cb-145">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="588cb-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="588cb-146">-StorageAccountName</span></span>
<span data-ttu-id="588cb-147">Azure 檔案共用儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="588cb-147">Azure file share storage account name</span></span>

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

### <span data-ttu-id="588cb-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="588cb-148">-VaultId</span></span>
<span data-ttu-id="588cb-149">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="588cb-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="588cb-150">-確認</span><span class="sxs-lookup"><span data-stu-id="588cb-150">-Confirm</span></span>
<span data-ttu-id="588cb-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="588cb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="588cb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="588cb-152">-WhatIf</span></span>
<span data-ttu-id="588cb-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="588cb-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="588cb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588cb-154">CommonParameters</span></span>
<span data-ttu-id="588cb-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="588cb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588cb-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="588cb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588cb-157">輸入</span><span class="sxs-lookup"><span data-stu-id="588cb-157">INPUTS</span></span>

### <span data-ttu-id="588cb-158">System.object</span><span class="sxs-lookup"><span data-stu-id="588cb-158">System.String</span></span>

### <span data-ttu-id="588cb-159">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="588cb-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="588cb-160">輸出</span><span class="sxs-lookup"><span data-stu-id="588cb-160">OUTPUTS</span></span>

### <span data-ttu-id="588cb-161">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="588cb-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="588cb-162">筆記</span><span class="sxs-lookup"><span data-stu-id="588cb-162">NOTES</span></span>

## <span data-ttu-id="588cb-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="588cb-163">RELATED LINKS</span></span>

[<span data-ttu-id="588cb-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="588cb-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="588cb-165">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="588cb-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


