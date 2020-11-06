---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83ed9062c5ad4beb0dff9c9c89b79a443cc68a52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446116"
---
# <span data-ttu-id="627b1-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="627b1-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="627b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="627b1-102">SYNOPSIS</span></span>
<span data-ttu-id="627b1-103">取得基本保留原則物件。</span><span class="sxs-lookup"><span data-stu-id="627b1-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="627b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="627b1-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="627b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="627b1-105">DESCRIPTION</span></span>
<span data-ttu-id="627b1-106">**AzureRmRecoveryServicesBackupRetentionPolicyObject** Cmdlet 會取得基 **AzureRMRecoveryServicesRetentionPolicyObject** 。</span><span class="sxs-lookup"><span data-stu-id="627b1-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="627b1-107">這個物件不會在系統中保留。</span><span class="sxs-lookup"><span data-stu-id="627b1-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="627b1-108">這是一個暫時物件，您可以使用 New-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet 來處理及搭配使用，以建立新的備份原則。</span><span class="sxs-lookup"><span data-stu-id="627b1-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="627b1-109">示例</span><span class="sxs-lookup"><span data-stu-id="627b1-109">EXAMPLES</span></span>

### <span data-ttu-id="627b1-110">範例1：建立備份保護原則</span><span class="sxs-lookup"><span data-stu-id="627b1-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="627b1-111">第一個命令會取得保留原則物件，然後將它儲存在 $RetPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="627b1-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="627b1-112">第二個命令會將 [保留原則] 物件的持續時間設為365天。</span><span class="sxs-lookup"><span data-stu-id="627b1-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="627b1-113">第三個命令會取得排程原則物件，然後將它儲存在 $SchPol 變數中。</span><span class="sxs-lookup"><span data-stu-id="627b1-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="627b1-114">最後一個命令會使用保留原則和使用先前命令建立的排程原則，建立備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="627b1-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="627b1-115">參數</span><span class="sxs-lookup"><span data-stu-id="627b1-115">PARAMETERS</span></span>

### <span data-ttu-id="627b1-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="627b1-116">-BackupManagementType</span></span>
<span data-ttu-id="627b1-117">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="627b1-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="627b1-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="627b1-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="627b1-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="627b1-119">AzureVM</span></span> 
- <span data-ttu-id="627b1-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="627b1-120">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627b1-121">-DefaultProfile</span></span>
<span data-ttu-id="627b1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="627b1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b1-123">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="627b1-123">-WorkloadType</span></span>
<span data-ttu-id="627b1-124">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="627b1-124">Specifies the workload type.</span></span>
<span data-ttu-id="627b1-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="627b1-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="627b1-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="627b1-126">AzureVM</span></span> 
- <span data-ttu-id="627b1-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="627b1-127">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627b1-128">CommonParameters</span></span>
<span data-ttu-id="627b1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="627b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627b1-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="627b1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627b1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="627b1-131">INPUTS</span></span>

### <span data-ttu-id="627b1-132">所有</span><span class="sxs-lookup"><span data-stu-id="627b1-132">None</span></span>
<span data-ttu-id="627b1-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="627b1-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="627b1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="627b1-134">OUTPUTS</span></span>

### <span data-ttu-id="627b1-135">RetentionPolicyBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="627b1-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="627b1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="627b1-136">NOTES</span></span>

## <span data-ttu-id="627b1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="627b1-137">RELATED LINKS</span></span>

[<span data-ttu-id="627b1-138">AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="627b1-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="627b1-139">新-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="627b1-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


