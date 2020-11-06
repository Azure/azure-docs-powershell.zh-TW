---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: c12241457b78d9020e447b6f464d5623e90d52b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455647"
---
# <span data-ttu-id="4c429-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4c429-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="4c429-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c429-102">SYNOPSIS</span></span>
<span data-ttu-id="4c429-103">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="4c429-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c429-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c429-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c429-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c429-105">DESCRIPTION</span></span>
<span data-ttu-id="4c429-106">**Restore-AzureRmRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="4c429-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="4c429-107">這個 Cmdlet 會從 [恢復服務] 保存庫開始還原到客戶的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="4c429-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="4c429-108">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4c429-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="4c429-109">它會復原磁碟資料和配置資訊。</span><span class="sxs-lookup"><span data-stu-id="4c429-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="4c429-110">完成還原作業之後，您必須建立並啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4c429-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="4c429-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c429-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4c429-112">示例</span><span class="sxs-lookup"><span data-stu-id="4c429-112">EXAMPLES</span></span>

### <span data-ttu-id="4c429-113">範例1：將專案還原到復原點</span><span class="sxs-lookup"><span data-stu-id="4c429-113">Example 1: Restore an item to a recovery point</span></span>
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

<span data-ttu-id="4c429-114">第一個命令會取得類型為「Add-azurevm」的備份容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c429-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="4c429-115">第二個命令會從 $Container 取得名為 V2VM 的備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c429-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="4c429-116">第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c429-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="4c429-117">第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c429-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="4c429-118">第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。</span><span class="sxs-lookup"><span data-stu-id="4c429-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="4c429-119">指定的日期範圍是過去7天。</span><span class="sxs-lookup"><span data-stu-id="4c429-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="4c429-120">最後一個命令會將磁片還原為 [DestRG] 資源群組中的 [目標儲存空間] 帳戶 DestAccount。</span><span class="sxs-lookup"><span data-stu-id="4c429-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="4c429-121">參數</span><span class="sxs-lookup"><span data-stu-id="4c429-121">PARAMETERS</span></span>

### <span data-ttu-id="4c429-122">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4c429-122">-RecoveryPoint</span></span>
<span data-ttu-id="4c429-123">指定要還原虛擬機器的復原點。</span><span class="sxs-lookup"><span data-stu-id="4c429-123">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="4c429-124">若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 Get-AzureRmRecoveryServicesBackupRecoveryPoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c429-124">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="4c429-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4c429-125">-StorageAccountName</span></span>
<span data-ttu-id="4c429-126">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c429-126">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="4c429-127">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="4c429-127">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="4c429-128">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c429-128">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="4c429-129">指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c429-129">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="4c429-130">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="4c429-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="4c429-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c429-131">-DefaultProfile</span></span>
<span data-ttu-id="4c429-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c429-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c429-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c429-133">CommonParameters</span></span>
<span data-ttu-id="4c429-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c429-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c429-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c429-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c429-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4c429-136">INPUTS</span></span>

### <span data-ttu-id="4c429-137">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="4c429-137">RecoveryPointBase</span></span>
<span data-ttu-id="4c429-138">形參 "RecoveryPoint" 接受管線中 "RecoveryPointBase" 類型的值</span><span class="sxs-lookup"><span data-stu-id="4c429-138">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="4c429-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4c429-139">OUTPUTS</span></span>

### <span data-ttu-id="4c429-140">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="4c429-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4c429-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4c429-141">NOTES</span></span>

## <span data-ttu-id="4c429-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c429-142">RELATED LINKS</span></span>

[<span data-ttu-id="4c429-143">備份-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4c429-143">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="4c429-144">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4c429-144">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="4c429-145">AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4c429-145">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


