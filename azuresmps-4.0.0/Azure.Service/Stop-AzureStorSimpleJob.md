---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967458"
---
# Stop-AzureStorSimpleJob

## 摘要
停止 StorSimple 作業。

## 句法

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureStorSimpleJob** Cmdlet 會停止日常的 StorSimple 作業。
您可以提供實例識別碼或作業名稱來指定作業。

## 示例

### 範例1：停止裝置的作業
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

這個命令會使用 **AzureStorSimpleJob** Cmdlet 來取得名為 Device07 之裝置的工作。
命令會使用管線運算子將作業傳遞到目前的 Cmdlet。
目前的 Cmdlet 會停止命令傳遞給它的任何作業。
命令會指定 *Force* 參數，因此在停止作業之前，不會提示您進行確認。

### 範例2：停止特定作業
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

這個命令會停止具有指定實例識別碼的作業。

## 參數

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

### -InstanceId
指定要停止的裝置作業識別碼。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### DeviceJobDetails
這個 Cmdlet 會取得這個 Cmdlet 停止的 **DeviceJob** 詳細資料。

## 筆記

## 相關連結

[AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


