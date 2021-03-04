---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3d3cbb196a287e24837c0e7b0e61b16eaa06ce95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913769"
---
# <span data-ttu-id="5d009-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5d009-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5d009-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d009-102">SYNOPSIS</span></span>

<span data-ttu-id="5d009-103">將備份專案的資料與群組原則還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="5d009-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="5d009-104">所需的參數會隨備份專案類型而不同。</span><span class="sxs-lookup"><span data-stu-id="5d009-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="5d009-105">相同的命令可用來還原 Azure 虛擬機器、在 Azure 虛擬機器中執行的資料庫，以及 Azure 檔案共用。</span><span class="sxs-lookup"><span data-stu-id="5d009-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="5d009-106">語法</span><span class="sxs-lookup"><span data-stu-id="5d009-106">SYNTAX</span></span>

### <span data-ttu-id="5d009-107">AzureAZPARameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5d009-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d009-108">AzureEVManagedAzParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d009-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d009-109">AzureAZREstoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="5d009-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d009-110">AzureAZMUnManagedAzAzParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d009-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d009-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d009-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d009-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d009-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d009-113">描述</span><span class="sxs-lookup"><span data-stu-id="5d009-113">DESCRIPTION</span></span>

<span data-ttu-id="5d009-114">**Restore-AzRecoveryServicesBackupItem** Cmdlet 會還原 Azure 備份專案的資料和組式到指定的修復點。</span><span class="sxs-lookup"><span data-stu-id="5d009-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="5d009-115">**Azure VM 備份**</span><span class="sxs-lookup"><span data-stu-id="5d009-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="5d009-116">您可以使用此命令備份 Azure 虛擬機器，並還原 (和未受管理) 磁片。</span><span class="sxs-lookup"><span data-stu-id="5d009-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="5d009-117">還原作業無法還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5d009-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="5d009-118">如果這是受管理的磁片 VM，應指定目標資源群組，將還原的磁片保留的位置。</span><span class="sxs-lookup"><span data-stu-id="5d009-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="5d009-119">指定目標資源群組時，如果快照存在於備份策略中指定的資源群組中，還原作業就會立即進行，而且會從本地快照建立磁片，並保留在目標資源群組中。</span><span class="sxs-lookup"><span data-stu-id="5d009-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="5d009-120">也有選項可將其還原為未受管理的磁片，但這會運用 Azure 修復服務儲存庫中的資料，因此速度將會變慢。</span><span class="sxs-lookup"><span data-stu-id="5d009-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="5d009-121">可用於從復原磁碟區建立 VM 的 VM 和部署範本的組配置，將會下載到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d009-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="5d009-122">如果這是未受管理的磁片 VM，則快照會存在於磁片的原始儲存帳戶和/或修復服務保存庫中。</span><span class="sxs-lookup"><span data-stu-id="5d009-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="5d009-123">如果使用者提供使用原始儲存空間帳戶進行還原的選項，就可以提供立即還原功能。</span><span class="sxs-lookup"><span data-stu-id="5d009-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="5d009-124">否則，會從 Azure 修復服務保存庫抓取資料，並且會以指定的儲存帳戶建立磁片，同時建立 VM 和部署範本的群組原則。</span><span class="sxs-lookup"><span data-stu-id="5d009-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d009-125">根據預設，Azure VM 備份會備份所有磁片。</span><span class="sxs-lookup"><span data-stu-id="5d009-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="5d009-126">您可以在啟用備份期間，使用 exclusionList 或 InclusionList 參數選擇性地備份相關的磁片。</span><span class="sxs-lookup"><span data-stu-id="5d009-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="5d009-127">選擇性復原磁碟的選項只有在有選擇性備份時才能使用。</span><span class="sxs-lookup"><span data-stu-id="5d009-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="5d009-128">如需詳細資訊，請參閱不同的可能參數集和參數文字。</span><span class="sxs-lookup"><span data-stu-id="5d009-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="5d009-129">如果使用 -VaultId 參數，則也應該使用 -VaultLocation 參數。</span><span class="sxs-lookup"><span data-stu-id="5d009-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="5d009-130">**針對 Azure 檔案共用備份**</span><span class="sxs-lookup"><span data-stu-id="5d009-130">**For Azure File share backup**</span></span>

<span data-ttu-id="5d009-131">您可以還原整個檔案共用，或共用上的特定/多個檔案/資料夾。</span><span class="sxs-lookup"><span data-stu-id="5d009-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="5d009-132">您可以還原到原始位置或替代位置。</span><span class="sxs-lookup"><span data-stu-id="5d009-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="5d009-133">**Azure 工作負載**</span><span class="sxs-lookup"><span data-stu-id="5d009-133">**For Azure Workloads**</span></span>

<span data-ttu-id="5d009-134">您可以在 Azure 虛擬機器中還原 SQL DB</span><span class="sxs-lookup"><span data-stu-id="5d009-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="5d009-135">例子</span><span class="sxs-lookup"><span data-stu-id="5d009-135">EXAMPLES</span></span>

### <span data-ttu-id="5d009-136">範例 1：從給定修復點還原備份 Managed 磁片 Azure VM 的磁片</span><span class="sxs-lookup"><span data-stu-id="5d009-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="5d009-137">第一個命令會獲得修復服務保存庫，並儲存在$vault變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5d009-138">第二個命令會獲得名稱為 "V2 VM" 的 Azure VM 類型的備份專案，並儲存在$BackupItem變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5d009-139">第三個命令會從七天前開始獲得日期，然後將它儲存在$StartDate變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5d009-140">第四個命令會獲得目前的日期，然後將它儲存在$EndDate變數中。</span><span class="sxs-lookup"><span data-stu-id="5d009-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5d009-141">第五個命令會針對特定備份專案，以 $StartDate和$EndDate。</span><span class="sxs-lookup"><span data-stu-id="5d009-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5d009-142">最後一個命令會還原目標資源群組 Target_RG 的所有磁片，然後在 DestRG 資源群組的儲存帳戶 DestAccount中提供 VM 群組原則資訊和部署範本。</span><span class="sxs-lookup"><span data-stu-id="5d009-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="5d009-143">範例 2：從指定的復原點還原備份受管理的磁片 Azure VM 的指定磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="5d009-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="5d009-144">第一個命令會獲得修復服務保存庫，並儲存在$vault變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5d009-145">第二個命令會獲得名稱為 "V2 VM" 的 Azure VM 類型的備份專案，並儲存在$BackupItem變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5d009-146">第三個命令會從七天前開始獲得日期，然後將它儲存在$StartDate變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5d009-147">第四個命令會獲得目前的日期，然後將它儲存在$EndDate變數中。</span><span class="sxs-lookup"><span data-stu-id="5d009-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5d009-148">第五個命令會針對特定備份專案，以 $StartDate和$EndDate。</span><span class="sxs-lookup"><span data-stu-id="5d009-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5d009-149">第六個命令會儲存要還原的磁片清單，以還原至 Restore。。</span><span class="sxs-lookup"><span data-stu-id="5d009-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="5d009-150">最後一個命令會還原指定磁片的指定磁片，即指定的 LUN 到目標資源群組 Target_RG，然後在 DestRG 資源群組中的儲存帳戶 DestAccount中提供 VM 群組原則資訊和部署範本。</span><span class="sxs-lookup"><span data-stu-id="5d009-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="5d009-151">範例 3：將受管理 VM 的磁片還原為未受管理的磁片</span><span class="sxs-lookup"><span data-stu-id="5d009-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

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

<span data-ttu-id="5d009-152">第一個命令會獲得 RecoveryServices 保存庫，並儲存在$vault變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5d009-153">第二個命令會獲得備份專案，然後將它儲存在$BackupItem變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5d009-154">第三個命令會從七天前開始獲得日期，然後將它儲存在$StartDate變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5d009-155">第四個命令會獲得目前的日期，然後將它儲存在$EndDate變數中。</span><span class="sxs-lookup"><span data-stu-id="5d009-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5d009-156">第五個命令會針對特定備份專案，以 $StartDate和$EndDate。</span><span class="sxs-lookup"><span data-stu-id="5d009-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5d009-157">第六個命令將磁片還原為未管理磁片。</span><span class="sxs-lookup"><span data-stu-id="5d009-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="5d009-158">範例 4：使用原始儲存帳戶將未管理之 VM 還原為未管理磁片</span><span class="sxs-lookup"><span data-stu-id="5d009-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

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

<span data-ttu-id="5d009-159">第一個命令會獲得 RecoveryServices 保存庫，並儲存在$vault變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5d009-160">第二個命令會獲得備份專案，然後將它儲存在$BackupItem變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5d009-161">第三個命令會從七天前開始獲得日期，然後將它儲存在$StartDate變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5d009-162">第四個命令會獲得目前的日期，然後將它儲存在$EndDate變數中。</span><span class="sxs-lookup"><span data-stu-id="5d009-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5d009-163">第五個命令會針對特定備份專案，以 $StartDate和$EndDate。</span><span class="sxs-lookup"><span data-stu-id="5d009-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5d009-164">第六個命令將磁片還原為未管理磁片至其原始儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="5d009-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="5d009-165">範例 5：還原 AzureFileShare 專案的多個檔案</span><span class="sxs-lookup"><span data-stu-id="5d009-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="5d009-166">第一個命令會獲得修復服務保存庫，並儲存在$vault變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5d009-167">第二個命令會獲得名為 fileshareitem 的備份專案，然後將它儲存在$BackupItem變數中。</span><span class="sxs-lookup"><span data-stu-id="5d009-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5d009-168">第三個命令會獲得特定備份專案的復原點清單。</span><span class="sxs-lookup"><span data-stu-id="5d009-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="5d009-169">第四個命令指定要還原哪些檔案，並儲存在$files變數。</span><span class="sxs-lookup"><span data-stu-id="5d009-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="5d009-170">最後一個命令會還原指定的檔案至其原始位置。</span><span class="sxs-lookup"><span data-stu-id="5d009-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="5d009-171">範例 6：將 Azure VM 內的 SQL DB 還原至另一個目標 VM，以建立不同的完整復原點</span><span class="sxs-lookup"><span data-stu-id="5d009-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

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

### <span data-ttu-id="5d009-172">範例 7：將 Azure VM 中的 SQL DB 還原至記錄復原點的另一個目標 VM</span><span class="sxs-lookup"><span data-stu-id="5d009-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

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

## <span data-ttu-id="5d009-173">參數</span><span class="sxs-lookup"><span data-stu-id="5d009-173">PARAMETERS</span></span>

### <span data-ttu-id="5d009-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d009-174">-DefaultProfile</span></span>

<span data-ttu-id="5d009-175">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d009-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d009-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5d009-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="5d009-177">用於從檔案共用還原多個檔案。</span><span class="sxs-lookup"><span data-stu-id="5d009-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="5d009-178">檔案共用中要還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="5d009-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="5d009-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5d009-179">-RecoveryPoint</span></span>

<span data-ttu-id="5d009-180">指定要還原備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="5d009-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="5d009-181">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 **Get-AzRecoveryServicesBackupRecoveryPoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d009-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="5d009-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="5d009-182">-ResolveConflict</span></span>

<span data-ttu-id="5d009-183">如果還原的專案也存在於目的地中，請使用這個來表示是否要覆寫。</span><span class="sxs-lookup"><span data-stu-id="5d009-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="5d009-184">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5d009-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d009-185">覆蓋</span><span class="sxs-lookup"><span data-stu-id="5d009-185">Overwrite</span></span>
- <span data-ttu-id="5d009-186">跳</span><span class="sxs-lookup"><span data-stu-id="5d009-186">Skip</span></span>

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

### <span data-ttu-id="5d009-187">-RestoreAsUnmanaged至</span><span class="sxs-lookup"><span data-stu-id="5d009-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="5d009-188">使用此參數指定還原為未管理磁片</span><span class="sxs-lookup"><span data-stu-id="5d009-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="5d009-189">-RestoreList</span><span class="sxs-lookup"><span data-stu-id="5d009-189">-RestoreDiskList</span></span>
<span data-ttu-id="5d009-190">指定要復原備份之 VM 的磁片</span><span class="sxs-lookup"><span data-stu-id="5d009-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="5d009-191">-RestoreOnlyOSCio</span><span class="sxs-lookup"><span data-stu-id="5d009-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="5d009-192">使用此切換只還原備份之 VM 的作業系統磁片</span><span class="sxs-lookup"><span data-stu-id="5d009-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="5d009-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5d009-193">-SourceFilePath</span></span>

<span data-ttu-id="5d009-194">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="5d009-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5d009-195">檔案共用中要還原的專案路徑。</span><span class="sxs-lookup"><span data-stu-id="5d009-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="5d009-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="5d009-196">-SourceFileType</span></span>

<span data-ttu-id="5d009-197">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="5d009-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5d009-198">檔案共用中要還原的專案類型。</span><span class="sxs-lookup"><span data-stu-id="5d009-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="5d009-199">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5d009-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5d009-200">檔</span><span class="sxs-lookup"><span data-stu-id="5d009-200">File</span></span>
- <span data-ttu-id="5d009-201">目錄</span><span class="sxs-lookup"><span data-stu-id="5d009-201">Directory</span></span>

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

### <span data-ttu-id="5d009-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5d009-202">-StorageAccountName</span></span>

<span data-ttu-id="5d009-203">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d009-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="5d009-204">做為還原程式一部分，此 Cmdlet 會在此儲存空間帳戶中儲存磁片和組程資訊。</span><span class="sxs-lookup"><span data-stu-id="5d009-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="5d009-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d009-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="5d009-206">指定訂閱中包含目標儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5d009-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="5d009-207">做為還原程式一部分，此 Cmdlet 會在此儲存空間帳戶中儲存磁片和組程資訊。</span><span class="sxs-lookup"><span data-stu-id="5d009-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="5d009-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="5d009-208">-TargetFileShareName</span></span>

<span data-ttu-id="5d009-209">檔案共用必須還原至的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="5d009-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5d009-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="5d009-210">-TargetFolder</span></span>

<span data-ttu-id="5d009-211">檔案共用必須還原到 TargetFileShareName 內的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5d009-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="5d009-212">如果要將備份的內容還原到根資料夾，請以空白字串形式提供目的檔案夾值。</span><span class="sxs-lookup"><span data-stu-id="5d009-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="5d009-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d009-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="5d009-214">受管理磁片還原至的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5d009-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="5d009-215">適用于使用受管理的磁片備份的 VM</span><span class="sxs-lookup"><span data-stu-id="5d009-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="5d009-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5d009-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="5d009-217">檔案共用必須還原至的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d009-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5d009-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d009-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="5d009-219">若要將修復點的磁片還原到其原始的儲存空間帳戶，請使用此開關。</span><span class="sxs-lookup"><span data-stu-id="5d009-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="5d009-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="5d009-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="5d009-221">DES 識別碼可加密還原的磁片。</span><span class="sxs-lookup"><span data-stu-id="5d009-221">The DES ID to encrypt the restored disks.</span></span>

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

### <span data-ttu-id="5d009-222">-RestoreTo一個Region</span><span class="sxs-lookup"><span data-stu-id="5d009-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="5d009-223">使用此切換來觸發跨區域還原至次要區域。</span><span class="sxs-lookup"><span data-stu-id="5d009-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

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

### <span data-ttu-id="5d009-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5d009-224">-VaultId</span></span>

<span data-ttu-id="5d009-225">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d009-225">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5d009-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="5d009-226">-VaultLocation</span></span>

<span data-ttu-id="5d009-227">復原服務庫的位置。</span><span class="sxs-lookup"><span data-stu-id="5d009-227">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5d009-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="5d009-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="5d009-229">修復設定檔</span><span class="sxs-lookup"><span data-stu-id="5d009-229">Recovery config</span></span>

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

### <span data-ttu-id="5d009-230">-確認</span><span class="sxs-lookup"><span data-stu-id="5d009-230">-Confirm</span></span>

<span data-ttu-id="5d009-231">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5d009-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d009-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d009-232">-WhatIf</span></span>

<span data-ttu-id="5d009-233">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d009-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="5d009-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d009-234">CommonParameters</span></span>
<span data-ttu-id="5d009-235">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d009-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d009-236">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d009-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d009-237">輸入</span><span class="sxs-lookup"><span data-stu-id="5d009-237">INPUTS</span></span>

### <span data-ttu-id="5d009-238">System.String</span><span class="sxs-lookup"><span data-stu-id="5d009-238">System.String</span></span>

### <span data-ttu-id="5d009-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5d009-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="5d009-240">輸出</span><span class="sxs-lookup"><span data-stu-id="5d009-240">OUTPUTS</span></span>

### <span data-ttu-id="5d009-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="5d009-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5d009-242">筆記</span><span class="sxs-lookup"><span data-stu-id="5d009-242">NOTES</span></span>

## <span data-ttu-id="5d009-243">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d009-243">RELATED LINKS</span></span>

[<span data-ttu-id="5d009-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5d009-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="5d009-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5d009-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="5d009-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5d009-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
