---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 0eaabc025a9252cdd48500f294fab699e7ebea1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914693"
---
# <span data-ttu-id="ef3c4-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef3c4-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="ef3c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3c4-103">取消進行中的工作。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-103">Cancels a running job.</span></span>

## <span data-ttu-id="ef3c4-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef3c4-104">SYNTAX</span></span>

### <span data-ttu-id="ef3c4-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ef3c4-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3c4-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="ef3c4-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef3c4-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef3c4-107">DESCRIPTION</span></span>
<span data-ttu-id="ef3c4-108">**Stop-AzRecoveryServicesBackupJob** Cmdlet 會取消現有的 Azure 備份工作。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="ef3c4-109">使用此 Cmdlet 可以停止花費太多時間並阻止其他活動的工作。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="ef3c4-110">您可以只取消備份和還原工作類型。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="ef3c4-111">使用目前的 Cmdlet 之前，使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定庫內容。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ef3c4-112">例子</span><span class="sxs-lookup"><span data-stu-id="ef3c4-112">EXAMPLES</span></span>

### <span data-ttu-id="ef3c4-113">範例 1：停止備份工作</span><span class="sxs-lookup"><span data-stu-id="ef3c4-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="ef3c4-114">第一個命令會獲得備份工作，然後將該工作儲存在$Job變數。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="ef3c4-115">最後一個命令會停止工作，在 $Job 中指定備份工作的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="ef3c4-116">參數</span><span class="sxs-lookup"><span data-stu-id="ef3c4-116">PARAMETERS</span></span>

### <span data-ttu-id="ef3c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3c4-117">-DefaultProfile</span></span>
<span data-ttu-id="ef3c4-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef3c4-119">-Job</span><span class="sxs-lookup"><span data-stu-id="ef3c4-119">-Job</span></span>
<span data-ttu-id="ef3c4-120">指定此 Cmdlet 取消的工作。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="ef3c4-121">若要取得 **BackupJob 物件** ，請使用 Get-AzRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef3c4-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="ef3c4-122">-JobId</span></span>
<span data-ttu-id="ef3c4-123">指定要取消的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="ef3c4-124">識別碼是 **BackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="ef3c4-125">若要取得 **BackupJob 物件** ，請使用 Get-AzRecoveryServicesBackupJob。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef3c4-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ef3c4-126">-VaultId</span></span>
<span data-ttu-id="ef3c4-127">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ef3c4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ef3c4-128">-Confirm</span></span>
<span data-ttu-id="ef3c4-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef3c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef3c4-130">-WhatIf</span></span>
<span data-ttu-id="ef3c4-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ef3c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3c4-132">CommonParameters</span></span>
<span data-ttu-id="ef3c4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef3c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3c4-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef3c4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3c4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ef3c4-135">INPUTS</span></span>

### <span data-ttu-id="ef3c4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ef3c4-136">System.String</span></span>

## <span data-ttu-id="ef3c4-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ef3c4-137">OUTPUTS</span></span>

### <span data-ttu-id="ef3c4-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="ef3c4-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ef3c4-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ef3c4-139">NOTES</span></span>

## <span data-ttu-id="ef3c4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef3c4-140">RELATED LINKS</span></span>

[<span data-ttu-id="ef3c4-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef3c4-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="ef3c4-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ef3c4-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


