---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793179"
---
# Invoke-AzStorageSyncChangeDetection

## 摘要
這個命令可以用來手動啟動命名空間變更的偵測。 您可以將它設定為整個共用、子資料夾或一組檔案的目標。 最多可以檢測到10000變更。 如果您知道變更範圍，請將此命令的執行限制為命名空間的一部分，因此變更偵測可以快速完成，且在10000變更限制內。

## 句法

### StringAndDirectoryParameterSet (預設) 
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### StringAndPathParameterSet
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdAndDirectoryParameterSet
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdAndPathParameterSet
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ObjectAndDirectoryParameterSet
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ObjectAndPathParameterSet
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
Azure 檔案同步處理會定期檢查同步處理 Azure 檔案共用中的命名空間，以取得與同步處理之外的其他方法所帶來的變更。目標是識別這些變更，並最終將它們同步處理到已連線的伺服器。 這個命令可以用來手動啟動命名空間變更的偵測。 您可以將它設定為整個共用、子資料夾或一組檔案的目標。 如果您知道變更範圍，請將此命令的執行限制為命名空間的一部分，因此變更偵測可以快速完成，且在10000變更限制內。

## 示例

### 範例1
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

在這個範例中，變更偵測會在同步處理 Azure 檔案共用的「資料」和「Reporting\Templates」目錄中執行。 所有路徑都是相對於 Azure 檔案共用命名空間的根。

### 範例2
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

在這個範例中，針對命令呼叫者已知已變更的一組檔案，會執行變更偵測。 我們的目標是讓 Azure 檔案同步偵測並同步處理這些變更。

### 範例3
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

在這個範例中，會針對「範例」目錄執行變更偵測，並以遞迴方式檢測子目錄中的變更。 請記住，此命令可以在自動中止前檢測到10000變更。 如果您懷疑已發生10000以上的變更，請在命名空間的子元件上執行命令。

## 參數

### -AsJob
在背景中執行 Cmdlet

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

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -DirectoryPath
將執行變更偵測的目錄。

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
CloudEndpoint 物件，通常是透過參數傳遞。

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
CloudEndpoint 的名稱。

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
在正常執行中，此 Cmdlet 在成功時不會傳回值。 如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。

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

### -Path
將執行變更偵測的路徑。

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recursive
指示目錄變更檢測是否為遞迴式。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
CloudEndpoint 資源識別碼

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageSyncServiceName
StorageSyncService 的名稱。

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncGroupName
SyncGroup 的名稱。

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### PSServerEndpoint 中的 StorageSync。

## 輸出

### System.void

## 筆記

## 相關連結
