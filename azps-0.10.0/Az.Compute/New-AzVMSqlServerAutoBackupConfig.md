---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: ecff02643dd6d0e017d56af01792a06dc7b8d998
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398269"
---
# <span data-ttu-id="523ea-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="523ea-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="523ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="523ea-102">SYNOPSIS</span></span>
<span data-ttu-id="523ea-103">建立 SQL Server 自動備份的群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="523ea-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="523ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="523ea-104">SYNTAX</span></span>

### <span data-ttu-id="523ea-105">StorageUriSqlServerAutoBackup (預設) </span><span class="sxs-lookup"><span data-stu-id="523ea-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="523ea-106">StorageCoNtextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="523ea-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="523ea-107">描述</span><span class="sxs-lookup"><span data-stu-id="523ea-107">DESCRIPTION</span></span>
<span data-ttu-id="523ea-108">**New-AzCMSqlServerAutoBackupConfig** Cmdlet 會建立 SQL Server 自動備份的群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="523ea-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="523ea-109">例子</span><span class="sxs-lookup"><span data-stu-id="523ea-109">EXAMPLES</span></span>

### <span data-ttu-id="523ea-110">範例 1：使用儲存空間 URI 和帳戶金鑰建立自動備份組</span><span class="sxs-lookup"><span data-stu-id="523ea-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="523ea-111">此命令會指定儲存空間 URI 和帳戶金鑰，以建立自動備份組組物件。</span><span class="sxs-lookup"><span data-stu-id="523ea-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="523ea-112">自動備份已啟用，且自動備份會保留 10 天。</span><span class="sxs-lookup"><span data-stu-id="523ea-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="523ea-113">該命令會將結果儲存在$AutoBackupConfig變數中。</span><span class="sxs-lookup"><span data-stu-id="523ea-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="523ea-114">您可以為其他 Cmdlet 指定此組Set-AzVMSqlServerExtension專案。</span><span class="sxs-lookup"><span data-stu-id="523ea-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="523ea-115">範例 2：使用儲存內容建立自動備份組式</span><span class="sxs-lookup"><span data-stu-id="523ea-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="523ea-116">第一個命令會建立儲存內容，然後將它儲存在$StorageCoNtext變數中。</span><span class="sxs-lookup"><span data-stu-id="523ea-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="523ea-117">詳細資訊請參閱 New-AzureStorageCoNtext。</span><span class="sxs-lookup"><span data-stu-id="523ea-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="523ea-118">第二個命令會指定自動備份組$StorageCoNtext。</span><span class="sxs-lookup"><span data-stu-id="523ea-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="523ea-119">自動備份已啟用，且自動備份會保留 10 天。</span><span class="sxs-lookup"><span data-stu-id="523ea-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="523ea-120">範例 3：使用儲存內容建立具有加密和密碼的自動備份組</span><span class="sxs-lookup"><span data-stu-id="523ea-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="523ea-121">此命令會建立並儲存自動備份群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="523ea-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="523ea-122">命令會指定在上一個範例中建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="523ea-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="523ea-123">命令會啟用密碼加密。</span><span class="sxs-lookup"><span data-stu-id="523ea-123">The command enables encryption with password.</span></span>
<span data-ttu-id="523ea-124">密碼先前儲存為數據變數中的安全$CertificatePassword字串。</span><span class="sxs-lookup"><span data-stu-id="523ea-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="523ea-125">若要建立安全字串，請使用 ConvertTo-SecureString Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="523ea-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="523ea-126">參數</span><span class="sxs-lookup"><span data-stu-id="523ea-126">PARAMETERS</span></span>

### <span data-ttu-id="523ea-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="523ea-127">-BackupScheduleType</span></span>
<span data-ttu-id="523ea-128">備份排程類型、手動或自動化</span><span class="sxs-lookup"><span data-stu-id="523ea-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="523ea-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="523ea-129">-BackupSystemDbs</span></span>
<span data-ttu-id="523ea-130">備份系統資料庫</span><span class="sxs-lookup"><span data-stu-id="523ea-130">Backup system databases</span></span>

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

### <span data-ttu-id="523ea-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="523ea-131">-CertificatePassword</span></span>
<span data-ttu-id="523ea-132">指定密碼以加密用來執行 SQL Server 加密備份的憑證。</span><span class="sxs-lookup"><span data-stu-id="523ea-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="523ea-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523ea-133">-DefaultProfile</span></span>
<span data-ttu-id="523ea-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="523ea-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="523ea-135">-啟用</span><span class="sxs-lookup"><span data-stu-id="523ea-135">-Enable</span></span>
<span data-ttu-id="523ea-136">表示已啟用 SQL Server 虛擬機器的自動備份。</span><span class="sxs-lookup"><span data-stu-id="523ea-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="523ea-137">如果您指定此參數，自動化備份會針對所有目前和新資料庫設定備份排程。</span><span class="sxs-lookup"><span data-stu-id="523ea-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="523ea-138">這會更新您的受管理的備份設定，以遵循此排程。</span><span class="sxs-lookup"><span data-stu-id="523ea-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="523ea-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="523ea-139">-EnableEncryption</span></span>
<span data-ttu-id="523ea-140">表示此 Cmdlet 啟用加密。</span><span class="sxs-lookup"><span data-stu-id="523ea-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="523ea-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="523ea-141">-FullBackupFrequency</span></span>
<span data-ttu-id="523ea-142">每天或每週的 Sql Server 完整備份頻率</span><span class="sxs-lookup"><span data-stu-id="523ea-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="523ea-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="523ea-143">-FullBackupStartHour</span></span>
<span data-ttu-id="523ea-144">當 Sql Server 完整備份 (0-23) 小時</span><span class="sxs-lookup"><span data-stu-id="523ea-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="523ea-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="523ea-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="523ea-146">Sql Server 完整備份視窗 ，以小時表示</span><span class="sxs-lookup"><span data-stu-id="523ea-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="523ea-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="523ea-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="523ea-148">Sql Server 記錄備份頻率，每 1-60 分鐘一次</span><span class="sxs-lookup"><span data-stu-id="523ea-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="523ea-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523ea-149">-ResourceGroupName</span></span>
<span data-ttu-id="523ea-150">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="523ea-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="523ea-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="523ea-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="523ea-152">指定要保留備份的天數。</span><span class="sxs-lookup"><span data-stu-id="523ea-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="523ea-153">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="523ea-153">-StorageContext</span></span>
<span data-ttu-id="523ea-154">指定要用來儲存備份的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="523ea-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="523ea-155">若要取得 **AzureStorageCoNtext 物件** ，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="523ea-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="523ea-156">預設值為與 SQL Server 虛擬機器相關聯的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="523ea-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="523ea-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="523ea-157">-StorageKey</span></span>
<span data-ttu-id="523ea-158">指定 Blob 儲存帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="523ea-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="523ea-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="523ea-159">-StorageUri</span></span>
<span data-ttu-id="523ea-160">指定 Blob 儲存帳戶 (URI) 統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="523ea-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="523ea-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523ea-161">CommonParameters</span></span>
<span data-ttu-id="523ea-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="523ea-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523ea-163">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="523ea-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523ea-164">輸入</span><span class="sxs-lookup"><span data-stu-id="523ea-164">INPUTS</span></span>

### <span data-ttu-id="523ea-165">沒有</span><span class="sxs-lookup"><span data-stu-id="523ea-165">None</span></span>
<span data-ttu-id="523ea-166">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="523ea-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="523ea-167">輸出</span><span class="sxs-lookup"><span data-stu-id="523ea-167">OUTPUTS</span></span>

### <span data-ttu-id="523ea-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="523ea-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="523ea-169">筆記</span><span class="sxs-lookup"><span data-stu-id="523ea-169">NOTES</span></span>

## <span data-ttu-id="523ea-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="523ea-170">RELATED LINKS</span></span>

[<span data-ttu-id="523ea-171">New-AzureMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="523ea-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="523ea-172">Set-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="523ea-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


