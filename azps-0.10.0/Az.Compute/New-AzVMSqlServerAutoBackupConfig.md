---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 1ff53a29fa26ebe7ac78cac5140a9105b43bb27d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796117"
---
# <span data-ttu-id="dc65b-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="dc65b-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="dc65b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc65b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc65b-103">建立 SQL Server 自動備份的設定物件。</span><span class="sxs-lookup"><span data-stu-id="dc65b-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="dc65b-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc65b-104">SYNTAX</span></span>

### <span data-ttu-id="dc65b-105">StorageUriSqlServerAutoBackup (預設) </span><span class="sxs-lookup"><span data-stu-id="dc65b-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc65b-106">StorageCoNtextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="dc65b-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc65b-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc65b-107">DESCRIPTION</span></span>
<span data-ttu-id="dc65b-108">**新的-AzVMSqlServerAutoBackupConfig** Cmdlet 會建立 SQL Server 自動備份的設定物件。</span><span class="sxs-lookup"><span data-stu-id="dc65b-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="dc65b-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc65b-109">EXAMPLES</span></span>

### <span data-ttu-id="dc65b-110">範例1：使用儲存空間 URI 和帳戶金鑰建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="dc65b-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="dc65b-111">這個命令會透過指定儲存 URI 和帳戶金鑰來建立自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="dc65b-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="dc65b-112">自動備份已啟用，自動備份會保留10天。</span><span class="sxs-lookup"><span data-stu-id="dc65b-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="dc65b-113">該命令會將結果儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="dc65b-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="dc65b-114">您可以為其他 Cmdlet 指定此設定專案，例如 Set-AzVMSqlServerExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc65b-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="dc65b-115">範例2：使用儲存內容建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="dc65b-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="dc65b-116">第一個命令會建立儲存內容，然後將它儲存在 $StorageCoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="dc65b-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="dc65b-117">如需詳細資訊，請參閱新 AzureStorageCoNtext。</span><span class="sxs-lookup"><span data-stu-id="dc65b-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="dc65b-118">第二個命令會透過指定 $StorageCoNtext 中的儲存內容來建立自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="dc65b-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="dc65b-119">自動備份已啟用，自動備份會保留10天。</span><span class="sxs-lookup"><span data-stu-id="dc65b-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="dc65b-120">範例3：使用含加密及密碼的儲存空間內容建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="dc65b-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="dc65b-121">這個命令會建立並儲存自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="dc65b-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="dc65b-122">此命令會指定在前一個範例中建立的儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dc65b-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="dc65b-123">使用密碼加密的命令。</span><span class="sxs-lookup"><span data-stu-id="dc65b-123">The command enables encryption with password.</span></span>
<span data-ttu-id="dc65b-124">密碼先前已以安全字串形式儲存在 $CertificatePassword 變數中。</span><span class="sxs-lookup"><span data-stu-id="dc65b-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="dc65b-125">若要建立安全的字串，請使用 ConvertTo-SecureString Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc65b-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="dc65b-126">參數</span><span class="sxs-lookup"><span data-stu-id="dc65b-126">PARAMETERS</span></span>

### <span data-ttu-id="dc65b-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="dc65b-127">-BackupScheduleType</span></span>
<span data-ttu-id="dc65b-128">備份排程類型、手動或自動</span><span class="sxs-lookup"><span data-stu-id="dc65b-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="dc65b-129">-BackupSystemDbs</span></span>
<span data-ttu-id="dc65b-130">備份系統資料庫</span><span class="sxs-lookup"><span data-stu-id="dc65b-130">Backup system databases</span></span>

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

### <span data-ttu-id="dc65b-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dc65b-131">-CertificatePassword</span></span>
<span data-ttu-id="dc65b-132">指定密碼來加密用來執行 SQL Server 加密備份的憑證。</span><span class="sxs-lookup"><span data-stu-id="dc65b-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc65b-133">-DefaultProfile</span></span>
<span data-ttu-id="dc65b-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc65b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc65b-135">-啟用</span><span class="sxs-lookup"><span data-stu-id="dc65b-135">-Enable</span></span>
<span data-ttu-id="dc65b-136">表示已啟用 SQL Server 虛擬機器的自動備份。</span><span class="sxs-lookup"><span data-stu-id="dc65b-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="dc65b-137">如果您指定此參數，[自動備份] 會為所有目前的資料庫和新資料庫設定備份排程。</span><span class="sxs-lookup"><span data-stu-id="dc65b-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="dc65b-138">這會更新您受管理的備份設定，以遵循此排程。</span><span class="sxs-lookup"><span data-stu-id="dc65b-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="dc65b-139">-EnableEncryption</span></span>
<span data-ttu-id="dc65b-140">表示此 Cmdlet 啟用加密。</span><span class="sxs-lookup"><span data-stu-id="dc65b-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="dc65b-141">-FullBackupFrequency</span></span>
<span data-ttu-id="dc65b-142">Sql Server 完整備份頻率，每日或每週</span><span class="sxs-lookup"><span data-stu-id="dc65b-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="dc65b-143">-FullBackupStartHour</span></span>
<span data-ttu-id="dc65b-144">當 Sql Server 完整備份啟動時， (0-23) 一天的小時</span><span class="sxs-lookup"><span data-stu-id="dc65b-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="dc65b-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="dc65b-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="dc65b-146">Sql Server 完整備份視窗的時間（小時）</span><span class="sxs-lookup"><span data-stu-id="dc65b-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="dc65b-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="dc65b-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="dc65b-148">Sql Server 記錄備份頻率，每隔1-60 分鐘一次</span><span class="sxs-lookup"><span data-stu-id="dc65b-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="dc65b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc65b-149">-ResourceGroupName</span></span>
<span data-ttu-id="dc65b-150">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc65b-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="dc65b-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="dc65b-152">指定保留備份的天數。</span><span class="sxs-lookup"><span data-stu-id="dc65b-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-153">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="dc65b-153">-StorageContext</span></span>
<span data-ttu-id="dc65b-154">指定將用來儲存備份的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc65b-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="dc65b-155">若要取得 **AzureStorageCoNtext** 物件，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc65b-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="dc65b-156">預設值是與 SQL Server 虛擬機器相關聯的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc65b-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc65b-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="dc65b-157">-StorageKey</span></span>
<span data-ttu-id="dc65b-158">指定 [blob 儲存空間] 帳戶的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="dc65b-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="dc65b-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="dc65b-159">-StorageUri</span></span>
<span data-ttu-id="dc65b-160">指定 blob 儲存空間帳戶 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="dc65b-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="dc65b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc65b-161">CommonParameters</span></span>
<span data-ttu-id="dc65b-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc65b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc65b-163">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc65b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc65b-164">輸入</span><span class="sxs-lookup"><span data-stu-id="dc65b-164">INPUTS</span></span>

### <span data-ttu-id="dc65b-165">所有</span><span class="sxs-lookup"><span data-stu-id="dc65b-165">None</span></span>
<span data-ttu-id="dc65b-166">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="dc65b-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc65b-167">輸出</span><span class="sxs-lookup"><span data-stu-id="dc65b-167">OUTPUTS</span></span>

### <span data-ttu-id="dc65b-168">AutoBackupSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="dc65b-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="dc65b-169">筆記</span><span class="sxs-lookup"><span data-stu-id="dc65b-169">NOTES</span></span>

## <span data-ttu-id="dc65b-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc65b-170">RELATED LINKS</span></span>

[<span data-ttu-id="dc65b-171">新-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="dc65b-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="dc65b-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="dc65b-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


