---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967222"
---
# Start-AzureStorSimpleDeviceFailoverJob

## 摘要
啟動大量容器群組的容錯移轉作業。

## 句法

### 空白 (預設) 
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureStorSimpleDeviceFailoverJob** Cmdlet 會將一個或多個卷容器群組的容錯移轉作業從一個裝置移到另一個裝置。

## 示例

### 範例1：針對命名的裝置和命名目標裝置啟動容錯移轉作業
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

這個命令會透過 **AzureStorSimpleFailoverVolumeContainers** Cmdlet，透過名為 ChewD_App7 的裝置取得容錯移轉磁片容器。
該命令會將結果傳遞到 **物件** 的 Cmdlet，該指令會放下 **IsDCGroupEligibleForDR** 屬性不是 $True 值的那些容器。
如需詳細資訊，請輸入 `Get-Help Where-Object` 。
目前的 Cmdlet 會針對其餘的容錯移轉磁片容器啟動容錯移轉作業。
命令會指定裝置名稱和目標裝置名稱。
此命令會傳回 Cmdlet 啟動作業的實例識別碼。

### 範例2：針對由識別碼指定的裝置和目標裝置啟動容錯移轉作業
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

這個命令會使用 **AzureStorSimpleFailoverVolumeContainers** ，透過名為 ChewD_App7 的裝置，取得容錯移轉磁片容器。
該命令會將結果傳遞到物件，該 **物件** 會放下 containters 的值不是 **IsDCGroupEligibleForDR** 屬性的 $True。
Cmdlet 會將結果傳遞到 **Select 物件** Cmdlet，以選取要傳遞到目前 Cmdlet 的第一個物件。
如需詳細資訊，請輸入 `Get-Help Select-Object` 。
目前的 Cmdlet 會針對選取的 [容錯移轉磁片] 容器啟動容錯移轉作業。
命令會指定裝置識別碼和目標裝置識別碼。
此命令會傳回 Cmdlet 啟動作業的實例識別碼。

## 參數

### -DeviceId
指定要有卷容器群組的 StorSimple 裝置的實例識別碼。

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
指定要有卷容器群組的 StorSimple 裝置的名稱。

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定 Azure 設定檔。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceId
指定此 Cmdlet 針對磁片容器群組進行容錯移轉之 StorSimple 裝置的實例識別碼。

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName
指定此 Cmdlet 針對磁片容器群組進行容錯移轉之 StorSimple 裝置的名稱。

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumecontainerGroups
指定此 Cmdlet 容錯移轉至另一個裝置的卷容器群組清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
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

### 清單\<DataContainerGroup\>
您可以將大量容器群組的清單輸送到這個 Cmdlet。

## 輸出

### 字串

## 筆記

## 相關連結

[AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


