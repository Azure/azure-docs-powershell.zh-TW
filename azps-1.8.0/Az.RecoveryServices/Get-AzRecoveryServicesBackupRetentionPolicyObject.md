---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: b3a1c990f8dff3b91c9e46fd1f01da734e47f963
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621136"
---
# <span data-ttu-id="c6eb5-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c6eb5-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="c6eb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="c6eb5-103">取得基本保留原則物件。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="c6eb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6eb5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6eb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="c6eb5-106">**AzRecoveryServicesBackupRetentionPolicyObject** Cmdlet 會取得基 **AzureRMRecoveryServicesRetentionPolicyObject** 。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="c6eb5-107">這個物件不會在系統中保留。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="c6eb5-108">這是一個暫時物件，您可以使用 New-AzRecoveryServicesBackupProtectionPolicy Cmdlet 來處理及搭配使用，以建立新的備份原則。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="c6eb5-109">示例</span><span class="sxs-lookup"><span data-stu-id="c6eb5-109">EXAMPLES</span></span>

### <span data-ttu-id="c6eb5-110">範例1：建立備份保護原則</span><span class="sxs-lookup"><span data-stu-id="c6eb5-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="c6eb5-111">第一個命令會取得保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="c6eb5-112">第二個命令會將 [保留原則] 物件的持續時間設為365天。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="c6eb5-113">第三個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="c6eb5-114">最後一個命令會使用保留原則和使用先前命令建立的排程原則，建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="c6eb5-115">參數</span><span class="sxs-lookup"><span data-stu-id="c6eb5-115">PARAMETERS</span></span>

### <span data-ttu-id="c6eb5-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="c6eb5-116">-BackupManagementType</span></span>
<span data-ttu-id="c6eb5-117">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="c6eb5-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c6eb5-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6eb5-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="c6eb5-119">AzureVM</span></span> 
- <span data-ttu-id="c6eb5-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="c6eb5-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="c6eb5-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="c6eb5-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6eb5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6eb5-122">-DefaultProfile</span></span>
<span data-ttu-id="c6eb5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6eb5-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c6eb5-124">-WorkloadType</span></span>
<span data-ttu-id="c6eb5-125">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-125">Specifies the workload type.</span></span>
<span data-ttu-id="c6eb5-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c6eb5-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6eb5-127">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="c6eb5-127">AzureVM</span></span> 
- <span data-ttu-id="c6eb5-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="c6eb5-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="c6eb5-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="c6eb5-129">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6eb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6eb5-130">CommonParameters</span></span>
<span data-ttu-id="c6eb5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6eb5-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6eb5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6eb5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c6eb5-133">INPUTS</span></span>

### <span data-ttu-id="c6eb5-134">所有</span><span class="sxs-lookup"><span data-stu-id="c6eb5-134">None</span></span>

## <span data-ttu-id="c6eb5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c6eb5-135">OUTPUTS</span></span>

### <span data-ttu-id="c6eb5-136">RetentionPolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="c6eb5-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="c6eb5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c6eb5-137">NOTES</span></span>

## <span data-ttu-id="c6eb5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6eb5-138">RELATED LINKS</span></span>

[<span data-ttu-id="c6eb5-139">AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="c6eb5-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="c6eb5-140">新-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c6eb5-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


