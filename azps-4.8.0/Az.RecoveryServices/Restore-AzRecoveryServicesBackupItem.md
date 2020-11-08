---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970818"
---
# <span data-ttu-id="3245a-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3245a-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3245a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3245a-102">SYNOPSIS</span></span>

<span data-ttu-id="3245a-103">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="3245a-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="3245a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3245a-104">SYNTAX</span></span>

### <span data-ttu-id="3245a-105">AzureVMParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3245a-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3245a-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3245a-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3245a-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="3245a-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3245a-108">說明</span><span class="sxs-lookup"><span data-stu-id="3245a-108">DESCRIPTION</span></span>

<span data-ttu-id="3245a-109">**Restore-AzRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="3245a-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="3245a-110">這個 Cmdlet 會從 [恢復服務] 保存庫開始還原到客戶的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="3245a-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="3245a-111">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3245a-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="3245a-112">在還原作業完成之後，它會將受管理的磁片還原至目標資源群組，並將設定資訊還原至客戶儲存空間帳戶，您必須建立虛擬機器並啟動。</span><span class="sxs-lookup"><span data-stu-id="3245a-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="3245a-113">如需詳細資訊，請 refter 到其他可能的參數集與參數文字。</span><span class="sxs-lookup"><span data-stu-id="3245a-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="3245a-114">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="3245a-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="3245a-115">注意：若要成功執行此 Cmdlet，除了-VaultId 參數之外，也應該使用 VaultLocation 參數。</span><span class="sxs-lookup"><span data-stu-id="3245a-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="3245a-116">示例</span><span class="sxs-lookup"><span data-stu-id="3245a-116">EXAMPLES</span></span>

### <span data-ttu-id="3245a-117">範例1：將專案還原到復原點</span><span class="sxs-lookup"><span data-stu-id="3245a-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3245a-118">第一個命令會取得類型為「Add-azurevm」的備份容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3245a-119">第二個命令會從 $Container 取得名為 V2VM 的備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3245a-120">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3245a-121">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3245a-122">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="3245a-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="3245a-123">指定的日期範圍是過去7天。</span><span class="sxs-lookup"><span data-stu-id="3245a-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="3245a-124">第七個命令指定要從復原點還原哪些磁片，並將它儲存在 $restoreDiskLUNs 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="3245a-125">最後一個命令會將磁片還原為 [DestRG] 資源群組中的 [目標儲存空間] 帳戶 DestAccount。</span><span class="sxs-lookup"><span data-stu-id="3245a-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="3245a-126">範例2：還原 AzureFileShare 專案的多個檔案</span><span class="sxs-lookup"><span data-stu-id="3245a-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="3245a-127">第一個命令會取得類型為「Add-azurevm」的備份容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3245a-128">第二個命令會取得名為 fileshareitem 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3245a-129">第三個命令會針對特定備份專案取得復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="3245a-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="3245a-130">第四個命令 spceifies 要還原哪些檔案，並將其儲存在 $files 變數中。</span><span class="sxs-lookup"><span data-stu-id="3245a-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="3245a-131">最後一個命令會將指定的檔案還原至其原始位置。</span><span class="sxs-lookup"><span data-stu-id="3245a-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="3245a-132">範例3</span><span class="sxs-lookup"><span data-stu-id="3245a-132">Example 3</span></span>

<span data-ttu-id="3245a-133">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="3245a-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="3245a-134"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="3245a-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="3245a-135">參數</span><span class="sxs-lookup"><span data-stu-id="3245a-135">PARAMETERS</span></span>

### <span data-ttu-id="3245a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3245a-136">-DefaultProfile</span></span>

<span data-ttu-id="3245a-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3245a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3245a-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="3245a-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="3245a-139">用於多個檔案從檔案共用中還原。</span><span class="sxs-lookup"><span data-stu-id="3245a-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="3245a-140">檔案共用中要還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3245a-140">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="3245a-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3245a-141">-RecoveryPoint</span></span>

<span data-ttu-id="3245a-142">指定要還原備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="3245a-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="3245a-143">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 **AzRecoveryServicesBackupRecoveryPoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3245a-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="3245a-144">-ResolveConflict</span></span>

<span data-ttu-id="3245a-145">如果還原的專案也存在於目的地中，請使用此選項來指出是否要覆寫。</span><span class="sxs-lookup"><span data-stu-id="3245a-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="3245a-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3245a-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3245a-147">原有</span><span class="sxs-lookup"><span data-stu-id="3245a-147">Overwrite</span></span>
- <span data-ttu-id="3245a-148">跳</span><span class="sxs-lookup"><span data-stu-id="3245a-148">Skip</span></span>

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

### <span data-ttu-id="3245a-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="3245a-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="3245a-150">使用此開關指定要還原為非託管磁片</span><span class="sxs-lookup"><span data-stu-id="3245a-150">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="3245a-151">-RestoreDiskList</span></span>
<span data-ttu-id="3245a-152">指定要復原備份的 VM 的磁片</span><span class="sxs-lookup"><span data-stu-id="3245a-152">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-153">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="3245a-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="3245a-154">使用此開關只還原已備份 VM 的 OS 磁片</span><span class="sxs-lookup"><span data-stu-id="3245a-154">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="3245a-155">-SourceFilePath</span></span>

<span data-ttu-id="3245a-156">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="3245a-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="3245a-157">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3245a-157">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="3245a-158">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="3245a-158">-SourceFileType</span></span>

<span data-ttu-id="3245a-159">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="3245a-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="3245a-160">要在檔案共用中還原的專案類型。</span><span class="sxs-lookup"><span data-stu-id="3245a-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="3245a-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3245a-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3245a-162">檔案</span><span class="sxs-lookup"><span data-stu-id="3245a-162">File</span></span>
- <span data-ttu-id="3245a-163">空目錄</span><span class="sxs-lookup"><span data-stu-id="3245a-163">Directory</span></span>

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

### <span data-ttu-id="3245a-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3245a-164">-StorageAccountName</span></span>

<span data-ttu-id="3245a-165">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3245a-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="3245a-166">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="3245a-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3245a-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="3245a-168">指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3245a-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="3245a-169">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="3245a-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-170">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="3245a-170">-TargetFileShareName</span></span>

<span data-ttu-id="3245a-171">檔案共用要還原到的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="3245a-171">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="3245a-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="3245a-172">-TargetFolder</span></span>

<span data-ttu-id="3245a-173">要在 TargetFileShareName 中還原檔案共用的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3245a-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="3245a-174">如果備份的內容要還原到根資料夾，請將目的檔案夾的值指定為空字串。</span><span class="sxs-lookup"><span data-stu-id="3245a-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="3245a-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3245a-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="3245a-176">要還原受管理磁片的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3245a-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="3245a-177">適用于使用受管理磁片的 VM 備份</span><span class="sxs-lookup"><span data-stu-id="3245a-177">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3245a-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="3245a-179">檔案共用要還原到的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="3245a-179">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="3245a-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3245a-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="3245a-181">如果要將復原點的磁片還原到其原始儲存空間帳戶，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="3245a-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3245a-182">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3245a-182">-VaultId</span></span>

<span data-ttu-id="3245a-183">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="3245a-183">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3245a-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="3245a-184">-VaultLocation</span></span>

<span data-ttu-id="3245a-185">[恢復服務] 保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="3245a-185">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3245a-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="3245a-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="3245a-187">復原配置</span><span class="sxs-lookup"><span data-stu-id="3245a-187">Recovery config</span></span>

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

### <span data-ttu-id="3245a-188">-確認</span><span class="sxs-lookup"><span data-stu-id="3245a-188">-Confirm</span></span>

<span data-ttu-id="3245a-189">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3245a-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3245a-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3245a-190">-WhatIf</span></span>

<span data-ttu-id="3245a-191">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3245a-191">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="3245a-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3245a-192">CommonParameters</span></span>
<span data-ttu-id="3245a-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3245a-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3245a-194">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3245a-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3245a-195">輸入</span><span class="sxs-lookup"><span data-stu-id="3245a-195">INPUTS</span></span>

### <span data-ttu-id="3245a-196">System.object</span><span class="sxs-lookup"><span data-stu-id="3245a-196">System.String</span></span>

### <span data-ttu-id="3245a-197">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="3245a-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="3245a-198">輸出</span><span class="sxs-lookup"><span data-stu-id="3245a-198">OUTPUTS</span></span>

### <span data-ttu-id="3245a-199">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="3245a-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3245a-200">筆記</span><span class="sxs-lookup"><span data-stu-id="3245a-200">NOTES</span></span>

## <span data-ttu-id="3245a-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="3245a-201">RELATED LINKS</span></span>

[<span data-ttu-id="3245a-202">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3245a-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3245a-203">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3245a-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3245a-204">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3245a-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
