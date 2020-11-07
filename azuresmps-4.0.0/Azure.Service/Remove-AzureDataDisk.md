---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967612"
---
# Remove-AzureDataDisk

## 摘要
從 Azure 虛擬機器移除資料磁片。

## 句法

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureDataDisk** Cmdlet 會從 Azure 虛擬機器中移除資料磁片。
根據預設，這個 Cmdlet 不會從儲存空間帳戶中移除資料磁片 blob。

## 示例

### 範例1：移除資料磁片
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

這個命令會透過使用 **VirtualMachine07 Cmdlet，** 在名為 ContosoService 的服務中，取得名為的虛擬機器。
命令會使用管線運算子，將虛擬機器傳至目前的 Cmdlet。
目前的 Cmdlet 會移除擁有 LUN 0 的資料磁片。

### 範例2：移除資料磁片與虛擬硬碟檔案
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

這個命令會在名為 ContosoService 的服務中取得名為 VirtualMachine07 的虛擬機器。
該命令會將虛擬機器傳遞至目前的 Cmdlet。
目前的 Cmdlet 會移除擁有 LUN 0 的資料磁片。
此命令包括 *DeleteVHD* 參數。
因此，它也會刪除基礎虛擬硬碟。
此命令會使用 **add-azurevm** Cmdlet 來更新虛擬機器以反映您所做的變更。

## 參數

### -DeleteVHD
表示此 Cmdlet 會從 blob 儲存體中移除資料磁片與虛擬硬碟 (VHD) 。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
指定這個 Cmdlet 回應資訊事件的方式。

此參數可接受的值為：

- 持續
- 理會
- 看
- SilentlyContinue
- 停止
- 封存

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
指定資訊變數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LUN
指定虛擬機器中資料磁碟機的邏輯單元號碼 (LUN) 。
有效值為：0到15。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### -VM
指定附加至資料磁片的虛擬機器物件。
若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureDataDisk](./Add-AzureDataDisk.md)

[AzureDataDisk](./Get-AzureDataDisk.md)

[Add-azurevm](./Get-AzureVM.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[更新-Add-azurevm](./Update-AzureVM.md)


