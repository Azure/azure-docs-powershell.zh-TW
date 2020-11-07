---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 2a1dbf5eea7f772a7819ed341a681adc24134225
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801377"
---
# Set-AzureRmVMSqlServerExtension

## 摘要
在虛擬機器上設定 Azure SQL Server 延伸。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVMSqlServerExtension** Cmdlet 會在虛擬機器上設定 AzureSQL 伺服器延伸。

## 示例

### 範例1：在虛擬機器上設定自動修補設定
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

第一個命令會使用 **AzureVMSqlServerAutoPatchingConfig** Cmdlet 建立設定物件。
該命令會將設定儲存在 $AutoPatchingConfig 變數中。

第二個命令會透過使用 Get-AzureRmVM Cmdlet，在名為 Service02 的服務上，取得名為 VirtualMachine11 的虛擬機器。
命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。

目前的 Cmdlet 會針對虛擬機器設定 $AutoPatchingConfig 中的自動修補設定。
命令會將虛擬機器傳遞到 Update-AzureRmVM Cmdlet。

### 範例2：在虛擬機器上設定自動備份設定
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

第一個命令會使用 **AzureVMSqlServerAutoBackupConfig** Cmdlet 建立設定物件。
該命令會將設定儲存在 $AutoBackupConfig 變數中。

第二個命令會在名為 Service02 的服務上取得名為 VirtualMachine11 的虛擬機器，然後將它傳遞到目前的 Cmdlet。

目前的 Cmdlet 會在虛擬機器的 $AutoBackupConfig 中設定自動備份設定。
命令會將虛擬機器傳遞到 Update-AzureRmVM Cmdlet。

### 範例3：停用虛擬機器上的 SQL Server 延伸
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。
此命令會在該虛擬機器上停用 SQL Server 虛擬電腦延伸。

### 範例4：卸載特定虛擬機器上的 SQL Server extension （機器翻譯）
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。
此命令會卸載該虛擬機器上的 SQL Server 虛擬機器延伸。

## 參數

### -AutoBackupSettings
指定自動 SQL Server 備份設定。
若要建立 **AutoBackupSettings** 物件，請使用 New-AzureVMSqlServerAutoBackupConfig Cmdlet。

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
指定自動 SQL Server 修補設定。
若要建立 **AutoPatchingSettings** 物件，請使用 New-AzureVMSqlServerAutoPatchingConfig Cmdlet。

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定虛擬機器的位置。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定副檔名的 SQL 伺服器名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -版本
指定 SQL Server 延伸的版本。

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定此 Cmdlet 設定 SQL Server 延伸的虛擬機器名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSAzureOperationResponse 中的 [計算] 命令

## 筆記

## 相關連結

[AzureRmVM](./Get-AzureRmVM.md)

[AzureRmVMSqlServerExtension](./Get-AzureRMVMSqlServerExtension.md)





[移除-AzureRmVMSqlServerExtension](./Remove-AzureRMVMSqlServerExtension.md)

[更新-AzureRmVM](./Update-AzureRmVM.md)


