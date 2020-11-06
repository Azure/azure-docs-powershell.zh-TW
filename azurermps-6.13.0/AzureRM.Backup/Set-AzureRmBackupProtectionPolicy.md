---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447479"
---
# <span data-ttu-id="c1f59-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1f59-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="c1f59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1f59-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f59-103">修改現有的保護原則。</span><span class="sxs-lookup"><span data-stu-id="c1f59-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1f59-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1f59-104">SYNTAX</span></span>

### <span data-ttu-id="c1f59-105">NoScheduleParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c1f59-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1f59-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="c1f59-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1f59-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="c1f59-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1f59-108">說明</span><span class="sxs-lookup"><span data-stu-id="c1f59-108">DESCRIPTION</span></span>
<span data-ttu-id="c1f59-109">**AzureRmBackupProtectionPolicy** Cmdlet 會修改 Azure 備份中的現有保護原則。</span><span class="sxs-lookup"><span data-stu-id="c1f59-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="c1f59-110">您可以修改下列保護原則元件：</span><span class="sxs-lookup"><span data-stu-id="c1f59-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="c1f59-111">列名</span><span class="sxs-lookup"><span data-stu-id="c1f59-111">Name</span></span>
- <span data-ttu-id="c1f59-112">備份排程</span><span class="sxs-lookup"><span data-stu-id="c1f59-112">Backup schedule</span></span>
- <span data-ttu-id="c1f59-113">保留原則任何變更都可能會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="c1f59-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="c1f59-114">示例</span><span class="sxs-lookup"><span data-stu-id="c1f59-114">EXAMPLES</span></span>

## <span data-ttu-id="c1f59-115">參數</span><span class="sxs-lookup"><span data-stu-id="c1f59-115">PARAMETERS</span></span>

### <span data-ttu-id="c1f59-116">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="c1f59-116">-BackupTime</span></span>
<span data-ttu-id="c1f59-117">為原則指定一天的新備份時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="c1f59-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="c1f59-118">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1f59-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="c1f59-119">如需 **DateTime** 物件的相關資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="c1f59-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f59-120">每日</span><span class="sxs-lookup"><span data-stu-id="c1f59-120">-Daily</span></span>
<span data-ttu-id="c1f59-121">表示備份作業是在每日排程上執行。</span><span class="sxs-lookup"><span data-stu-id="c1f59-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f59-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="c1f59-122">-DaysOfWeek</span></span>
<span data-ttu-id="c1f59-123">指定一周中的天數陣列。</span><span class="sxs-lookup"><span data-stu-id="c1f59-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="c1f59-124">此原則會在此參數指定的天數上執行備份。</span><span class="sxs-lookup"><span data-stu-id="c1f59-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="c1f59-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c1f59-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c1f59-126">從</span><span class="sxs-lookup"><span data-stu-id="c1f59-126">Monday</span></span> 
- <span data-ttu-id="c1f59-127">星期二</span><span class="sxs-lookup"><span data-stu-id="c1f59-127">Tuesday</span></span> 
- <span data-ttu-id="c1f59-128">星期三</span><span class="sxs-lookup"><span data-stu-id="c1f59-128">Wednesday</span></span> 
- <span data-ttu-id="c1f59-129">星期四</span><span class="sxs-lookup"><span data-stu-id="c1f59-129">Thursday</span></span> 
- <span data-ttu-id="c1f59-130">日</span><span class="sxs-lookup"><span data-stu-id="c1f59-130">Friday</span></span> 
- <span data-ttu-id="c1f59-131">星期六</span><span class="sxs-lookup"><span data-stu-id="c1f59-131">Saturday</span></span> 
- <span data-ttu-id="c1f59-132">日</span><span class="sxs-lookup"><span data-stu-id="c1f59-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f59-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f59-133">-DefaultProfile</span></span>
<span data-ttu-id="c1f59-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c1f59-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1f59-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="c1f59-135">-NewName</span></span>
<span data-ttu-id="c1f59-136">指定原則的新名稱。</span><span class="sxs-lookup"><span data-stu-id="c1f59-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="c1f59-137">此名稱在電子倉庫中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c1f59-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f59-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1f59-138">-ProtectionPolicy</span></span>
<span data-ttu-id="c1f59-139">指定此 Cmdlet 修改的保護原則。</span><span class="sxs-lookup"><span data-stu-id="c1f59-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="c1f59-140">若要取得 **AzureRmBackupProtectionPolicy** 物件，請使用 Get-AzureRmBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1f59-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f59-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1f59-141">-RetentionPolicy</span></span>
<span data-ttu-id="c1f59-142">指定備份原則的保留原則陣列。</span><span class="sxs-lookup"><span data-stu-id="c1f59-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="c1f59-143">若要取得 **AzureRmBackupRetentionPolicy** 物件，請使用 New-AzureRmBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1f59-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f59-144">-每週</span><span class="sxs-lookup"><span data-stu-id="c1f59-144">-Weekly</span></span>
<span data-ttu-id="c1f59-145">表示備份作業是在每週排程上執行。</span><span class="sxs-lookup"><span data-stu-id="c1f59-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f59-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f59-146">CommonParameters</span></span>
<span data-ttu-id="c1f59-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1f59-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f59-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1f59-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f59-149">輸入</span><span class="sxs-lookup"><span data-stu-id="c1f59-149">INPUTS</span></span>

### <span data-ttu-id="c1f59-150">AzureRMBackupProtectionPolicy 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="c1f59-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="c1f59-151">參數： ProtectionPolicy (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c1f59-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="c1f59-152">輸出</span><span class="sxs-lookup"><span data-stu-id="c1f59-152">OUTPUTS</span></span>

### <span data-ttu-id="c1f59-153">AzureRMBackupJob 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="c1f59-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="c1f59-154">筆記</span><span class="sxs-lookup"><span data-stu-id="c1f59-154">NOTES</span></span>

## <span data-ttu-id="c1f59-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1f59-155">RELATED LINKS</span></span>

[<span data-ttu-id="c1f59-156">新-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1f59-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


