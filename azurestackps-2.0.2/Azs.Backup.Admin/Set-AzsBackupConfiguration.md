---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968484"
---
# <span data-ttu-id="52ab1-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="52ab1-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="52ab1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="52ab1-103">更新備份位置。</span><span class="sxs-lookup"><span data-stu-id="52ab1-103">Update a backup location.</span></span>

## <span data-ttu-id="52ab1-104">句法</span><span class="sxs-lookup"><span data-stu-id="52ab1-104">SYNTAX</span></span>

### <span data-ttu-id="52ab1-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="52ab1-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="52ab1-106">時更新</span><span class="sxs-lookup"><span data-stu-id="52ab1-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="52ab1-107">說明</span><span class="sxs-lookup"><span data-stu-id="52ab1-107">DESCRIPTION</span></span>
<span data-ttu-id="52ab1-108">更新備份位置。</span><span class="sxs-lookup"><span data-stu-id="52ab1-108">Update a backup location.</span></span>

## <span data-ttu-id="52ab1-109">示例</span><span class="sxs-lookup"><span data-stu-id="52ab1-109">EXAMPLES</span></span>

### <span data-ttu-id="52ab1-110">範例1：設定備份配置</span><span class="sxs-lookup"><span data-stu-id="52ab1-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="52ab1-111">設定 Azure 堆疊備份配置。</span><span class="sxs-lookup"><span data-stu-id="52ab1-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="52ab1-112">參數</span><span class="sxs-lookup"><span data-stu-id="52ab1-112">PARAMETERS</span></span>

### <span data-ttu-id="52ab1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52ab1-113">-AsJob</span></span>
<span data-ttu-id="52ab1-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="52ab1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="52ab1-115">-備份</span><span class="sxs-lookup"><span data-stu-id="52ab1-115">-Backup</span></span>
<span data-ttu-id="52ab1-116">備份位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="52ab1-116">Information about the backup location.</span></span>
<span data-ttu-id="52ab1-117">若要建立，請參閱備份屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="52ab1-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="52ab1-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="52ab1-119">排程程式執行備份之頻率的間隔（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="52ab1-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="52ab1-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="52ab1-121">在儲存位置中備份的保留期間（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="52ab1-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ab1-122">-DefaultProfile</span></span>
<span data-ttu-id="52ab1-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52ab1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="52ab1-124">-EncryptionCertPath</span></span>
<span data-ttu-id="52ab1-125">包含公開金鑰 ( .cer) 的加密憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="52ab1-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="52ab1-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="52ab1-127">如果已啟用備份排程程式，則為 True。</span><span class="sxs-lookup"><span data-stu-id="52ab1-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-128">-位置</span><span class="sxs-lookup"><span data-stu-id="52ab1-128">-Location</span></span>
<span data-ttu-id="52ab1-129">備份位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="52ab1-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="52ab1-130">-NoWait</span></span>
<span data-ttu-id="52ab1-131">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="52ab1-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52ab1-132">-Password</span><span class="sxs-lookup"><span data-stu-id="52ab1-132">-Password</span></span>
<span data-ttu-id="52ab1-133">存取位置的密碼。</span><span class="sxs-lookup"><span data-stu-id="52ab1-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-134">-Path</span><span class="sxs-lookup"><span data-stu-id="52ab1-134">-Path</span></span>
<span data-ttu-id="52ab1-135">更新位置的路徑</span><span class="sxs-lookup"><span data-stu-id="52ab1-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ab1-136">-ResourceGroupName</span></span>
<span data-ttu-id="52ab1-137">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52ab1-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52ab1-138">-SubscriptionId</span></span>
<span data-ttu-id="52ab1-139">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="52ab1-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="52ab1-140">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="52ab1-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="52ab1-141">-Tag</span></span>
<span data-ttu-id="52ab1-142">鍵值對清單。</span><span class="sxs-lookup"><span data-stu-id="52ab1-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="52ab1-143">-UserName</span></span>
<span data-ttu-id="52ab1-144">存取位置的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="52ab1-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="52ab1-145">-確認</span><span class="sxs-lookup"><span data-stu-id="52ab1-145">-Confirm</span></span>
<span data-ttu-id="52ab1-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52ab1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ab1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ab1-147">-WhatIf</span></span>
<span data-ttu-id="52ab1-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52ab1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ab1-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52ab1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ab1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ab1-150">CommonParameters</span></span>
<span data-ttu-id="52ab1-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52ab1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ab1-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="52ab1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ab1-153">輸入</span><span class="sxs-lookup"><span data-stu-id="52ab1-153">INPUTS</span></span>

### <span data-ttu-id="52ab1-154">IBackupLocation （BackupAdmin）。 Api20180901。</span><span class="sxs-lookup"><span data-stu-id="52ab1-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="52ab1-155">輸出</span><span class="sxs-lookup"><span data-stu-id="52ab1-155">OUTPUTS</span></span>

### <span data-ttu-id="52ab1-156">IBackupLocation （BackupAdmin）。 Api20180901。</span><span class="sxs-lookup"><span data-stu-id="52ab1-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="52ab1-157">筆記</span><span class="sxs-lookup"><span data-stu-id="52ab1-157">NOTES</span></span>

<span data-ttu-id="52ab1-158">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="52ab1-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52ab1-159">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="52ab1-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="52ab1-160">備份 <IBackupLocation> ：備份位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="52ab1-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="52ab1-161">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="52ab1-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="52ab1-162">`[Tag <IResourceTags>]`： [鍵值] 對的清單。</span><span class="sxs-lookup"><span data-stu-id="52ab1-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="52ab1-163">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="52ab1-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="52ab1-164">`[BackupFrequencyInHours <Int32?>]`：排程程式執行備份之頻率的間隔（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="52ab1-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="52ab1-165">`[BackupRetentionPeriodInDays <Int32?>]`：在儲存位置中備份的保留期間（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="52ab1-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="52ab1-166">`[EncryptionCertBase64 <String>]`：備份加密憑證的 base64 原始資料。</span><span class="sxs-lookup"><span data-stu-id="52ab1-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="52ab1-167">`[IsBackupSchedulerEnabled <Boolean?>]`：如果已啟用備份排程程式，則為 True。</span><span class="sxs-lookup"><span data-stu-id="52ab1-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="52ab1-168">`[Password <String>]`：存取位置的密碼。</span><span class="sxs-lookup"><span data-stu-id="52ab1-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="52ab1-169">`[Path <String>]`：更新位置的路徑</span><span class="sxs-lookup"><span data-stu-id="52ab1-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="52ab1-170">`[UserName <String>]`：用於存取位置的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="52ab1-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="52ab1-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="52ab1-171">RELATED LINKS</span></span>

