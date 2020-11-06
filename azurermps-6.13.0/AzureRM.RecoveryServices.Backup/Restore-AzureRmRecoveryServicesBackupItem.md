---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443748"
---
# <span data-ttu-id="032e8-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="032e8-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="032e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="032e8-102">SYNOPSIS</span></span>
<span data-ttu-id="032e8-103">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="032e8-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="032e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="032e8-104">SYNTAX</span></span>

### <span data-ttu-id="032e8-105">AzureVMParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="032e8-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="032e8-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="032e8-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="032e8-107">說明</span><span class="sxs-lookup"><span data-stu-id="032e8-107">DESCRIPTION</span></span>
<span data-ttu-id="032e8-108">**Restore-AzureRmRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="032e8-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="032e8-109">這個 Cmdlet 會從 [恢復服務] 保存庫開始還原到客戶的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="032e8-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="032e8-110">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="032e8-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="032e8-111">它會復原磁碟資料和配置資訊。</span><span class="sxs-lookup"><span data-stu-id="032e8-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="032e8-112">完成還原作業之後，您必須建立並啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="032e8-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="032e8-113">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="032e8-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="032e8-114">示例</span><span class="sxs-lookup"><span data-stu-id="032e8-114">EXAMPLES</span></span>

### <span data-ttu-id="032e8-115">範例1：將專案還原到復原點</span><span class="sxs-lookup"><span data-stu-id="032e8-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="032e8-116">第一個命令會取得類型為「Add-azurevm」的備份容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="032e8-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="032e8-117">第二個命令會從 $Container 取得名為 V2VM 的備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="032e8-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="032e8-118">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="032e8-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="032e8-119">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="032e8-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="032e8-120">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="032e8-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="032e8-121">指定的日期範圍是過去7天。</span><span class="sxs-lookup"><span data-stu-id="032e8-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="032e8-122">最後一個命令會將磁片還原為 [DestRG] 資源群組中的 [目標儲存空間] 帳戶 DestAccount。</span><span class="sxs-lookup"><span data-stu-id="032e8-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="032e8-123">參數</span><span class="sxs-lookup"><span data-stu-id="032e8-123">PARAMETERS</span></span>

### <span data-ttu-id="032e8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032e8-124">-DefaultProfile</span></span>
<span data-ttu-id="032e8-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="032e8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032e8-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="032e8-126">-RecoveryPoint</span></span>
<span data-ttu-id="032e8-127">指定要還原虛擬機器的復原點。</span><span class="sxs-lookup"><span data-stu-id="032e8-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="032e8-128">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 Get-AzureRmRecoveryServicesBackupRecoveryPoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="032e8-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="032e8-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="032e8-129">-ResolveConflict</span></span>
<span data-ttu-id="032e8-130">如果還原的專案也存在於目的地中，請使用此選項來指出是否要覆寫。</span><span class="sxs-lookup"><span data-stu-id="032e8-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032e8-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="032e8-131">-SourceFilePath</span></span>
<span data-ttu-id="032e8-132">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="032e8-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="032e8-133">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="032e8-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="032e8-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="032e8-134">-SourceFileType</span></span>
<span data-ttu-id="032e8-135">用於從檔案共用還原特定專案。</span><span class="sxs-lookup"><span data-stu-id="032e8-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="032e8-136">要在檔案共用中還原之專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="032e8-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032e8-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="032e8-137">-StorageAccountName</span></span>
<span data-ttu-id="032e8-138">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="032e8-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="032e8-139">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="032e8-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032e8-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032e8-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="032e8-141">指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="032e8-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="032e8-142">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="032e8-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032e8-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="032e8-143">-TargetFileShareName</span></span>
<span data-ttu-id="032e8-144">檔案共用要還原到的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="032e8-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="032e8-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="032e8-145">-TargetFolder</span></span>
<span data-ttu-id="032e8-146">要在 targetFileShareName 中將檔案共用還原到哪個資料夾。請將該變數留白，以便在 [根資料夾] 下還原。</span><span class="sxs-lookup"><span data-stu-id="032e8-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="032e8-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032e8-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="032e8-148">要還原受管理磁片的資源群組。</span><span class="sxs-lookup"><span data-stu-id="032e8-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="032e8-149">適用于使用受管理磁片的 VM 備份</span><span class="sxs-lookup"><span data-stu-id="032e8-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="032e8-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="032e8-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="032e8-151">檔案共用要還原到的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="032e8-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="032e8-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="032e8-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="032e8-153">如果要將復原點的磁片還原到其原始儲存空間帳戶，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="032e8-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="032e8-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="032e8-154">-VaultId</span></span>
<span data-ttu-id="032e8-155">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="032e8-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="032e8-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="032e8-156">-VaultLocation</span></span>
<span data-ttu-id="032e8-157">[恢復服務] 保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="032e8-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="032e8-158">-確認</span><span class="sxs-lookup"><span data-stu-id="032e8-158">-Confirm</span></span>
<span data-ttu-id="032e8-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="032e8-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="032e8-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="032e8-160">-WhatIf</span></span>
<span data-ttu-id="032e8-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="032e8-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="032e8-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="032e8-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="032e8-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032e8-163">CommonParameters</span></span>
<span data-ttu-id="032e8-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="032e8-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032e8-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="032e8-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032e8-166">輸入</span><span class="sxs-lookup"><span data-stu-id="032e8-166">INPUTS</span></span>

### <span data-ttu-id="032e8-167">System.object</span><span class="sxs-lookup"><span data-stu-id="032e8-167">System.String</span></span>
<span data-ttu-id="032e8-168">參數： VaultId (ByValue) ，VaultLocation (ByValue) </span><span class="sxs-lookup"><span data-stu-id="032e8-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="032e8-169">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="032e8-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="032e8-170">參數： RecoveryPoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="032e8-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="032e8-171">輸出</span><span class="sxs-lookup"><span data-stu-id="032e8-171">OUTPUTS</span></span>

### <span data-ttu-id="032e8-172">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="032e8-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="032e8-173">筆記</span><span class="sxs-lookup"><span data-stu-id="032e8-173">NOTES</span></span>

## <span data-ttu-id="032e8-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="032e8-174">RELATED LINKS</span></span>

[<span data-ttu-id="032e8-175">備份-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="032e8-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="032e8-176">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="032e8-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="032e8-177">AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="032e8-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


