---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: a57ed6bb12a1357ebd8d9b4f090bd1d551f3c554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911165"
---
# Publish-AzVMDscConfiguration

## 簡介
將 DSC 腳本上傳到 Azure Blob 儲存體。

## 語法

### 上傳存檔 (預設) 
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 建立存檔
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Publish-Az VIRTUALDscConfiguration Cmdlet** 會上傳您想要的狀態組態 (DSC) 腳本至 Azure Blob 儲存空間，之後可以使用 Set-AzVMDscExtension Cmdlet 將腳本新用至 Azure 虛擬機器。

## 例子

### 範例 1：建立 .zip 套件上傳至 Azure 儲存空間
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

此命令會為給定腳本和任何從屬資源模組建立 .zip 套件，並將其上傳到 Azure 儲存空間。

### 範例 2：建立 .zip 封裝，然後儲存到本地檔案
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

此命令會為指定腳本和任何從屬資源模組建立 .zip 套件，並儲存在名為 .\MyConfiguration.ps1.zip 的本地.\MyConfiguration.ps1.zip。

### 範例 3：新增組配置至存檔，然後將它上傳到儲存空間
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

此命令會將名為 Sample.ps1 的組配置新增到組配置存檔，以上傳至 Azure 儲存空間，並略過從屬資源模組。

### 範例 4：新增組配置和組組資料至存檔，然後將它上傳到儲存空間
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

此命令會將名為 Sample.ps1 的組SampleData.psd1 組組資料新增到組配置存檔，以上傳到 Azure 儲存空間。

### 範例 5：新增組配置、組組資料和其他內容至存檔，然後將它上傳到儲存空間
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

此命令會新增名為 Sample.ps1 的組SampleData.psd、組SampleData.psd1，以及將其他內容新增到組配置存檔，以上傳到 Azure 儲存空間。

## 參數

### -AdditionalPath
指定要納入組案存檔之檔案或目錄的路徑。
它會連同組配置一起下載到虛擬機器。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
指定指定組案資料的 .psd1 檔案路徑。
這會新增到組配置存檔，然後傳遞到組組函數。
它會由透過 Cmdlet 提供的組Set-AzVMDscExtension路徑所覆蓋

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
指定包含一或多個組配置的檔案路徑。
檔案可以是 Windows PowerShell 腳本 (.ps1) 或 Windows PowerShell 模組 (.psm1) 檔案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
指定已上傳組配置的 Azure 儲存容器名稱。

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -強制
強制執行命令，但不要求使用者確認。

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

### -OutputArchivePath
指定要撰寫組案存檔的 .zip 檔案路徑。
使用這個參數時，設定腳本不會上傳到 Azure Blob 儲存體。

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含儲存空間帳戶的資源組名。

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
表示此 Cmdlet 排除組配置存檔中的 DSC 資源相依性。

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

### -StorageAccountName
指定用來將設定腳本上傳到 ContainerName 參數所指定的 *容器的 Azure* 儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
指定儲存終點的尾碼。

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.String[]

## 輸出

### System.String

## 筆記

## 相關連結

[Get-AzMSDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzMSDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzMSDscExtension](./Set-AzVMDscExtension.md)


