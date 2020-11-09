---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287656"
---
# Invoke-AzStorageSyncCompatibilityCheck

## 摘要
檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。

## 句法

### PathBased (預設) 
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## 說明
**AzStorageSyncCompatibilityCheck** Cmdlet 會檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。針對本機或遠端路徑，它會在系統和檔案命名空間上執行一組驗證，然後傳回它找到的任何相容性問題。
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
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

這個命令會檢查系統與 C:\DATA. 中的檔案和資料夾的相容性

### 範例2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

這個命令會檢查 C:\DATA 中檔案和資料夾的相容性，但不會執行系統相容性檢查。

### 範例3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSValidationResult 中的 StorageSync。

## 筆記
* 關鍵字： azure、Az、arm、資源、管理、storagesync、filesync

## 相關連結
