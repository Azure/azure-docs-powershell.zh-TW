---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967645"
---
# <span data-ttu-id="dd332-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="dd332-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="dd332-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd332-102">SYNOPSIS</span></span>
<span data-ttu-id="dd332-103">建立 SQL Server 自動備份的設定物件。</span><span class="sxs-lookup"><span data-stu-id="dd332-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="dd332-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd332-104">SYNTAX</span></span>

### <span data-ttu-id="dd332-105">StorageUriSqlServerAutoBackup (預設) </span><span class="sxs-lookup"><span data-stu-id="dd332-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd332-106">StorageCoNtextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="dd332-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dd332-107">說明</span><span class="sxs-lookup"><span data-stu-id="dd332-107">DESCRIPTION</span></span>
<span data-ttu-id="dd332-108">**新的-AzureVMSqlServerAutoBackupConfig** Cmdlet 會建立 SQL Server 自動備份的設定物件。</span><span class="sxs-lookup"><span data-stu-id="dd332-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="dd332-109">示例</span><span class="sxs-lookup"><span data-stu-id="dd332-109">EXAMPLES</span></span>

### <span data-ttu-id="dd332-110">範例1：使用儲存空間 URI 和帳戶金鑰建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="dd332-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="dd332-111">這個命令會透過指定 [儲存 URL] 和 [帳戶金鑰] 來建立自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="dd332-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="dd332-112">範例2：使用儲存內容建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="dd332-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="dd332-113">這個命令會透過指定儲存內容來建立自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="dd332-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="dd332-114">範例3：使用含加密及密碼的儲存空間內容建立自動備份設定</span><span class="sxs-lookup"><span data-stu-id="dd332-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="dd332-115">這個命令會透過指定儲存內容及啟用密碼的加密選項，來建立自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="dd332-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="dd332-116">Certificatepassword ist 儲存在名為 $CertPasswd 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dd332-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="dd332-117">參數</span><span class="sxs-lookup"><span data-stu-id="dd332-117">PARAMETERS</span></span>

### <span data-ttu-id="dd332-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="dd332-118">-BackupScheduleType</span></span>
<span data-ttu-id="dd332-119">備份排程類型、手動或自動</span><span class="sxs-lookup"><span data-stu-id="dd332-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="dd332-120">-BackupSystemDbs</span></span>
<span data-ttu-id="dd332-121">備份系統資料庫</span><span class="sxs-lookup"><span data-stu-id="dd332-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dd332-122">-CertificatePassword</span></span>
<span data-ttu-id="dd332-123">指定密碼來加密用來執行 SQL Server 加密備份的憑證。</span><span class="sxs-lookup"><span data-stu-id="dd332-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-124">-啟用</span><span class="sxs-lookup"><span data-stu-id="dd332-124">-Enable</span></span>
<span data-ttu-id="dd332-125">表示已啟用 SQL Server 虛擬機器的自動備份。</span><span class="sxs-lookup"><span data-stu-id="dd332-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="dd332-126">如果您使用這個參數，[自動備份] 會為所有目前的資料庫和新資料庫設定備份排程。</span><span class="sxs-lookup"><span data-stu-id="dd332-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="dd332-127">這會更新您受管理的備份設定，以遵循此排程。</span><span class="sxs-lookup"><span data-stu-id="dd332-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="dd332-128">-EnableEncryption</span></span>
<span data-ttu-id="dd332-129">表示已啟用加密。</span><span class="sxs-lookup"><span data-stu-id="dd332-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="dd332-130">-FullBackupFrequency</span></span>
<span data-ttu-id="dd332-131">Sql Server 完整備份頻率、每天或每週</span><span class="sxs-lookup"><span data-stu-id="dd332-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="dd332-132">-FullBackupStartHour</span></span>
<span data-ttu-id="dd332-133">當 Sql Server 完整備份啟動時， (0-23) 一天的小時</span><span class="sxs-lookup"><span data-stu-id="dd332-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="dd332-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="dd332-135">Sql Server 完整備份視窗的時間（小時）</span><span class="sxs-lookup"><span data-stu-id="dd332-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dd332-136">-InformationAction</span></span>
<span data-ttu-id="dd332-137">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="dd332-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dd332-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="dd332-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dd332-139">持續</span><span class="sxs-lookup"><span data-stu-id="dd332-139">Continue</span></span>
- <span data-ttu-id="dd332-140">理會</span><span class="sxs-lookup"><span data-stu-id="dd332-140">Ignore</span></span>
- <span data-ttu-id="dd332-141">看</span><span class="sxs-lookup"><span data-stu-id="dd332-141">Inquire</span></span>
- <span data-ttu-id="dd332-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dd332-142">SilentlyContinue</span></span>
- <span data-ttu-id="dd332-143">停止</span><span class="sxs-lookup"><span data-stu-id="dd332-143">Stop</span></span>
- <span data-ttu-id="dd332-144">封存</span><span class="sxs-lookup"><span data-stu-id="dd332-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dd332-145">-InformationVariable</span></span>
<span data-ttu-id="dd332-146">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="dd332-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd332-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="dd332-148">Sql Server 記錄備份頻率，每隔1-60 分鐘一次</span><span class="sxs-lookup"><span data-stu-id="dd332-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-149">-設定檔</span><span class="sxs-lookup"><span data-stu-id="dd332-149">-Profile</span></span>
<span data-ttu-id="dd332-150">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="dd332-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd332-151">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="dd332-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="dd332-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="dd332-153">指定保留期間的長度（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="dd332-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-154">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="dd332-154">-StorageContext</span></span>
<span data-ttu-id="dd332-155">指定要用來儲存備份的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="dd332-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="dd332-156">[預設值] 是與 SQL Server 虛擬機器相關聯的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="dd332-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="dd332-157">-StorageKey</span></span>
<span data-ttu-id="dd332-158">指定 [blob 儲存空間] 帳戶的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="dd332-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="dd332-159">-StorageUri</span></span>
<span data-ttu-id="dd332-160">指定 blob 儲存空間帳戶的 URI。</span><span class="sxs-lookup"><span data-stu-id="dd332-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd332-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd332-161">CommonParameters</span></span>
<span data-ttu-id="dd332-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd332-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd332-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd332-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd332-164">輸入</span><span class="sxs-lookup"><span data-stu-id="dd332-164">INPUTS</span></span>

## <span data-ttu-id="dd332-165">輸出</span><span class="sxs-lookup"><span data-stu-id="dd332-165">OUTPUTS</span></span>

## <span data-ttu-id="dd332-166">筆記</span><span class="sxs-lookup"><span data-stu-id="dd332-166">NOTES</span></span>

## <span data-ttu-id="dd332-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd332-167">RELATED LINKS</span></span>

[<span data-ttu-id="dd332-168">新-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="dd332-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


