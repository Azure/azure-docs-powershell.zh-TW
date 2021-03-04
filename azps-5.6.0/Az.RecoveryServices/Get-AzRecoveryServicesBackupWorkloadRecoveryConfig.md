---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: d608b4265435041a918ba71cdd68ae00892bcc20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903793"
---
# <span data-ttu-id="28fa0-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="28fa0-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="28fa0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="28fa0-103">此命令會建構備份專案的復原組態，例如 SQL DB。</span><span class="sxs-lookup"><span data-stu-id="28fa0-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="28fa0-104">設定物件會儲存所有詳細資料，例如復原模式、還原的目標目的地，以及應用程式特定參數 ，例如 SQL 的目標實體路徑。</span><span class="sxs-lookup"><span data-stu-id="28fa0-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="28fa0-105">語法</span><span class="sxs-lookup"><span data-stu-id="28fa0-105">SYNTAX</span></span>

### <span data-ttu-id="28fa0-106">RpParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28fa0-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28fa0-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="28fa0-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28fa0-108">描述</span><span class="sxs-lookup"><span data-stu-id="28fa0-108">DESCRIPTION</span></span>
<span data-ttu-id="28fa0-109">該命令會傳回傳遞至還原 Cmdlet 的 AzureWorkload 專案的復原設定檔。</span><span class="sxs-lookup"><span data-stu-id="28fa0-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="28fa0-110">例子</span><span class="sxs-lookup"><span data-stu-id="28fa0-110">EXAMPLES</span></span>

### <span data-ttu-id="28fa0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="28fa0-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="28fa0-112">第一個 Cmdlet 是用來取得修復點物件。</span><span class="sxs-lookup"><span data-stu-id="28fa0-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="28fa0-113">第二個 Cmdlet 會為原始位置還原建立復原計畫。</span><span class="sxs-lookup"><span data-stu-id="28fa0-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="28fa0-114">第三個 Cmdlet 會針對替代位置還原建立復原計畫。</span><span class="sxs-lookup"><span data-stu-id="28fa0-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="28fa0-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="28fa0-115">Example 2</span></span>

<span data-ttu-id="28fa0-116">此命令會建構備份專案的復原組態，例如 SQL DB。</span><span class="sxs-lookup"><span data-stu-id="28fa0-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="28fa0-117"> (自動) </span><span class="sxs-lookup"><span data-stu-id="28fa0-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="28fa0-118">參數</span><span class="sxs-lookup"><span data-stu-id="28fa0-118">PARAMETERS</span></span>

### <span data-ttu-id="28fa0-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="28fa0-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="28fa0-120">指定備份 DB 應還原到另一個選取的伺服器。</span><span class="sxs-lookup"><span data-stu-id="28fa0-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28fa0-121">-DefaultProfile</span></span>
<span data-ttu-id="28fa0-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28fa0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28fa0-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="28fa0-123">-FilePath</span></span>
<span data-ttu-id="28fa0-124">指定用於還原作業的 filepath。</span><span class="sxs-lookup"><span data-stu-id="28fa0-124">Specifies the filepath which is used for restore operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="28fa0-125">-FromFull</span></span>
<span data-ttu-id="28fa0-126">指定要將記錄備份用於的完整修複Point。</span><span class="sxs-lookup"><span data-stu-id="28fa0-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-127">-專案</span><span class="sxs-lookup"><span data-stu-id="28fa0-127">-Item</span></span>
<span data-ttu-id="28fa0-128">指定執行還原作業的備份專案。</span><span class="sxs-lookup"><span data-stu-id="28fa0-128">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="28fa0-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="28fa0-130">指定備份的 DB 會以復原點中的 DB 資訊進行覆蓋。</span><span class="sxs-lookup"><span data-stu-id="28fa0-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="28fa0-131">-PointInTime</span></span>
<span data-ttu-id="28fa0-132">需要抓取復原點之時間範圍的結束時間</span><span class="sxs-lookup"><span data-stu-id="28fa0-132">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="28fa0-133">-RecoveryPoint</span></span>
<span data-ttu-id="28fa0-134">要還原的修復點物件</span><span class="sxs-lookup"><span data-stu-id="28fa0-134">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="28fa0-135">-RestoreAsFiles</span></span>
<span data-ttu-id="28fa0-136">指定將資料庫還原為電腦中的檔案。</span><span class="sxs-lookup"><span data-stu-id="28fa0-136">Specifies to restore Database as files in a machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="28fa0-137">-TargetContainer</span></span>
<span data-ttu-id="28fa0-138">指定需要還原 DB 檔案的目的電腦。</span><span class="sxs-lookup"><span data-stu-id="28fa0-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="28fa0-139">-TargetItem</span></span>
<span data-ttu-id="28fa0-140">指定需要還原 DB 的目標。</span><span class="sxs-lookup"><span data-stu-id="28fa0-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="28fa0-141">針對 SQL 還原，它只需要為可保護的專案類型 SQLInstance。</span><span class="sxs-lookup"><span data-stu-id="28fa0-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fa0-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="28fa0-142">-VaultId</span></span>
<span data-ttu-id="28fa0-143">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="28fa0-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="28fa0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28fa0-144">CommonParameters</span></span>
<span data-ttu-id="28fa0-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28fa0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28fa0-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28fa0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28fa0-147">輸入</span><span class="sxs-lookup"><span data-stu-id="28fa0-147">INPUTS</span></span>

### <span data-ttu-id="28fa0-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="28fa0-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="28fa0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="28fa0-149">System.String</span></span>

## <span data-ttu-id="28fa0-150">輸出</span><span class="sxs-lookup"><span data-stu-id="28fa0-150">OUTPUTS</span></span>

### <span data-ttu-id="28fa0-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="28fa0-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="28fa0-152">筆記</span><span class="sxs-lookup"><span data-stu-id="28fa0-152">NOTES</span></span>

## <span data-ttu-id="28fa0-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="28fa0-153">RELATED LINKS</span></span>
