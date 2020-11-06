---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: eb54d22f74216dc883726d34df204ce80c711a22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621067"
---
# <span data-ttu-id="b1e40-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b1e40-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b1e40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1e40-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e40-103">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="b1e40-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="b1e40-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1e40-104">SYNTAX</span></span>

### <span data-ttu-id="b1e40-105">AzureVMParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1e40-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e40-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1e40-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1e40-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1e40-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1e40-108">說明</span><span class="sxs-lookup"><span data-stu-id="b1e40-108">DESCRIPTION</span></span>
<span data-ttu-id="b1e40-109">**Restore-AzRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="b1e40-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="b1e40-110">這個 Cmdlet 會從 [恢復服務] 保存庫開始還原到客戶的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b1e40-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="b1e40-111">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b1e40-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="b1e40-112">它會復原磁碟資料和配置資訊。</span><span class="sxs-lookup"><span data-stu-id="b1e40-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="b1e40-113">完成還原作業之後，您必須建立並啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b1e40-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="b1e40-114">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1e40-114">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b1e40-115">示例</span><span class="sxs-lookup"><span data-stu-id="b1e40-115">EXAMPLES</span></span>

### <span data-ttu-id="b1e40-116">範例1：將專案還原到復原點</span><span class="sxs-lookup"><span data-stu-id="b1e40-116">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b1e40-117">第一個命令會取得類型為「Add-azurevm」的備份容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1e40-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b1e40-118">第二個命令會從 $Container 取得名為 V2VM 的備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1e40-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b1e40-119">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1e40-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="b1e40-120">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1e40-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="b1e40-121">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="b1e40-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="b1e40-122">指定的日期範圍是過去7天。</span><span class="sxs-lookup"><span data-stu-id="b1e40-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="b1e40-123">最後一個命令會將磁片還原為 [DestRG] 資源群組中的 [目標儲存空間] 帳戶 DestAccount。</span><span class="sxs-lookup"><span data-stu-id="b1e40-123">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="b1e40-124">參數</span><span class="sxs-lookup"><span data-stu-id="b1e40-124">PARAMETERS</span></span>

### <span data-ttu-id="b1e40-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e40-125">-DefaultProfile</span></span>
<span data-ttu-id="b1e40-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1e40-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1e40-127">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b1e40-127">-RecoveryPoint</span></span>
<span data-ttu-id="b1e40-128">指定要還原虛擬機器的復原點。</span><span class="sxs-lookup"><span data-stu-id="b1e40-128">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="b1e40-129">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 Get-AzRecoveryServicesBackupRecoveryPoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1e40-129">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="b1e40-130">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="b1e40-130">-ResolveConflict</span></span>
<span data-ttu-id="b1e40-131">如果還原的專案也存在於目的地中，請使用此選項來指出是否要覆寫。</span><span class="sxs-lookup"><span data-stu-id="b1e40-131">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

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

### <span data-ttu-id="b1e40-132">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="b1e40-132">-SourceFilePath</span></span>
<span data-ttu-id="b1e40-133">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="b1e40-133">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="b1e40-134">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b1e40-134">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="b1e40-135">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="b1e40-135">-SourceFileType</span></span>
<span data-ttu-id="b1e40-136">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="b1e40-136">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="b1e40-137">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b1e40-137">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="b1e40-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1e40-138">-StorageAccountName</span></span>
<span data-ttu-id="b1e40-139">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1e40-139">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="b1e40-140">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="b1e40-140">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="b1e40-141">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e40-141">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="b1e40-142">指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1e40-142">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="b1e40-143">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="b1e40-143">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="b1e40-144">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="b1e40-144">-TargetFileShareName</span></span>
<span data-ttu-id="b1e40-145">檔案共用要還原到的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b1e40-145">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="b1e40-146">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="b1e40-146">-TargetFolder</span></span>
<span data-ttu-id="b1e40-147">要在 targetFileShareName 中將檔案共用還原到哪個資料夾。請將該變數留白，以便在 [根資料夾] 下還原。</span><span class="sxs-lookup"><span data-stu-id="b1e40-147">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="b1e40-148">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e40-148">-TargetResourceGroupName</span></span>
<span data-ttu-id="b1e40-149">要還原受管理磁片的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b1e40-149">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="b1e40-150">適用于使用受管理磁片的 VM 備份</span><span class="sxs-lookup"><span data-stu-id="b1e40-150">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="b1e40-151">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1e40-151">-TargetStorageAccountName</span></span>
<span data-ttu-id="b1e40-152">檔案共用要還原到的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b1e40-152">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="b1e40-153">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1e40-153">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="b1e40-154">如果要將復原點的磁片還原到其原始儲存空間帳戶，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="b1e40-154">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="b1e40-155">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b1e40-155">-VaultId</span></span>
<span data-ttu-id="b1e40-156">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="b1e40-156">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b1e40-157">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="b1e40-157">-VaultLocation</span></span>
<span data-ttu-id="b1e40-158">[恢復服務] 保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="b1e40-158">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b1e40-159">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="b1e40-159">-WLRecoveryConfig</span></span>
<span data-ttu-id="b1e40-160">復原配置</span><span class="sxs-lookup"><span data-stu-id="b1e40-160">Recovery config</span></span>

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

### <span data-ttu-id="b1e40-161">-確認</span><span class="sxs-lookup"><span data-stu-id="b1e40-161">-Confirm</span></span>
<span data-ttu-id="b1e40-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1e40-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e40-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e40-163">-WhatIf</span></span>
<span data-ttu-id="b1e40-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1e40-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1e40-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1e40-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e40-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e40-166">CommonParameters</span></span>
<span data-ttu-id="b1e40-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1e40-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e40-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1e40-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e40-169">輸入</span><span class="sxs-lookup"><span data-stu-id="b1e40-169">INPUTS</span></span>

### <span data-ttu-id="b1e40-170">System.object</span><span class="sxs-lookup"><span data-stu-id="b1e40-170">System.String</span></span>

### <span data-ttu-id="b1e40-171">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="b1e40-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b1e40-172">輸出</span><span class="sxs-lookup"><span data-stu-id="b1e40-172">OUTPUTS</span></span>

### <span data-ttu-id="b1e40-173">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="b1e40-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b1e40-174">筆記</span><span class="sxs-lookup"><span data-stu-id="b1e40-174">NOTES</span></span>

## <span data-ttu-id="b1e40-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1e40-175">RELATED LINKS</span></span>

[<span data-ttu-id="b1e40-176">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b1e40-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b1e40-177">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b1e40-177">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b1e40-178">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b1e40-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)


