---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 803299a64fb98aecc249bc7bb2f505ada74a5573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454912"
---
# <span data-ttu-id="6c325-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c325-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="6c325-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c325-102">SYNOPSIS</span></span>
<span data-ttu-id="6c325-103">建立備份原則。</span><span class="sxs-lookup"><span data-stu-id="6c325-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c325-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c325-104">SYNTAX</span></span>

### <span data-ttu-id="6c325-105">NoScheduleParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c325-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c325-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="6c325-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c325-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="6c325-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c325-108">說明</span><span class="sxs-lookup"><span data-stu-id="6c325-108">DESCRIPTION</span></span>
<span data-ttu-id="6c325-109">**新的-AzureRmBackupProtectionPolicy** Cmdlet 會建立 azure 備份原則做為 azure PowerShell 物件。</span><span class="sxs-lookup"><span data-stu-id="6c325-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="6c325-110">備份原則定義備份專案的時間和頻率。</span><span class="sxs-lookup"><span data-stu-id="6c325-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="6c325-111">Enable-AzureRmBackupProtection Cmdlet 使用備份原則。</span><span class="sxs-lookup"><span data-stu-id="6c325-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="6c325-112">示例</span><span class="sxs-lookup"><span data-stu-id="6c325-112">EXAMPLES</span></span>

### <span data-ttu-id="6c325-113">範例1：建立每日及每月保留的每日備份原則</span><span class="sxs-lookup"><span data-stu-id="6c325-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="6c325-114">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="6c325-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="6c325-115">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c325-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="6c325-116">第二個命令會建立一個保留原則，每日保留30天，然後將它儲存在 $Daily 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c325-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="6c325-117">第三個命令會建立保留原則，每個月的第10個和第二十個是12個月的備份。</span><span class="sxs-lookup"><span data-stu-id="6c325-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="6c325-118">該命令會將保留原則儲存在 $Monthly 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c325-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="6c325-119">最後一個命令會在 $Vault 的每日備份時間為 3:00 PM 的電子倉庫中建立備份原則。</span><span class="sxs-lookup"><span data-stu-id="6c325-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="6c325-120">該命令會指派儲存在 $Daily 和 $Monthly 中的保留原則。</span><span class="sxs-lookup"><span data-stu-id="6c325-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="6c325-121">該命令會將結果儲存在 $ProtectionPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c325-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="6c325-122">參數</span><span class="sxs-lookup"><span data-stu-id="6c325-122">PARAMETERS</span></span>

### <span data-ttu-id="6c325-123">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="6c325-123">-BackupTime</span></span>
<span data-ttu-id="6c325-124">指定當天的時間（作為 **DateTime** 物件），以進行備份操作。</span><span class="sxs-lookup"><span data-stu-id="6c325-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="6c325-125">若要取得 **DateTime** ，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c325-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="6c325-126">如需 **DateTime** 物件的相關資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="6c325-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-127">每日</span><span class="sxs-lookup"><span data-stu-id="6c325-127">-Daily</span></span>
<span data-ttu-id="6c325-128">表示備份作業是在每日排程上執行。</span><span class="sxs-lookup"><span data-stu-id="6c325-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="6c325-129">-DaysOfWeek</span></span>
<span data-ttu-id="6c325-130">指定一周中的天數陣列。</span><span class="sxs-lookup"><span data-stu-id="6c325-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="6c325-131">此原則會在此參數指定的天數上執行備份。</span><span class="sxs-lookup"><span data-stu-id="6c325-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="6c325-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6c325-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c325-133">從</span><span class="sxs-lookup"><span data-stu-id="6c325-133">Monday</span></span> 
- <span data-ttu-id="6c325-134">星期二</span><span class="sxs-lookup"><span data-stu-id="6c325-134">Tuesday</span></span> 
- <span data-ttu-id="6c325-135">星期三</span><span class="sxs-lookup"><span data-stu-id="6c325-135">Wednesday</span></span> 
- <span data-ttu-id="6c325-136">星期四</span><span class="sxs-lookup"><span data-stu-id="6c325-136">Thursday</span></span> 
- <span data-ttu-id="6c325-137">日</span><span class="sxs-lookup"><span data-stu-id="6c325-137">Friday</span></span> 
- <span data-ttu-id="6c325-138">星期六</span><span class="sxs-lookup"><span data-stu-id="6c325-138">Saturday</span></span> 
- <span data-ttu-id="6c325-139">日</span><span class="sxs-lookup"><span data-stu-id="6c325-139">Sunday</span></span>

<span data-ttu-id="6c325-140">如果您指定的是 *每週* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="6c325-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c325-141">-Name</span></span>
<span data-ttu-id="6c325-142">指定備份原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c325-142">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="6c325-143">選取在電子倉庫中唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c325-143">Select a name that is unique in the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-144">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c325-144">-RetentionPolicy</span></span>
<span data-ttu-id="6c325-145">指定備份原則的保留原則陣列。</span><span class="sxs-lookup"><span data-stu-id="6c325-145">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="6c325-146">若要取得 **AzureRmBackupRetentionPolicy** ，請使用 New-AzureRmBackupRetentionPolicyObject Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c325-146">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-147">-類型</span><span class="sxs-lookup"><span data-stu-id="6c325-147">-Type</span></span>
<span data-ttu-id="6c325-148">指定原則所套用的備份專案類型。</span><span class="sxs-lookup"><span data-stu-id="6c325-148">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="6c325-149">目前唯一支援的值為 Add-azurevm。</span><span class="sxs-lookup"><span data-stu-id="6c325-149">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-150">-保存庫</span><span class="sxs-lookup"><span data-stu-id="6c325-150">-Vault</span></span>
<span data-ttu-id="6c325-151">指定備份原則所屬的 Azure 備份電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="6c325-151">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="6c325-152">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c325-152">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-153">-每週</span><span class="sxs-lookup"><span data-stu-id="6c325-153">-Weekly</span></span>
<span data-ttu-id="6c325-154">表示每週一個或多天觸發備份原則。</span><span class="sxs-lookup"><span data-stu-id="6c325-154">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c325-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c325-155">-DefaultProfile</span></span>
<span data-ttu-id="6c325-156">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c325-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c325-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c325-157">CommonParameters</span></span>
<span data-ttu-id="6c325-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c325-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c325-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c325-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c325-160">輸入</span><span class="sxs-lookup"><span data-stu-id="6c325-160">INPUTS</span></span>

### <span data-ttu-id="6c325-161">所有</span><span class="sxs-lookup"><span data-stu-id="6c325-161">None</span></span>

## <span data-ttu-id="6c325-162">輸出</span><span class="sxs-lookup"><span data-stu-id="6c325-162">OUTPUTS</span></span>

### <span data-ttu-id="6c325-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c325-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="6c325-164">筆記</span><span class="sxs-lookup"><span data-stu-id="6c325-164">NOTES</span></span>
* <span data-ttu-id="6c325-165">所有</span><span class="sxs-lookup"><span data-stu-id="6c325-165">None</span></span>

## <span data-ttu-id="6c325-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c325-166">RELATED LINKS</span></span>

[<span data-ttu-id="6c325-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6c325-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="6c325-168">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c325-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="6c325-169">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="6c325-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="6c325-170">新-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6c325-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="6c325-171">移除-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c325-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="6c325-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c325-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


