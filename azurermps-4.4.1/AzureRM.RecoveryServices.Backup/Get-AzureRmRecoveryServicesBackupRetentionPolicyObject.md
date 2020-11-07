---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 5fd705d38f2deb232c9b62861804eb2830f45999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625975"
---
# <span data-ttu-id="35fc9-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="35fc9-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="35fc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="35fc9-103">取得基本保留原則物件。</span><span class="sxs-lookup"><span data-stu-id="35fc9-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35fc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="35fc9-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35fc9-105">說明</span><span class="sxs-lookup"><span data-stu-id="35fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="35fc9-106">**AzureRmRecoveryServicesBackupRetentionPolicyObject** Cmdlet 會取得基 **AzureRMRecoveryServicesRetentionPolicyObject** 。</span><span class="sxs-lookup"><span data-stu-id="35fc9-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="35fc9-107">這個物件不會在系統中保留。</span><span class="sxs-lookup"><span data-stu-id="35fc9-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="35fc9-108">這是一個暫時物件，您可以使用 New-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet 來處理及搭配使用，以建立新的備份原則。</span><span class="sxs-lookup"><span data-stu-id="35fc9-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="35fc9-109">示例</span><span class="sxs-lookup"><span data-stu-id="35fc9-109">EXAMPLES</span></span>

### <span data-ttu-id="35fc9-110">範例1：建立備份保護原則</span><span class="sxs-lookup"><span data-stu-id="35fc9-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="35fc9-111">第一個命令會取得保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="35fc9-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="35fc9-112">第二個命令會將 [保留原則] 物件的持續時間設為365天。</span><span class="sxs-lookup"><span data-stu-id="35fc9-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="35fc9-113">第三個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="35fc9-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="35fc9-114">最後一個命令會使用保留原則和使用先前命令建立的排程原則，建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="35fc9-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="35fc9-115">參數</span><span class="sxs-lookup"><span data-stu-id="35fc9-115">PARAMETERS</span></span>

### <span data-ttu-id="35fc9-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="35fc9-116">-BackupManagementType</span></span>
<span data-ttu-id="35fc9-117">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="35fc9-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="35fc9-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="35fc9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35fc9-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="35fc9-119">AzureVM</span></span> 
- <span data-ttu-id="35fc9-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="35fc9-120">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fc9-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="35fc9-121">-WorkloadType</span></span>
<span data-ttu-id="35fc9-122">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="35fc9-122">Specifies the workload type.</span></span>
<span data-ttu-id="35fc9-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="35fc9-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35fc9-124">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="35fc9-124">AzureVM</span></span> 
- <span data-ttu-id="35fc9-125">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="35fc9-125">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35fc9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fc9-126">-DefaultProfile</span></span>
<span data-ttu-id="35fc9-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35fc9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35fc9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fc9-128">CommonParameters</span></span>
<span data-ttu-id="35fc9-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35fc9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fc9-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35fc9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fc9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="35fc9-131">INPUTS</span></span>

## <span data-ttu-id="35fc9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="35fc9-132">OUTPUTS</span></span>

### <span data-ttu-id="35fc9-133">RetentionPolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="35fc9-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="35fc9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="35fc9-134">NOTES</span></span>

## <span data-ttu-id="35fc9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="35fc9-135">RELATED LINKS</span></span>

[<span data-ttu-id="35fc9-136">AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="35fc9-136">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="35fc9-137">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="35fc9-137">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


