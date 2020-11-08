---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138658"
---
# <span data-ttu-id="b1b7d-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b1b7d-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b1b7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1b7d-102">SYNOPSIS</span></span>

<span data-ttu-id="b1b7d-103">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="b1b7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1b7d-104">SYNTAX</span></span>

### <span data-ttu-id="b1b7d-105">AzureVMParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1b7d-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b7d-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b7d-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b7d-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="b1b7d-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b7d-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b7d-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b7d-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b7d-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b7d-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b7d-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b7d-111">說明</span><span class="sxs-lookup"><span data-stu-id="b1b7d-111">DESCRIPTION</span></span>

<span data-ttu-id="b1b7d-112">**Restore-AzRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="b1b7d-113">這個 Cmdlet 會從 [恢復服務] 保存庫開始還原到客戶的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="b1b7d-114">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="b1b7d-115">在還原作業完成之後，它會將受管理的磁片還原至目標資源群組，並將設定資訊還原至客戶儲存空間帳戶，您必須建立虛擬機器並啟動。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="b1b7d-116">如需詳細資訊，請 refter 到其他可能的參數集與參數文字。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="b1b7d-117">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="b1b7d-118">注意：若要成功執行此 Cmdlet，除了-VaultId 參數之外，也應該使用 VaultLocation 參數。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="b1b7d-119">示例</span><span class="sxs-lookup"><span data-stu-id="b1b7d-119">EXAMPLES</span></span>

### <span data-ttu-id="b1b7d-120">範例1：將專案還原到復原點</span><span class="sxs-lookup"><span data-stu-id="b1b7d-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b1b7d-121">第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="b1b7d-122">第二個命令會取得備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b1b7d-123">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="b1b7d-124">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="b1b7d-125">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="b1b7d-126">第六個命令指定要從復原點還原哪些磁片，並將它儲存在 $restoreDiskLUNs 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="b1b7d-127">最後一個命令會將磁片還原為 [DestRG] 資源群組中的 [目標儲存空間] 帳戶 DestAccount。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="b1b7d-128">範例2：還原 AzureFileShare 專案的多個檔案</span><span class="sxs-lookup"><span data-stu-id="b1b7d-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b1b7d-129">第一個命令會取得類型為「Add-azurevm」的備份容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b1b7d-130">第二個命令會取得名為 fileshareitem 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b1b7d-131">第三個命令會針對特定備份專案取得復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="b1b7d-132">第四個命令 spceifies 要還原哪些檔案，並將其儲存在 $files 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="b1b7d-133">最後一個命令會將指定的檔案還原至其原始位置。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="b1b7d-134">範例3</span><span class="sxs-lookup"><span data-stu-id="b1b7d-134">Example 3</span></span>

<span data-ttu-id="b1b7d-135">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="b1b7d-136"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="b1b7d-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="b1b7d-137">範例4：將受管理的 VM 還原成受管理的磁片</span><span class="sxs-lookup"><span data-stu-id="b1b7d-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b1b7d-138">第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="b1b7d-139">第二個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b1b7d-140">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="b1b7d-141">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="b1b7d-142">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="b1b7d-143">第六個命令會將磁片還原為具有指定目標資源群組的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="b1b7d-144">範例5：將受管理的 VM 還原為非託管磁片</span><span class="sxs-lookup"><span data-stu-id="b1b7d-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b1b7d-145">第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="b1b7d-146">第二個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b1b7d-147">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="b1b7d-148">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="b1b7d-149">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="b1b7d-150">第六個命令會將磁片還原為非託管磁片。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="b1b7d-151">範例6：使用原始儲存空間帳戶將未受管理的 VM 還原為非託管磁片。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b1b7d-152">第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="b1b7d-153">第二個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b1b7d-154">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="b1b7d-155">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="b1b7d-156">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="b1b7d-157">第六個命令使用 VM 的原始儲存空間帳戶，將磁片還原為非託管磁片。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="b1b7d-158">參數</span><span class="sxs-lookup"><span data-stu-id="b1b7d-158">PARAMETERS</span></span>

### <span data-ttu-id="b1b7d-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b7d-159">-DefaultProfile</span></span>

<span data-ttu-id="b1b7d-160">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b7d-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="b1b7d-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="b1b7d-162">用於多個檔案從檔案共用中還原。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="b1b7d-163">檔案共用中要還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="b1b7d-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b1b7d-164">-RecoveryPoint</span></span>

<span data-ttu-id="b1b7d-165">指定要還原備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="b1b7d-166">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 **AzRecoveryServicesBackupRecoveryPoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="b1b7d-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="b1b7d-167">-ResolveConflict</span></span>

<span data-ttu-id="b1b7d-168">如果還原的專案也存在於目的地中，請使用此選項來指出是否要覆寫。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="b1b7d-169">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b1b7d-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1b7d-170">原有</span><span class="sxs-lookup"><span data-stu-id="b1b7d-170">Overwrite</span></span>
- <span data-ttu-id="b1b7d-171">跳</span><span class="sxs-lookup"><span data-stu-id="b1b7d-171">Skip</span></span>

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

### <span data-ttu-id="b1b7d-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="b1b7d-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="b1b7d-173">使用此開關指定要還原為非託管磁片</span><span class="sxs-lookup"><span data-stu-id="b1b7d-173">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="b1b7d-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="b1b7d-174">-RestoreDiskList</span></span>
<span data-ttu-id="b1b7d-175">指定要復原備份的 VM 的磁片</span><span class="sxs-lookup"><span data-stu-id="b1b7d-175">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="b1b7d-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="b1b7d-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="b1b7d-177">使用此開關只還原已備份 VM 的 OS 磁片</span><span class="sxs-lookup"><span data-stu-id="b1b7d-177">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="b1b7d-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="b1b7d-178">-SourceFilePath</span></span>

<span data-ttu-id="b1b7d-179">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="b1b7d-180">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="b1b7d-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="b1b7d-181">-SourceFileType</span></span>

<span data-ttu-id="b1b7d-182">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="b1b7d-183">要在檔案共用中還原的專案類型。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="b1b7d-184">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b1b7d-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1b7d-185">檔案</span><span class="sxs-lookup"><span data-stu-id="b1b7d-185">File</span></span>
- <span data-ttu-id="b1b7d-186">空目錄</span><span class="sxs-lookup"><span data-stu-id="b1b7d-186">Directory</span></span>

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

### <span data-ttu-id="b1b7d-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1b7d-187">-StorageAccountName</span></span>

<span data-ttu-id="b1b7d-188">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="b1b7d-189">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="b1b7d-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b7d-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="b1b7d-191">指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="b1b7d-192">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="b1b7d-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="b1b7d-193">-TargetFileShareName</span></span>

<span data-ttu-id="b1b7d-194">檔案共用要還原到的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="b1b7d-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="b1b7d-195">-TargetFolder</span></span>

<span data-ttu-id="b1b7d-196">要在 TargetFileShareName 中還原檔案共用的資料夾。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="b1b7d-197">如果備份的內容要還原到根資料夾，請將目的檔案夾的值指定為空字串。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="b1b7d-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b7d-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="b1b7d-199">要還原受管理磁片的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="b1b7d-200">適用于使用受管理磁片的 VM 備份</span><span class="sxs-lookup"><span data-stu-id="b1b7d-200">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="b1b7d-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1b7d-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="b1b7d-202">檔案共用要還原到的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="b1b7d-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1b7d-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="b1b7d-204">如果要將復原點的磁片還原到其原始儲存空間帳戶，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="b1b7d-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b1b7d-205">-VaultId</span></span>

<span data-ttu-id="b1b7d-206">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b1b7d-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="b1b7d-207">-VaultLocation</span></span>

<span data-ttu-id="b1b7d-208">[恢復服務] 保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b1b7d-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="b1b7d-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="b1b7d-210">復原配置</span><span class="sxs-lookup"><span data-stu-id="b1b7d-210">Recovery config</span></span>

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

### <span data-ttu-id="b1b7d-211">-確認</span><span class="sxs-lookup"><span data-stu-id="b1b7d-211">-Confirm</span></span>

<span data-ttu-id="b1b7d-212">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b7d-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b7d-213">-WhatIf</span></span>

<span data-ttu-id="b1b7d-214">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="b1b7d-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b7d-215">CommonParameters</span></span>
<span data-ttu-id="b1b7d-216">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b7d-217">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1b7d-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b7d-218">輸入</span><span class="sxs-lookup"><span data-stu-id="b1b7d-218">INPUTS</span></span>

### <span data-ttu-id="b1b7d-219">System.object</span><span class="sxs-lookup"><span data-stu-id="b1b7d-219">System.String</span></span>

### <span data-ttu-id="b1b7d-220">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="b1b7d-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b1b7d-221">輸出</span><span class="sxs-lookup"><span data-stu-id="b1b7d-221">OUTPUTS</span></span>

### <span data-ttu-id="b1b7d-222">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="b1b7d-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b1b7d-223">筆記</span><span class="sxs-lookup"><span data-stu-id="b1b7d-223">NOTES</span></span>

## <span data-ttu-id="b1b7d-224">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1b7d-224">RELATED LINKS</span></span>

[<span data-ttu-id="b1b7d-225">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b1b7d-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b1b7d-226">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b1b7d-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b1b7d-227">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b1b7d-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
