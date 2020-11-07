---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 6c8debac9091d28091695847b36d0cbc1b219125
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791947"
---
# <span data-ttu-id="e486b-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e486b-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e486b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e486b-102">SYNOPSIS</span></span>

<span data-ttu-id="e486b-103">啟動備份專案的備份。</span><span class="sxs-lookup"><span data-stu-id="e486b-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="e486b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e486b-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e486b-105">說明</span><span class="sxs-lookup"><span data-stu-id="e486b-105">DESCRIPTION</span></span>

<span data-ttu-id="e486b-106">**AzRecoveryServicesBackupItem** Cmdlet 會針對受保護的 Azure 備份專案（未與備份排程關聯）啟動備份。</span><span class="sxs-lookup"><span data-stu-id="e486b-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="e486b-107">您可以在啟用保護後立即執行初始備份，或在排程備份失敗後啟動備份。</span><span class="sxs-lookup"><span data-stu-id="e486b-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="e486b-108">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="e486b-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="e486b-109">示例</span><span class="sxs-lookup"><span data-stu-id="e486b-109">EXAMPLES</span></span>

### <span data-ttu-id="e486b-110">範例1：啟動備份專案的備份</span><span class="sxs-lookup"><span data-stu-id="e486b-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="e486b-111">第一個命令會取得類型為 pstestv2vm1 的備份容器，然後將它儲存在 $NamedContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="e486b-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="e486b-112">第二個命令會取得與 $NamedContainer 容器相對應的備份專案，然後將其儲存在 $Item 變數中。</span><span class="sxs-lookup"><span data-stu-id="e486b-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="e486b-113">最後一個命令會在 $Item 中觸發備份專案的備份作業。</span><span class="sxs-lookup"><span data-stu-id="e486b-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="e486b-114">參數</span><span class="sxs-lookup"><span data-stu-id="e486b-114">PARAMETERS</span></span>

### <span data-ttu-id="e486b-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="e486b-115">-BackupType</span></span>

<span data-ttu-id="e486b-116">要執行的備份類型</span><span class="sxs-lookup"><span data-stu-id="e486b-116">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e486b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e486b-117">-DefaultProfile</span></span>

<span data-ttu-id="e486b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e486b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e486b-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="e486b-119">-EnableCompression</span></span>

<span data-ttu-id="e486b-120">如果需要啟用壓縮</span><span class="sxs-lookup"><span data-stu-id="e486b-120">If enabling compression is required</span></span>

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

### <span data-ttu-id="e486b-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="e486b-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="e486b-122">將到期時間指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="e486b-122">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e486b-123">-專案</span><span class="sxs-lookup"><span data-stu-id="e486b-123">-Item</span></span>

<span data-ttu-id="e486b-124">指定此 Cmdlet 啟動備份操作的備份專案。</span><span class="sxs-lookup"><span data-stu-id="e486b-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e486b-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e486b-125">-VaultId</span></span>

<span data-ttu-id="e486b-126">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="e486b-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e486b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e486b-127">-Confirm</span></span>

<span data-ttu-id="e486b-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e486b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e486b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e486b-129">-WhatIf</span></span>

<span data-ttu-id="e486b-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e486b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e486b-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e486b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e486b-132">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e486b-132">-CommonParameters</span></span>

<span data-ttu-id="e486b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e486b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e486b-134">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e486b-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e486b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e486b-135">INPUTS</span></span>

### <span data-ttu-id="e486b-136">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="e486b-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="e486b-137">System.object Null ' 1 [CoreLib，System.object = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e486b-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e486b-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e486b-138">System.String</span></span>

## <span data-ttu-id="e486b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e486b-139">OUTPUTS</span></span>

### <span data-ttu-id="e486b-140">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="e486b-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e486b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e486b-141">NOTES</span></span>

## <span data-ttu-id="e486b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e486b-142">RELATED LINKS</span></span>

[<span data-ttu-id="e486b-143">AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e486b-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="e486b-144">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e486b-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e486b-145">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e486b-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
