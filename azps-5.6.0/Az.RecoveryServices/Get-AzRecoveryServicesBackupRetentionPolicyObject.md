---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: bb1c63b41d27f92991a3504cdd5c2fd8fe547298
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903434"
---
# <span data-ttu-id="0c880-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0c880-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="0c880-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c880-102">SYNOPSIS</span></span>
<span data-ttu-id="0c880-103">獲得基本保留原則物件。</span><span class="sxs-lookup"><span data-stu-id="0c880-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="0c880-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c880-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c880-105">描述</span><span class="sxs-lookup"><span data-stu-id="0c880-105">DESCRIPTION</span></span>
<span data-ttu-id="0c880-106">**Get-AzRecoveryServicesBackupRetentionPolicyObject Cmdlet** 會取得基礎 **AzureRMRecoveryServicesRetentionPolicyObject。**</span><span class="sxs-lookup"><span data-stu-id="0c880-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="0c880-107">此物件不會持續存在系統中。</span><span class="sxs-lookup"><span data-stu-id="0c880-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="0c880-108">這是一個臨時物件，您可以操作並使用 New-AzRecoveryServicesBackupProtectionPolicy Cmdlet 來建立新的備份策略。</span><span class="sxs-lookup"><span data-stu-id="0c880-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="0c880-109">例子</span><span class="sxs-lookup"><span data-stu-id="0c880-109">EXAMPLES</span></span>

### <span data-ttu-id="0c880-110">範例 1：建立備份保護原則</span><span class="sxs-lookup"><span data-stu-id="0c880-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="0c880-111">第一個命令會獲得保留原則物件，然後將它儲存在$RetPol變數中。</span><span class="sxs-lookup"><span data-stu-id="0c880-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="0c880-112">第二個命令將保留原則物件的持續時間設定為 365 天。</span><span class="sxs-lookup"><span data-stu-id="0c880-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="0c880-113">第三個命令會獲得排程策略物件，然後將它儲存在$SchPol變數中。</span><span class="sxs-lookup"><span data-stu-id="0c880-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="0c880-114">最後一個命令會使用使用先前命令所建立之保留原則和排程策略來建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="0c880-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="0c880-115">參數</span><span class="sxs-lookup"><span data-stu-id="0c880-115">PARAMETERS</span></span>

### <span data-ttu-id="0c880-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0c880-116">-BackupManagementType</span></span>
<span data-ttu-id="0c880-117">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="0c880-117">The class of resources being protected.</span></span> <span data-ttu-id="0c880-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0c880-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c880-119">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="0c880-119">AzureVM</span></span> 
- <span data-ttu-id="0c880-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="0c880-120">AzureWorkload</span></span>
- <span data-ttu-id="0c880-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="0c880-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c880-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c880-122">-DefaultProfile</span></span>
<span data-ttu-id="0c880-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c880-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c880-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0c880-124">-WorkloadType</span></span>
<span data-ttu-id="0c880-125">資源的工作量類型。</span><span class="sxs-lookup"><span data-stu-id="0c880-125">Workload type of the resource.</span></span> <span data-ttu-id="0c880-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0c880-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c880-127">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="0c880-127">AzureVM</span></span> 
- <span data-ttu-id="0c880-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="0c880-128">AzureFiles</span></span>
- <span data-ttu-id="0c880-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="0c880-129">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c880-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c880-130">CommonParameters</span></span>
<span data-ttu-id="0c880-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c880-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c880-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c880-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c880-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0c880-133">INPUTS</span></span>

### <span data-ttu-id="0c880-134">沒有</span><span class="sxs-lookup"><span data-stu-id="0c880-134">None</span></span>

## <span data-ttu-id="0c880-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0c880-135">OUTPUTS</span></span>

### <span data-ttu-id="0c880-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="0c880-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="0c880-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0c880-137">NOTES</span></span>

## <span data-ttu-id="0c880-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c880-138">RELATED LINKS</span></span>

[<span data-ttu-id="0c880-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="0c880-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="0c880-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0c880-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


