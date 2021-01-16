---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276635"
---
# Set-AzVMSqlServerExtension

## 摘要
在虛擬機器上設定 Azure SQL Server 延伸。

## 句法

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzVMSqlServerExtension** Cmdlet 會在虛擬機器上設定 AzureSQL 伺服器延伸。

## 示例

### 範例1：在虛擬機器上設定自動修補設定
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

第一個命令會使用 **AzVMSqlServerAutoPatchingConfig** Cmdlet 建立設定物件。
該命令會將設定儲存在 $AutoPatchingConfig 變數中。
第二個命令會透過使用 Get-AzVM Cmdlet，在名為 Service02 的服務上，取得名為 VirtualMachine11 的虛擬機器。
命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。
目前的 Cmdlet 會針對虛擬機器設定 $AutoPatchingConfig 中的自動修補設定。
命令會將虛擬機器傳遞到 Update-AzVM Cmdlet。

### 範例2：在虛擬機器上設定自動備份設定
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

第一個命令會使用 **AzVMSqlServerAutoBackupConfig** Cmdlet 建立設定物件。
該命令會將設定儲存在 $AutoBackupConfig 變數中。
第二個命令會在名為 Service02 的服務上取得名為 VirtualMachine11 的虛擬機器，然後將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會在虛擬機器的 $AutoBackupConfig 中設定自動備份設定。
命令會將虛擬機器傳遞到 Update-AzVM Cmdlet。

### 範例3：停用虛擬機器上的 SQL Server 延伸
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。
此命令會在該虛擬機器上停用 SQL Server 虛擬電腦延伸。

### 範例4：卸載特定虛擬機器上的 SQL Server extension （機器翻譯）
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

這個命令會在 Service03 上取得名為 VirtualMachine08 的虛擬機器，然後將它傳遞到目前的 Cmdlet。
此命令會卸載該虛擬機器上的 SQL Server 虛擬機器延伸。

## 參數

### -AutoBackupSettings
指定自動 SQL Server 備份設定。
若要建立 **AutoBackupSettings** 物件，請使用 New-AzVMSqlServerAutoBackupConfig Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
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
若要建立 **AutoPatchingSettings** 物件，請使用 New-AzVMSqlServerAutoPatchingConfig Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
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
Type: System.String
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
Type: System.String
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
Type: System.String
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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### AutoPatchingSettings 的計算。

### AutoBackupSettings 的計算。

### KeyVaultCredentialSettings 的計算。

## 輸出

### PSAzureOperationResponse 中的 [計算] 命令

## 筆記

## 相關連結

[AzVM](./Get-AzVM.md)

[AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[新-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[新-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[移除-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[更新-AzVM](./Update-AzVM.md)


