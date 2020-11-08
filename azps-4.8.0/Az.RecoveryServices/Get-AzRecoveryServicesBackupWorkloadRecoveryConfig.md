---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128667"
---
# <span data-ttu-id="255bf-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="255bf-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="255bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="255bf-102">SYNOPSIS</span></span>
<span data-ttu-id="255bf-103">這個命令會構造已備份專案（例如 SQL 資料庫）的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="255bf-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="255bf-104">[設定] 物件會儲存所有詳細資料，例如 [還原] 模式、[還原] 和 [應用程式特定] 參數（例如 [SQL] 的目標實體路徑）。</span><span class="sxs-lookup"><span data-stu-id="255bf-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="255bf-105">句法</span><span class="sxs-lookup"><span data-stu-id="255bf-105">SYNTAX</span></span>

### <span data-ttu-id="255bf-106">RpParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="255bf-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="255bf-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="255bf-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="255bf-108">說明</span><span class="sxs-lookup"><span data-stu-id="255bf-108">DESCRIPTION</span></span>
<span data-ttu-id="255bf-109">此命令會針對傳遞到 restore Cmdlet 的 AzureWorkload 專案傳回復原配置。</span><span class="sxs-lookup"><span data-stu-id="255bf-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="255bf-110">示例</span><span class="sxs-lookup"><span data-stu-id="255bf-110">EXAMPLES</span></span>

### <span data-ttu-id="255bf-111">範例1</span><span class="sxs-lookup"><span data-stu-id="255bf-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="255bf-112">第一個 Cmdlet 是用來取得復原點物件。</span><span class="sxs-lookup"><span data-stu-id="255bf-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="255bf-113">第二個 Cmdlet 會建立原始位置還原的恢復方案。</span><span class="sxs-lookup"><span data-stu-id="255bf-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="255bf-114">第三個 Cmdlet 會建立備用位置還原的恢復方案。</span><span class="sxs-lookup"><span data-stu-id="255bf-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="255bf-115">範例2</span><span class="sxs-lookup"><span data-stu-id="255bf-115">Example 2</span></span>

<span data-ttu-id="255bf-116">這個命令會構造已備份專案（例如 SQL 資料庫）的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="255bf-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="255bf-117"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="255bf-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="255bf-118">參數</span><span class="sxs-lookup"><span data-stu-id="255bf-118">PARAMETERS</span></span>

### <span data-ttu-id="255bf-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="255bf-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="255bf-120">指定備份的資料庫應該還原到另一個選取的伺服器。</span><span class="sxs-lookup"><span data-stu-id="255bf-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="255bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255bf-121">-DefaultProfile</span></span>
<span data-ttu-id="255bf-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="255bf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="255bf-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="255bf-123">-FilePath</span></span>
<span data-ttu-id="255bf-124">指定用於還原操作的 filepath。</span><span class="sxs-lookup"><span data-stu-id="255bf-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="255bf-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="255bf-125">-FromFull</span></span>
<span data-ttu-id="255bf-126">指定將套用記錄備份的完整 RecoveryPoint。</span><span class="sxs-lookup"><span data-stu-id="255bf-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="255bf-127">-專案</span><span class="sxs-lookup"><span data-stu-id="255bf-127">-Item</span></span>
<span data-ttu-id="255bf-128">指定執行還原操作的備份專案。</span><span class="sxs-lookup"><span data-stu-id="255bf-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="255bf-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="255bf-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="255bf-130">指定備份的資料庫將由復原點中出現的 DB 資訊覆寫。</span><span class="sxs-lookup"><span data-stu-id="255bf-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="255bf-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="255bf-131">-PointInTime</span></span>
<span data-ttu-id="255bf-132">需要回遷復原點之時間範圍的結束時間</span><span class="sxs-lookup"><span data-stu-id="255bf-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="255bf-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="255bf-133">-RecoveryPoint</span></span>
<span data-ttu-id="255bf-134">要還原的復原點物件</span><span class="sxs-lookup"><span data-stu-id="255bf-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="255bf-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="255bf-135">-RestoreAsFiles</span></span>
<span data-ttu-id="255bf-136">指定將資料庫還原為電腦中的檔案。</span><span class="sxs-lookup"><span data-stu-id="255bf-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="255bf-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="255bf-137">-TargetContainer</span></span>
<span data-ttu-id="255bf-138">指定需要還原 DB 檔案的目的電腦。</span><span class="sxs-lookup"><span data-stu-id="255bf-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="255bf-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="255bf-139">-TargetItem</span></span>
<span data-ttu-id="255bf-140">指定需要還原資料庫的目標。</span><span class="sxs-lookup"><span data-stu-id="255bf-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="255bf-141">若是 SQL 還原，則必須是只能進行受保護的專案類型 SQLInstance。</span><span class="sxs-lookup"><span data-stu-id="255bf-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="255bf-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="255bf-142">-VaultId</span></span>
<span data-ttu-id="255bf-143">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="255bf-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="255bf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255bf-144">CommonParameters</span></span>
<span data-ttu-id="255bf-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="255bf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255bf-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="255bf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255bf-147">輸入</span><span class="sxs-lookup"><span data-stu-id="255bf-147">INPUTS</span></span>

### <span data-ttu-id="255bf-148">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="255bf-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="255bf-149">System.object</span><span class="sxs-lookup"><span data-stu-id="255bf-149">System.String</span></span>

## <span data-ttu-id="255bf-150">輸出</span><span class="sxs-lookup"><span data-stu-id="255bf-150">OUTPUTS</span></span>

### <span data-ttu-id="255bf-151">RecoveryConfigBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="255bf-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="255bf-152">筆記</span><span class="sxs-lookup"><span data-stu-id="255bf-152">NOTES</span></span>

## <span data-ttu-id="255bf-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="255bf-153">RELATED LINKS</span></span>