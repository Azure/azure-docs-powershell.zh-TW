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
# New-AzVMSqlServerAutoBackupConfig

## 簡介
建立 SQL Server 自動備份的群組原則物件。

## 語法

### StorageUriSqlServerAutoBackup (預設) 
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageCoNtextSqlServerAutoBackup
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzCMSqlServerAutoBackupConfig** Cmdlet 會建立 SQL Server 自動備份的群組原則物件。

## 例子

### 範例 1：使用儲存空間 URI 和帳戶金鑰建立自動備份組
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

此命令會指定儲存空間 URI 和帳戶金鑰，以建立自動備份組組物件。
自動備份已啟用，且自動備份會保留 10 天。
該命令會將結果儲存在$AutoBackupConfig變數中。
您可以為其他 Cmdlet 指定此組Set-AzVMSqlServerExtension專案。

### 範例 2：使用儲存內容建立自動備份組式
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

第一個命令會建立儲存內容，然後將它儲存在$StorageCoNtext變數中。
詳細資訊請參閱 New-AzureStorageCoNtext。

第二個命令會指定自動備份組$StorageCoNtext。
自動備份已啟用，且自動備份會保留 10 天。

### 範例 3：使用儲存內容建立具有加密和密碼的自動備份組
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

此命令會建立並儲存自動備份群組原則物件。
命令會指定在上一個範例中建立儲存內容。
命令會啟用密碼加密。
密碼先前儲存為數據變數中的安全$CertificatePassword字串。
若要建立安全字串，請使用 ConvertTo-SecureString Cmdlet。

## 參數

### -BackupScheduleType
備份排程類型、手動或自動化

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

### -BackupSystemDbs
備份系統資料庫

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

### -CertificatePassword
指定密碼以加密用來執行 SQL Server 加密備份的憑證。

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

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -啟用
表示已啟用 SQL Server 虛擬機器的自動備份。
如果您指定此參數，自動化備份會針對所有目前和新資料庫設定備份排程。
這會更新您的受管理的備份設定，以遵循此排程。

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

### -EnableEncryption
表示此 Cmdlet 啟用加密。

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

### -FullBackupFrequency
每天或每週的 Sql Server 完整備份頻率

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

### -FullBackupStartHour
當 Sql Server 完整備份 (0-23) 小時

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

### -FullBackupWindowInHours
Sql Server 完整備份視窗 ，以小時表示

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

### -LogBackupFrequencyInMinutes
Sql Server 記錄備份頻率，每 1-60 分鐘一次

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

### -ResourceGroupName
指定虛擬機器的資源組名。

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

### -RetentionPeriodInDays
指定要保留備份的天數。

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

### -StorageCoNtext
指定要用來儲存備份的儲存空間帳戶。
若要取得 **AzureStorageCoNtext 物件** ，請使用 New-AzureStorageContext Cmdlet。
預設值為與 SQL Server 虛擬機器相關聯的儲存空間帳戶。

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

### -StorageKey
指定 Blob 儲存帳戶的儲存金鑰。

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

### -StorageUri
指定 Blob 儲存帳戶 (URI) 統一資源識別項。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有
此 Cmdlet 不接受任何輸入。

## 輸出

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

## 筆記

## 相關連結

[New-AzureMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[Set-AzMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


