---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907902"
---
# <span data-ttu-id="c191c-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="c191c-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="c191c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c191c-102">SYNOPSIS</span></span>
<span data-ttu-id="c191c-103">建立 SQL Server 自動備份的群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="c191c-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c191c-104">語法</span><span class="sxs-lookup"><span data-stu-id="c191c-104">SYNTAX</span></span>

### <span data-ttu-id="c191c-105">StorageUriSqlServerAutoBackup (預設) </span><span class="sxs-lookup"><span data-stu-id="c191c-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c191c-106">StorageCoNtextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="c191c-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c191c-107">描述</span><span class="sxs-lookup"><span data-stu-id="c191c-107">DESCRIPTION</span></span>
<span data-ttu-id="c191c-108">**New-AzCMSqlServerAutoBackupConfig** Cmdlet 會建立 SQL Server 自動備份的群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="c191c-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c191c-109">例子</span><span class="sxs-lookup"><span data-stu-id="c191c-109">EXAMPLES</span></span>

### <span data-ttu-id="c191c-110">範例 1：使用儲存空間 URI 和帳戶金鑰建立自動備份組</span><span class="sxs-lookup"><span data-stu-id="c191c-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c191c-111">此命令會指定儲存空間 URI 和帳戶金鑰，以建立自動備份組組物件。</span><span class="sxs-lookup"><span data-stu-id="c191c-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="c191c-112">已啟用自動備份，且自動備份會保留 10 天。</span><span class="sxs-lookup"><span data-stu-id="c191c-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="c191c-113">該命令會將結果儲存在$AutoBackupConfig變數中。</span><span class="sxs-lookup"><span data-stu-id="c191c-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="c191c-114">您可以為其他 Cmdlet 指定此組Set-AzVMSqlServerExtension專案。</span><span class="sxs-lookup"><span data-stu-id="c191c-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="c191c-115">範例 2：使用儲存內容建立自動備份組式</span><span class="sxs-lookup"><span data-stu-id="c191c-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c191c-116">第一個命令會建立儲存內容，然後將它儲存在$StorageCoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="c191c-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="c191c-117">詳細資訊請參閱 New-AzStorageCoNtext。</span><span class="sxs-lookup"><span data-stu-id="c191c-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="c191c-118">第二個命令會指定自動備份組$StorageCoNtext。</span><span class="sxs-lookup"><span data-stu-id="c191c-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="c191c-119">已啟用自動備份，且自動備份會保留 10 天。</span><span class="sxs-lookup"><span data-stu-id="c191c-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="c191c-120">範例 3：使用儲存內容建立具有加密和密碼的自動備份組式</span><span class="sxs-lookup"><span data-stu-id="c191c-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="c191c-121">此命令會建立並儲存自動備份群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="c191c-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="c191c-122">命令會指定在上一個範例中建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="c191c-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="c191c-123">此命令會啟用密碼加密。</span><span class="sxs-lookup"><span data-stu-id="c191c-123">The command enables encryption with password.</span></span>
<span data-ttu-id="c191c-124">密碼先前儲存為數據變數中的安全$CertificatePassword字串。</span><span class="sxs-lookup"><span data-stu-id="c191c-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="c191c-125">若要建立安全字串，請使用 ConvertTo-SecureString Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c191c-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="c191c-126">參數</span><span class="sxs-lookup"><span data-stu-id="c191c-126">PARAMETERS</span></span>

### <span data-ttu-id="c191c-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="c191c-127">-BackupScheduleType</span></span>
<span data-ttu-id="c191c-128">備份排程類型、手動或自動化</span><span class="sxs-lookup"><span data-stu-id="c191c-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="c191c-129">-BackupSystemDbs</span></span>
<span data-ttu-id="c191c-130">備份系統資料庫</span><span class="sxs-lookup"><span data-stu-id="c191c-130">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c191c-131">-CertificatePassword</span></span>
<span data-ttu-id="c191c-132">指定密碼以加密用來執行 SQL Server 加密備份的憑證。</span><span class="sxs-lookup"><span data-stu-id="c191c-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c191c-133">-DefaultProfile</span></span>
<span data-ttu-id="c191c-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c191c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c191c-135">-啟用</span><span class="sxs-lookup"><span data-stu-id="c191c-135">-Enable</span></span>
<span data-ttu-id="c191c-136">表示已啟用 SQL Server 虛擬機器的自動備份。</span><span class="sxs-lookup"><span data-stu-id="c191c-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="c191c-137">如果您指定此參數，自動化備份會針對所有目前和新資料庫設定備份排程。</span><span class="sxs-lookup"><span data-stu-id="c191c-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="c191c-138">這會更新您的受管理的備份設定，以遵循此排程。</span><span class="sxs-lookup"><span data-stu-id="c191c-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="c191c-139">-EnableEncryption</span></span>
<span data-ttu-id="c191c-140">表示此 Cmdlet 啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c191c-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="c191c-141">-FullBackupFrequency</span></span>
<span data-ttu-id="c191c-142">每天或每週的 Sql Server 完整備份頻率</span><span class="sxs-lookup"><span data-stu-id="c191c-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="c191c-143">-FullBackupStartHour</span></span>
<span data-ttu-id="c191c-144">當 Sql Server 完整備份 (0-23) 小時</span><span class="sxs-lookup"><span data-stu-id="c191c-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="c191c-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="c191c-146">Sql Server 完整備份視窗 ，以小時表示</span><span class="sxs-lookup"><span data-stu-id="c191c-146">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="c191c-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="c191c-148">Sql Server 記錄備份頻率，每 1-60 分鐘一次</span><span class="sxs-lookup"><span data-stu-id="c191c-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c191c-149">-ResourceGroupName</span></span>
<span data-ttu-id="c191c-150">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c191c-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c191c-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="c191c-152">指定要保留備份的天數。</span><span class="sxs-lookup"><span data-stu-id="c191c-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-153">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c191c-153">-StorageContext</span></span>
<span data-ttu-id="c191c-154">指定要用來儲存備份的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c191c-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="c191c-155">若要取得 **AzureStorageCoNtext 物件** ，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c191c-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="c191c-156">預設值為與 SQL Server 虛擬機器相關聯的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c191c-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="c191c-157">-StorageKey</span></span>
<span data-ttu-id="c191c-158">指定 Blob 儲存帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="c191c-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="c191c-159">-StorageUri</span></span>
<span data-ttu-id="c191c-160">指定 Blob 儲存帳戶 (URI) 統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="c191c-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c191c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c191c-161">CommonParameters</span></span>
<span data-ttu-id="c191c-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c191c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c191c-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c191c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c191c-164">輸入</span><span class="sxs-lookup"><span data-stu-id="c191c-164">INPUTS</span></span>

### <span data-ttu-id="c191c-165">System.String</span><span class="sxs-lookup"><span data-stu-id="c191c-165">System.String</span></span>

### <span data-ttu-id="c191c-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c191c-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c191c-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c191c-167">System.Int32</span></span>

### <span data-ttu-id="c191c-168">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c191c-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="c191c-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="c191c-169">System.Uri</span></span>

### <span data-ttu-id="c191c-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="c191c-170">System.Security.SecureString</span></span>

### <span data-ttu-id="c191c-171">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c191c-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c191c-172">輸出</span><span class="sxs-lookup"><span data-stu-id="c191c-172">OUTPUTS</span></span>

### <span data-ttu-id="c191c-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="c191c-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="c191c-174">筆記</span><span class="sxs-lookup"><span data-stu-id="c191c-174">NOTES</span></span>

## <span data-ttu-id="c191c-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="c191c-175">RELATED LINKS</span></span>

[<span data-ttu-id="c191c-176">New-AzMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="c191c-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="c191c-177">Set-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c191c-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


