---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791844"
---
# <span data-ttu-id="a9a58-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a9a58-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a9a58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9a58-102">SYNOPSIS</span></span>

<span data-ttu-id="a9a58-103">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="a9a58-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="a9a58-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9a58-104">SYNTAX</span></span>

### <span data-ttu-id="a9a58-105">AzureVMParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a9a58-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a58-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9a58-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9a58-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9a58-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a58-108">說明</span><span class="sxs-lookup"><span data-stu-id="a9a58-108">DESCRIPTION</span></span>

<span data-ttu-id="a9a58-109">**Restore-AzRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="a9a58-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="a9a58-110">這個 Cmdlet 會從 [恢復服務] 保存庫開始還原到客戶的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9a58-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="a9a58-111">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a9a58-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="a9a58-112">它會復原磁碟資料和配置資訊。</span><span class="sxs-lookup"><span data-stu-id="a9a58-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="a9a58-113">完成還原作業之後，您必須建立並啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a9a58-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="a9a58-114">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="a9a58-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="a9a58-115">注意：若要成功執行此 Cmdlet，除了-VaultId 參數之外，也應該使用 VaultLocation 參數。</span><span class="sxs-lookup"><span data-stu-id="a9a58-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="a9a58-116">示例</span><span class="sxs-lookup"><span data-stu-id="a9a58-116">EXAMPLES</span></span>

### <span data-ttu-id="a9a58-117">範例1：將專案還原到復原點</span><span class="sxs-lookup"><span data-stu-id="a9a58-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="a9a58-118">第一個命令會取得類型為「Add-azurevm」的備份容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="a9a58-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a9a58-119">第二個命令會從 $Container 取得名為 V2VM 的備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="a9a58-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a9a58-120">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="a9a58-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="a9a58-121">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="a9a58-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="a9a58-122">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="a9a58-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="a9a58-123">指定的日期範圍是過去7天。</span><span class="sxs-lookup"><span data-stu-id="a9a58-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="a9a58-124">最後一個命令會將磁片還原為 [DestRG] 資源群組中的 [目標儲存空間] 帳戶 DestAccount。</span><span class="sxs-lookup"><span data-stu-id="a9a58-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="a9a58-125">參數</span><span class="sxs-lookup"><span data-stu-id="a9a58-125">PARAMETERS</span></span>

### <span data-ttu-id="a9a58-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a58-126">-DefaultProfile</span></span>

<span data-ttu-id="a9a58-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9a58-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9a58-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a9a58-128">-RecoveryPoint</span></span>

<span data-ttu-id="a9a58-129">指定要還原虛擬機器的復原點。</span><span class="sxs-lookup"><span data-stu-id="a9a58-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="a9a58-130">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 **AzRecoveryServicesBackupRecoveryPoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9a58-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="a9a58-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="a9a58-131">-ResolveConflict</span></span>

<span data-ttu-id="a9a58-132">如果還原的專案也存在於目的地中，請使用此選項來指出是否要覆寫。</span><span class="sxs-lookup"><span data-stu-id="a9a58-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="a9a58-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a9a58-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9a58-134">原有</span><span class="sxs-lookup"><span data-stu-id="a9a58-134">Overwrite</span></span>
- <span data-ttu-id="a9a58-135">跳</span><span class="sxs-lookup"><span data-stu-id="a9a58-135">Skip</span></span>

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

### <span data-ttu-id="a9a58-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="a9a58-136">-SourceFilePath</span></span>

<span data-ttu-id="a9a58-137">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="a9a58-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a9a58-138">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a9a58-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="a9a58-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="a9a58-139">-SourceFileType</span></span>

<span data-ttu-id="a9a58-140">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="a9a58-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a9a58-141">要在檔案共用中還原的專案類型。</span><span class="sxs-lookup"><span data-stu-id="a9a58-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="a9a58-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a9a58-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9a58-143">檔案</span><span class="sxs-lookup"><span data-stu-id="a9a58-143">File</span></span>
- <span data-ttu-id="a9a58-144">空目錄</span><span class="sxs-lookup"><span data-stu-id="a9a58-144">Directory</span></span>

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

### <span data-ttu-id="a9a58-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a9a58-145">-StorageAccountName</span></span>

<span data-ttu-id="a9a58-146">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9a58-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="a9a58-147">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="a9a58-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="a9a58-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a58-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="a9a58-149">指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9a58-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="a9a58-150">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="a9a58-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="a9a58-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="a9a58-151">-TargetFileShareName</span></span>

<span data-ttu-id="a9a58-152">檔案共用要還原到的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="a9a58-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="a9a58-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="a9a58-153">-TargetFolder</span></span>

<span data-ttu-id="a9a58-154">要在 TargetFileShareName 中還原檔案共用的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a9a58-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="a9a58-155">如果備份的內容要還原到根資料夾，請將目的檔案夾的值指定為空字串。</span><span class="sxs-lookup"><span data-stu-id="a9a58-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="a9a58-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a58-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="a9a58-157">要還原受管理磁片的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a9a58-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a9a58-158">適用于使用受管理磁片的 VM 備份</span><span class="sxs-lookup"><span data-stu-id="a9a58-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="a9a58-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a9a58-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="a9a58-160">檔案共用要還原到的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9a58-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="a9a58-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a9a58-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="a9a58-162">如果要將復原點的磁片還原到其原始儲存空間帳戶，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="a9a58-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="a9a58-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a9a58-163">-VaultId</span></span>

<span data-ttu-id="a9a58-164">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="a9a58-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a9a58-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="a9a58-165">-VaultLocation</span></span>

<span data-ttu-id="a9a58-166">[恢復服務] 保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="a9a58-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a9a58-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="a9a58-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="a9a58-168">復原配置</span><span class="sxs-lookup"><span data-stu-id="a9a58-168">Recovery config</span></span>

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

### <span data-ttu-id="a9a58-169">-確認</span><span class="sxs-lookup"><span data-stu-id="a9a58-169">-Confirm</span></span>

<span data-ttu-id="a9a58-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9a58-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a58-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a58-171">-WhatIf</span></span>

<span data-ttu-id="a9a58-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9a58-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9a58-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9a58-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a58-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a58-174">-CommonParameters</span></span>

<span data-ttu-id="a9a58-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9a58-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a58-176">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9a58-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a58-177">輸入</span><span class="sxs-lookup"><span data-stu-id="a9a58-177">INPUTS</span></span>

### <span data-ttu-id="a9a58-178">System.object</span><span class="sxs-lookup"><span data-stu-id="a9a58-178">System.String</span></span>

### <span data-ttu-id="a9a58-179">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="a9a58-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="a9a58-180">輸出</span><span class="sxs-lookup"><span data-stu-id="a9a58-180">OUTPUTS</span></span>

### <span data-ttu-id="a9a58-181">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="a9a58-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a9a58-182">筆記</span><span class="sxs-lookup"><span data-stu-id="a9a58-182">NOTES</span></span>

## <span data-ttu-id="a9a58-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9a58-183">RELATED LINKS</span></span>

[<span data-ttu-id="a9a58-184">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a9a58-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a9a58-185">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a9a58-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a9a58-186">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a9a58-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
