---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447868"
---
# Get-AzureRmBackupJob

## 摘要
取得備份作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### FiltersSet (預設) 
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。

## 示例

### 範例1：取得備份保存庫中的所有工作
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。

第二個命令會在 $Vault 中取得 vault 的所有作業。

### 範例2：取得完成的工作
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

這個命令會在 $Vault 中從 vault 中取得已完成的工作。

### 範例3：取得最後一周失敗的工作
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

此命令會從 $Vault 中的 [vault] 的最後一周取得失敗的工作。
*From* 參數指定過去七天的時間。
該命令不會指定 *To* 參數的值。
因此，它會使用目前時間的預設值。

### 範例4：輪詢備份完成的正在進行中的工作
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。

腳本的第一行會取得正在進行的 $Vault 中的所有工作，然後將這些作業儲存在 $Jobs 陣列變數中。

第二行會將 $Jobs 陣列中的第一個工作儲存在 $Job 變數中。

第三行會啟動一個 **while** 迴圈，以檢查作業的目前狀態，直到作業完成為止。
如需有關 **while** 關鍵字的資訊，請輸入 `Get-Help about_While` 。

**While** 迴圈會將訊息寫入主控台，並在十秒內休眠，然後更新 $Job 變數。
此腳本會使用 $Job 現有的值和目前的 Cmdlet 來更新 $Job 變數，以取得工作的目前狀態。
如需有關 Windows PowerShell Cmdlet 的詳細資訊，請輸入 `Get-Help Write-Host` 和 `Get-Help Start-Sleep` 。

腳本的最後一行告訴您腳本已完成。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -從
指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。
若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。
如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -工作
指定此 Cmdlet 取得的作業。
若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -作業 Id
指定此 Cmdlet 所取得作業的識別碼。
識別碼是 **AzureRmBackupJob** 物件的 **InstanceId** 屬性。
若要取得 **AzureRmBackupJob** 物件，請使用 AzureRmBackupJob。

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -操作
指定此 Cmdlet 取得作業的操作。
此參數可接受的值為：

- 備份 
- ConfigureBackup 
- DeleteBackupData 
- 註冊表 
- 還原 
- 對 
- 登出

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -狀態
指定此 Cmdlet 取得作業的狀態。
此參數可接受的值為：

- 正在
- 成功
- 取消
- 正在
- 完畢
- CompletedWithWarnings 

您可以指定此參數來尋找所有正在進行中的作業或所有失敗的工作。

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。
預設值為目前的系統時間。
如果您指定此參數，您也必須指定 *From* 參數。

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -類型
指定此 Cmdlet 取得備份作業的容器類型。
目前唯一支援的值為 Add-azurevm。

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -保存庫
指定此 Cmdlet 取得作業的備份保存庫。
若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### AzureRmBackupVault

## 輸出

### AzureRmBackupJob[]
這個 Cmdlet 會傳回一或多個備份作業。

## 筆記
* 所有

## 相關連結

[AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[停止 AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[稍候-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


