---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: cbe1160c691fe128f5f2950d728501b815294c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134687"
---
# <span data-ttu-id="3feb2-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3feb2-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3feb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3feb2-102">SYNOPSIS</span></span>

<span data-ttu-id="3feb2-103">將備份專案的資料和設定還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="3feb2-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="3feb2-104">所需的參數會依備份專案類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="3feb2-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="3feb2-105">您也可以使用相同的命令來還原 Azure 虛擬機器、在 Azure 虛擬機器和 Azure 檔案共用中執行的資料庫。</span><span class="sxs-lookup"><span data-stu-id="3feb2-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="3feb2-106">句法</span><span class="sxs-lookup"><span data-stu-id="3feb2-106">SYNTAX</span></span>

### <span data-ttu-id="3feb2-107">AzureVMParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3feb2-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3feb2-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="3feb2-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3feb2-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="3feb2-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3feb2-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="3feb2-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3feb2-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="3feb2-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3feb2-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="3feb2-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3feb2-113">說明</span><span class="sxs-lookup"><span data-stu-id="3feb2-113">DESCRIPTION</span></span>

<span data-ttu-id="3feb2-114">**Restore-AzRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="3feb2-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="3feb2-115">**針對 Azure VM 備份**</span><span class="sxs-lookup"><span data-stu-id="3feb2-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="3feb2-116">您可以使用此命令來備份 Azure 虛擬機器和復原磁碟 (受管理和未管理) 。</span><span class="sxs-lookup"><span data-stu-id="3feb2-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="3feb2-117">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3feb2-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="3feb2-118">如果這是受管理的磁片 VM，則應該在保留復原磁碟的位置指定目標資源群組。</span><span class="sxs-lookup"><span data-stu-id="3feb2-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="3feb2-119">指定目標資源群組時，如果快照存在於備份原則中指定的資源群組中，還原作業就會立即開始，而且磁片是從本機快照建立，並保留在目標資源群組中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="3feb2-120">您也可以選擇將它們還原為未受管理的磁片，但這會利用 Azure 復原服務保存庫中的資料，因此會變得更慢。</span><span class="sxs-lookup"><span data-stu-id="3feb2-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="3feb2-121">VM 與部署範本的設定，可用於從已還原的磁片建立 VM，將會下載到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="3feb2-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="3feb2-122">如果這是未受管理的磁片 VM，則快照會存在於磁片的原始儲存空間帳戶和/或 [恢復服務] 保存庫中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="3feb2-123">如果使用者提供使用原始儲存空間帳戶進行還原的選項，則可以提供立即還原。</span><span class="sxs-lookup"><span data-stu-id="3feb2-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="3feb2-124">否則，系統會從 Azure 復原服務電子倉庫取得資料，並在指定的儲存空間帳戶以及 VM 與部署範本的設定中建立磁片。</span><span class="sxs-lookup"><span data-stu-id="3feb2-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3feb2-125">根據預設，Azure VM 備份會備份所有磁片。</span><span class="sxs-lookup"><span data-stu-id="3feb2-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="3feb2-126">您可以在啟用-備份期間，使用 exclusionList 或 InclusionList 參數選擇性地備份相關磁片。</span><span class="sxs-lookup"><span data-stu-id="3feb2-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="3feb2-127">只有有選擇性地備份磁片時，才能使用選擇性復原磁碟的選項。</span><span class="sxs-lookup"><span data-stu-id="3feb2-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="3feb2-128">如需詳細資訊，請參閱不同可能的參數集與參數文字。</span><span class="sxs-lookup"><span data-stu-id="3feb2-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="3feb2-129">如果使用-VaultId 參數，則也應該使用-VaultLocation 參數。</span><span class="sxs-lookup"><span data-stu-id="3feb2-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="3feb2-130">**針對 Azure 檔案共用備份**</span><span class="sxs-lookup"><span data-stu-id="3feb2-130">**For Azure File share backup**</span></span>

<span data-ttu-id="3feb2-131">您可以在共用上還原整個檔案共用或特定/多個檔案/資料夾。</span><span class="sxs-lookup"><span data-stu-id="3feb2-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="3feb2-132">您可以還原至原始位置或移至備用位置。</span><span class="sxs-lookup"><span data-stu-id="3feb2-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="3feb2-133">**針對 Azure 工作負載**</span><span class="sxs-lookup"><span data-stu-id="3feb2-133">**For Azure Workloads**</span></span>

<span data-ttu-id="3feb2-134">您可以在 Azure Vm 中還原 SQL 存儲</span><span class="sxs-lookup"><span data-stu-id="3feb2-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="3feb2-135">示例</span><span class="sxs-lookup"><span data-stu-id="3feb2-135">EXAMPLES</span></span>

### <span data-ttu-id="3feb2-136">範例1：從指定的復原點還原已備份之受管理磁片 Azure VM 的磁片</span><span class="sxs-lookup"><span data-stu-id="3feb2-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3feb2-137">第一個命令會取得 [恢復服務] 電子倉庫，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="3feb2-138">第二個命令會取得類型為 "V2VM" 的備份專案，並將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3feb2-139">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3feb2-140">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3feb2-141">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="3feb2-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="3feb2-142">最後一個命令會將所有磁片還原至 [目標資源] 群組 Target_RG，然後在 [DestRG 資源] 群組的 [儲存帳戶] DestAccount 中提供 VM 配置資訊和部署範本。</span><span class="sxs-lookup"><span data-stu-id="3feb2-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="3feb2-143">範例2：從指定的復原點還原已備份之受管理磁片 Azure VM 的指定磁片</span><span class="sxs-lookup"><span data-stu-id="3feb2-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3feb2-144">第一個命令會取得 [恢復服務] 電子倉庫，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="3feb2-145">第二個命令會取得類型為 "V2VM" 的備份專案，並將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3feb2-146">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3feb2-147">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3feb2-148">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="3feb2-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="3feb2-149">第六個命令會儲存要在 restoreDiskLUN 變數中還原的磁片清單。</span><span class="sxs-lookup"><span data-stu-id="3feb2-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="3feb2-150">最後一個命令會將指定 Lun 的指定磁片還原至 [目標資源] 群組 Target_RG，然後在 [DestRG] 資源群組的 [儲存空間帳戶] DestAccount 中提供 VM 配置資訊和部署範本。</span><span class="sxs-lookup"><span data-stu-id="3feb2-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="3feb2-151">範例3：將受管理的 VM 磁片還原為非託管磁片</span><span class="sxs-lookup"><span data-stu-id="3feb2-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3feb2-152">第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="3feb2-153">第二個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3feb2-154">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3feb2-155">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3feb2-156">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="3feb2-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="3feb2-157">第六個命令會將磁片還原為非託管磁片。</span><span class="sxs-lookup"><span data-stu-id="3feb2-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="3feb2-158">範例4：使用原始儲存空間帳戶將未受管理的 VM 還原為非託管磁片</span><span class="sxs-lookup"><span data-stu-id="3feb2-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3feb2-159">第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="3feb2-160">第二個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3feb2-161">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3feb2-162">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3feb2-163">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="3feb2-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="3feb2-164">第六個命令會將磁片還原為非託管磁片至其原始儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="3feb2-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="3feb2-165">範例5：還原 AzureFileShare 專案的多個檔案</span><span class="sxs-lookup"><span data-stu-id="3feb2-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3feb2-166">第一個命令會取得 [恢復服務] 電子倉庫，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="3feb2-167">第二個命令會取得名為 fileshareitem 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3feb2-168">第三個命令會針對特定備份專案取得復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="3feb2-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="3feb2-169">第四個命令會指定要還原哪些檔案，並將其儲存在 $files 變數中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="3feb2-170">最後一個命令會將指定的檔案還原至其原始位置。</span><span class="sxs-lookup"><span data-stu-id="3feb2-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="3feb2-171">範例6：針對不同的完整復原點，將 Azure VM 中的 SQL 資料庫還原至另一個目標 VM</span><span class="sxs-lookup"><span data-stu-id="3feb2-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### <span data-ttu-id="3feb2-172">範例7：將 Azure VM 中的 SQL 資料庫還原至另一個目標 VM 以取得記錄復原點</span><span class="sxs-lookup"><span data-stu-id="3feb2-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## <span data-ttu-id="3feb2-173">參數</span><span class="sxs-lookup"><span data-stu-id="3feb2-173">PARAMETERS</span></span>

### <span data-ttu-id="3feb2-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3feb2-174">-DefaultProfile</span></span>

<span data-ttu-id="3feb2-175">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3feb2-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3feb2-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="3feb2-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="3feb2-177">用於多個檔案從檔案共用中還原。</span><span class="sxs-lookup"><span data-stu-id="3feb2-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="3feb2-178">檔案共用中要還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3feb2-178">The paths of the items to be restored within the file share.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3feb2-179">-RecoveryPoint</span></span>

<span data-ttu-id="3feb2-180">指定要還原備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="3feb2-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="3feb2-181">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 **AzRecoveryServicesBackupRecoveryPoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3feb2-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="3feb2-182">-ResolveConflict</span></span>

<span data-ttu-id="3feb2-183">如果還原的專案也存在於目的地中，請使用此選項來指出是否要覆寫。</span><span class="sxs-lookup"><span data-stu-id="3feb2-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="3feb2-184">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3feb2-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3feb2-185">原有</span><span class="sxs-lookup"><span data-stu-id="3feb2-185">Overwrite</span></span>
- <span data-ttu-id="3feb2-186">跳</span><span class="sxs-lookup"><span data-stu-id="3feb2-186">Skip</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="3feb2-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="3feb2-188">使用此開關指定要還原為非託管磁片</span><span class="sxs-lookup"><span data-stu-id="3feb2-188">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="3feb2-189">-RestoreDiskList</span></span>
<span data-ttu-id="3feb2-190">指定要復原備份的 VM 的磁片</span><span class="sxs-lookup"><span data-stu-id="3feb2-190">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="3feb2-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="3feb2-192">使用此開關只還原已備份 VM 的 OS 磁片</span><span class="sxs-lookup"><span data-stu-id="3feb2-192">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="3feb2-193">-SourceFilePath</span></span>

<span data-ttu-id="3feb2-194">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="3feb2-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="3feb2-195">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3feb2-195">The path of the item to be restored within the file share.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="3feb2-196">-SourceFileType</span></span>

<span data-ttu-id="3feb2-197">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="3feb2-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="3feb2-198">要在檔案共用中還原的專案類型。</span><span class="sxs-lookup"><span data-stu-id="3feb2-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="3feb2-199">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3feb2-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3feb2-200">檔案</span><span class="sxs-lookup"><span data-stu-id="3feb2-200">File</span></span>
- <span data-ttu-id="3feb2-201">空目錄</span><span class="sxs-lookup"><span data-stu-id="3feb2-201">Directory</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3feb2-202">-StorageAccountName</span></span>

<span data-ttu-id="3feb2-203">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3feb2-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="3feb2-204">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3feb2-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="3feb2-206">指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3feb2-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="3feb2-207">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="3feb2-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="3feb2-208">-TargetFileShareName</span></span>

<span data-ttu-id="3feb2-209">檔案共用要還原到的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="3feb2-209">The File Share to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="3feb2-210">-TargetFolder</span></span>

<span data-ttu-id="3feb2-211">要在 TargetFileShareName 中還原檔案共用的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3feb2-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="3feb2-212">如果備份的內容要還原到根資料夾，請將目的檔案夾的值指定為空字串。</span><span class="sxs-lookup"><span data-stu-id="3feb2-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3feb2-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="3feb2-214">要還原受管理磁片的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3feb2-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="3feb2-215">適用于使用受管理磁片的 VM 備份</span><span class="sxs-lookup"><span data-stu-id="3feb2-215">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3feb2-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="3feb2-217">檔案共用要還原到的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="3feb2-217">The storage account to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3feb2-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="3feb2-219">如果要將復原點的磁片還原到其原始儲存空間帳戶，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="3feb2-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="3feb2-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="3feb2-221">用來加密已復原磁碟的 DES ID。</span><span class="sxs-lookup"><span data-stu-id="3feb2-221">The DES ID to encrypt the restored disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="3feb2-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="3feb2-223">使用此開關觸發 [交叉區域] 還原至 [次要區域]。</span><span class="sxs-lookup"><span data-stu-id="3feb2-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3feb2-224">-VaultId</span></span>

<span data-ttu-id="3feb2-225">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="3feb2-225">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3feb2-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="3feb2-226">-VaultLocation</span></span>

<span data-ttu-id="3feb2-227">[恢復服務] 保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="3feb2-227">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3feb2-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="3feb2-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="3feb2-229">復原配置</span><span class="sxs-lookup"><span data-stu-id="3feb2-229">Recovery config</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3feb2-230">-確認</span><span class="sxs-lookup"><span data-stu-id="3feb2-230">-Confirm</span></span>

<span data-ttu-id="3feb2-231">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3feb2-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3feb2-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3feb2-232">-WhatIf</span></span>

<span data-ttu-id="3feb2-233">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3feb2-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="3feb2-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3feb2-234">CommonParameters</span></span>
<span data-ttu-id="3feb2-235">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3feb2-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3feb2-236">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3feb2-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3feb2-237">輸入</span><span class="sxs-lookup"><span data-stu-id="3feb2-237">INPUTS</span></span>

### <span data-ttu-id="3feb2-238">System.object</span><span class="sxs-lookup"><span data-stu-id="3feb2-238">System.String</span></span>

### <span data-ttu-id="3feb2-239">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="3feb2-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="3feb2-240">輸出</span><span class="sxs-lookup"><span data-stu-id="3feb2-240">OUTPUTS</span></span>

### <span data-ttu-id="3feb2-241">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="3feb2-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3feb2-242">筆記</span><span class="sxs-lookup"><span data-stu-id="3feb2-242">NOTES</span></span>

## <span data-ttu-id="3feb2-243">相關連結</span><span class="sxs-lookup"><span data-stu-id="3feb2-243">RELATED LINKS</span></span>

[<span data-ttu-id="3feb2-244">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3feb2-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3feb2-245">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3feb2-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3feb2-246">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3feb2-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
