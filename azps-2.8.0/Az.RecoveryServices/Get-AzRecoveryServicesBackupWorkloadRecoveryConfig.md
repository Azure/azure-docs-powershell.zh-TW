---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4a3ab7ca60807f294ee5739116c8b8bcc965ae2e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791870"
---
# <span data-ttu-id="47628-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="47628-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="47628-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47628-102">SYNOPSIS</span></span>
<span data-ttu-id="47628-103">這個命令會構造已備份專案（例如 SQL 資料庫）的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="47628-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="47628-104">[設定] 物件會儲存所有詳細資料，例如 [還原] 模式、[還原] 和 [應用程式特定] 參數（例如 [SQL] 的目標實體路徑）。</span><span class="sxs-lookup"><span data-stu-id="47628-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="47628-105">句法</span><span class="sxs-lookup"><span data-stu-id="47628-105">SYNTAX</span></span>

### <span data-ttu-id="47628-106">RpParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="47628-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47628-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="47628-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47628-108">說明</span><span class="sxs-lookup"><span data-stu-id="47628-108">DESCRIPTION</span></span>
<span data-ttu-id="47628-109">此命令會針對傳遞到 restore Cmdlet 的 AzureWorkload 專案傳回復原配置。</span><span class="sxs-lookup"><span data-stu-id="47628-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="47628-110">示例</span><span class="sxs-lookup"><span data-stu-id="47628-110">EXAMPLES</span></span>

### <span data-ttu-id="47628-111">範例1</span><span class="sxs-lookup"><span data-stu-id="47628-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="47628-112">第一個 Cmdlet 是用來取得復原點物件。</span><span class="sxs-lookup"><span data-stu-id="47628-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="47628-113">第二個 Cmdlet 會建立原始位置還原的恢復方案。</span><span class="sxs-lookup"><span data-stu-id="47628-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="47628-114">第三個 Cmdlet 會建立備用位置還原的恢復方案。</span><span class="sxs-lookup"><span data-stu-id="47628-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="47628-115">參數</span><span class="sxs-lookup"><span data-stu-id="47628-115">PARAMETERS</span></span>

### <span data-ttu-id="47628-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="47628-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="47628-117">指定備份的資料庫將由復原點中出現的 DB 資訊覆寫。</span><span class="sxs-lookup"><span data-stu-id="47628-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="47628-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47628-118">-DefaultProfile</span></span>
<span data-ttu-id="47628-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47628-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47628-120">-專案</span><span class="sxs-lookup"><span data-stu-id="47628-120">-Item</span></span>
<span data-ttu-id="47628-121">指定執行還原操作的備份專案。</span><span class="sxs-lookup"><span data-stu-id="47628-121">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="47628-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="47628-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="47628-123">指定備份的資料庫將由復原點中出現的 DB 資訊覆寫。</span><span class="sxs-lookup"><span data-stu-id="47628-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="47628-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="47628-124">-PointInTime</span></span>
<span data-ttu-id="47628-125">需要回遷復原點之時間範圍的結束時間</span><span class="sxs-lookup"><span data-stu-id="47628-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="47628-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="47628-126">-RecoveryPoint</span></span>
<span data-ttu-id="47628-127">要還原的復原點物件</span><span class="sxs-lookup"><span data-stu-id="47628-127">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="47628-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="47628-128">-TargetItem</span></span>
<span data-ttu-id="47628-129">指定需要還原資料庫的目標。</span><span class="sxs-lookup"><span data-stu-id="47628-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="47628-130">若是 SQL 還原，則必須是只能進行受保護的專案類型 SQLInstance。</span><span class="sxs-lookup"><span data-stu-id="47628-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="47628-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="47628-131">-VaultId</span></span>
<span data-ttu-id="47628-132">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="47628-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="47628-133">-確認</span><span class="sxs-lookup"><span data-stu-id="47628-133">-Confirm</span></span>
<span data-ttu-id="47628-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47628-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47628-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47628-135">-WhatIf</span></span>
<span data-ttu-id="47628-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47628-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47628-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47628-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47628-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47628-138">CommonParameters</span></span>
<span data-ttu-id="47628-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47628-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47628-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47628-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47628-141">輸入</span><span class="sxs-lookup"><span data-stu-id="47628-141">INPUTS</span></span>

### <span data-ttu-id="47628-142">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="47628-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="47628-143">System.object</span><span class="sxs-lookup"><span data-stu-id="47628-143">System.String</span></span>

## <span data-ttu-id="47628-144">輸出</span><span class="sxs-lookup"><span data-stu-id="47628-144">OUTPUTS</span></span>

### <span data-ttu-id="47628-145">RecoveryConfigBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="47628-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="47628-146">筆記</span><span class="sxs-lookup"><span data-stu-id="47628-146">NOTES</span></span>

## <span data-ttu-id="47628-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="47628-147">RELATED LINKS</span></span>