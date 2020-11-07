---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967737"
---
# Get-AzureStorSimpleDeviceConnectedInitiator

## 摘要
取得 StorSimple 裝置可用的 iSCSI 連線。

## 句法

### IdentifyById
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureStorSimpleDeviceConnectedInitiator** Cmdlet 會取得適用于 StorSimple 裝置的 iSCSI 連線清單。
這個 Cmdlet 傳回的 iSCSI 連線物件包含下列屬性：

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **交互**
- **Iqn**
- **IscsiConnectionId**

這個 Cmdlet 只會在為裝置開啟 iSCSI 連線時取得連線物件。
根據預設，會關閉連線。

## 示例

### 範例1：取得裝置的所有連線
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

這個命令會取得名為 Contoso63-AppVm 的裝置的所有 iSCSI 連線。
這個命令只會在為裝置開啟連線時，才會傳回連線。

## 參數

### -DeviceId
指定要取得 iSCSI 啟動器的 StorSimple 裝置實例識別碼。

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
指定要取得 iSCSI 啟動器之 StorSimple 裝置的名稱。

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### 清單\<IscsiConnection\>
這個 Cmdlet 會傳回包含下列屬性的 iSCSI 連線物件： 

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **交互**
- **Iqn**
- **IscsiConnectionId**

## 筆記

## 相關連結

[AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


