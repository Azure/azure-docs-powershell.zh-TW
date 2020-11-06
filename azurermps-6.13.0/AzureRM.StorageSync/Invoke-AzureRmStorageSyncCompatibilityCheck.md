---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450143"
---
# Invoke-AzureRmStorageSyncCompatibilityCheck

## 摘要
檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### PathBased (預設) 
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## 說明
**AzureRmStorageSyncCompatibilityCheck** Cmdlet 會檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。針對本機或遠端路徑，它會在系統和檔案命名空間上執行一組驗證，然後傳回它找到的任何相容性問題。
系統檢查：
- OS 相容性檔案命名空間檢查：
- 不支援的字元
- 檔案大小上限
- 最大路徑長度
- 檔長度上限
- 資料集大小上限
- 目錄深度上限

## 示例

### 範例1
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

這個命令會檢查系統與 C:\DATA. 中的檔案和資料夾的相容性

### 範例2
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

這個命令會檢查 C:\DATA 中檔案和資料夾的相容性，但不會執行系統相容性檢查。

### 範例3
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

這個命令會檢查系統與 C:\DATA 中的檔案和資料夾相容性，然後將結果匯出為 CSV 檔案至 C:\results。

## 參數

### -ComputerName
您執行此檢查的電腦。

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -認證
您要驗證之共用的認證。

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
您要驗證之共用的 UNC 路徑。

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -安靜
取消將輸出報告寫入到主控台。

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

### -SkipNamespaceChecks
設定此標誌以略過檔案命名空間驗證，只執行系統驗證。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
將此標誌設定為略過系統驗證，且只執行檔命名空間驗證。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSValidationResult 中的 StorageSync。

## 筆記
* 關鍵字： azure、azurerm、arm、資源、管理、storagesync、filesync

## 相關連結
