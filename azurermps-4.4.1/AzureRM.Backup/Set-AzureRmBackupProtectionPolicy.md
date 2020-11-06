---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 70e6cf359f81911d8dff2e96944e93c388cfc80e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450034"
---
# <span data-ttu-id="8373d-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8373d-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="8373d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8373d-102">SYNOPSIS</span></span>
<span data-ttu-id="8373d-103">修改現有的保護原則。</span><span class="sxs-lookup"><span data-stu-id="8373d-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8373d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8373d-104">SYNTAX</span></span>

### <span data-ttu-id="8373d-105">NoScheduleParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8373d-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8373d-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="8373d-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8373d-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="8373d-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8373d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8373d-108">DESCRIPTION</span></span>
<span data-ttu-id="8373d-109">**AzureRmBackupProtectionPolicy** Cmdlet 會修改 Azure 備份中的現有保護原則。</span><span class="sxs-lookup"><span data-stu-id="8373d-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="8373d-110">您可以修改下列保護原則元件：</span><span class="sxs-lookup"><span data-stu-id="8373d-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="8373d-111">列名</span><span class="sxs-lookup"><span data-stu-id="8373d-111">Name</span></span>
- <span data-ttu-id="8373d-112">備份排程</span><span class="sxs-lookup"><span data-stu-id="8373d-112">Backup schedule</span></span>
- <span data-ttu-id="8373d-113">保留原則</span><span class="sxs-lookup"><span data-stu-id="8373d-113">Retention policies</span></span>

<span data-ttu-id="8373d-114">任何變更都可能會影響與原則相關的專案的備份與保留。</span><span class="sxs-lookup"><span data-stu-id="8373d-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="8373d-115">示例</span><span class="sxs-lookup"><span data-stu-id="8373d-115">EXAMPLES</span></span>

## <span data-ttu-id="8373d-116">參數</span><span class="sxs-lookup"><span data-stu-id="8373d-116">PARAMETERS</span></span>

### <span data-ttu-id="8373d-117">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="8373d-117">-BackupTime</span></span>
<span data-ttu-id="8373d-118">為原則指定一天的新備份時間（作為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="8373d-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="8373d-119">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8373d-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="8373d-120">如需 **DateTime** 物件的相關資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="8373d-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="8373d-121">每日</span><span class="sxs-lookup"><span data-stu-id="8373d-121">-Daily</span></span>
<span data-ttu-id="8373d-122">表示備份作業是在每日排程上執行。</span><span class="sxs-lookup"><span data-stu-id="8373d-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

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

### <span data-ttu-id="8373d-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="8373d-123">-DaysOfWeek</span></span>
<span data-ttu-id="8373d-124">指定一周中的天數陣列。</span><span class="sxs-lookup"><span data-stu-id="8373d-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="8373d-125">此原則會在此參數指定的天數上執行備份。</span><span class="sxs-lookup"><span data-stu-id="8373d-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="8373d-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8373d-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8373d-127">從</span><span class="sxs-lookup"><span data-stu-id="8373d-127">Monday</span></span> 
- <span data-ttu-id="8373d-128">星期二</span><span class="sxs-lookup"><span data-stu-id="8373d-128">Tuesday</span></span> 
- <span data-ttu-id="8373d-129">星期三</span><span class="sxs-lookup"><span data-stu-id="8373d-129">Wednesday</span></span> 
- <span data-ttu-id="8373d-130">星期四</span><span class="sxs-lookup"><span data-stu-id="8373d-130">Thursday</span></span> 
- <span data-ttu-id="8373d-131">日</span><span class="sxs-lookup"><span data-stu-id="8373d-131">Friday</span></span> 
- <span data-ttu-id="8373d-132">星期六</span><span class="sxs-lookup"><span data-stu-id="8373d-132">Saturday</span></span> 
- <span data-ttu-id="8373d-133">日</span><span class="sxs-lookup"><span data-stu-id="8373d-133">Sunday</span></span>

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

### <span data-ttu-id="8373d-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="8373d-134">-NewName</span></span>
<span data-ttu-id="8373d-135">指定原則的新名稱。</span><span class="sxs-lookup"><span data-stu-id="8373d-135">Specifies the new name for the policy.</span></span>
<span data-ttu-id="8373d-136">此名稱在電子倉庫中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8373d-136">This name must be unique in a vault.</span></span>

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

### <span data-ttu-id="8373d-137">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8373d-137">-ProtectionPolicy</span></span>
<span data-ttu-id="8373d-138">指定此 Cmdlet 修改的保護原則。</span><span class="sxs-lookup"><span data-stu-id="8373d-138">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="8373d-139">若要取得 **AzureRmBackupProtectionPolicy** 物件，請使用 Get-AzureRmBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8373d-139">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="8373d-140">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8373d-140">-RetentionPolicy</span></span>
<span data-ttu-id="8373d-141">指定備份原則的保留原則陣列。</span><span class="sxs-lookup"><span data-stu-id="8373d-141">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="8373d-142">若要取得 **AzureRmBackupRetentionPolicy** 物件，請使用 New-AzureRmBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8373d-142">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="8373d-143">-每週</span><span class="sxs-lookup"><span data-stu-id="8373d-143">-Weekly</span></span>
<span data-ttu-id="8373d-144">表示備份作業是在每週排程上執行。</span><span class="sxs-lookup"><span data-stu-id="8373d-144">Indicates that the backup operation runs on a Weekly schedule.</span></span>

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

### <span data-ttu-id="8373d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8373d-145">-DefaultProfile</span></span>
<span data-ttu-id="8373d-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8373d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8373d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8373d-147">CommonParameters</span></span>
<span data-ttu-id="8373d-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8373d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8373d-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8373d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8373d-150">輸入</span><span class="sxs-lookup"><span data-stu-id="8373d-150">INPUTS</span></span>

### <span data-ttu-id="8373d-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8373d-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="8373d-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8373d-152">OUTPUTS</span></span>

### <span data-ttu-id="8373d-153">所有</span><span class="sxs-lookup"><span data-stu-id="8373d-153">None</span></span>

## <span data-ttu-id="8373d-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8373d-154">NOTES</span></span>

## <span data-ttu-id="8373d-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8373d-155">RELATED LINKS</span></span>

[<span data-ttu-id="8373d-156">新-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8373d-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

