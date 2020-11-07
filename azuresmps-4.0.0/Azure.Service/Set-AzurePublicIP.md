---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967401"
---
# Set-AzurePublicIP

## 摘要
新增公用 IP 至 Azure 虛擬機器。

## 句法

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzurePublicIP** Cmdlet 會將公用 IP 新增至 Azure 虛擬機器。
如果您在現有的虛擬機器上執行這個 Cmdlet，請更新虛擬機器以實現您所做的變更。
您可以指定網功能變數名稱稱標籤，為公用 IP 建立對應的 DNS 專案。

## 示例

### 範例1：在現有的虛擬機器中新增公用 IP
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

這個命令會透過使用 **FTPInstance Cmdlet，** 在名為 FTPInAzure 的服務中，取得名為的虛擬機器。
命令會使用管線運算子，將該虛擬機器傳至目前的 Cmdlet。
目前的 Cmdlet 會新增公用 IP 名稱 ftpip。
該命令會將虛擬機器傳到由 **add-azurevm** Cmdlet （可實現您的變更）。

### 範例2：將公用 IP 新增至新的虛擬機器
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

這個命令會使用 **AzureVMConfig** Cmdlet 來建立虛擬機器設定物件。
該命令會將該物件傳遞至 **AzureProvisioningConfig** Cmdlet，這會提供額外的配置。
目前的 Cmdlet 會新增公用 IP 名稱 ftpip。
該命令會將設定傳遞到 **新的 add-azurevm** Cmdlet，這會建立虛擬機器。

### 範例3：新增公用 IP 與標籤至現有的虛擬機器
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

這個命令會透過使用 **FTPInstance Cmdlet，** 在名為 FTPInAzure 的服務中，取得名為的虛擬機器。
命令會使用管線運算子，將該虛擬機器傳至目前的 Cmdlet。
目前的 Cmdlet 會新增公用 IP 名稱 ftpip 和標籤 ipname。
此命令會更新實現變更的虛擬機器。

### 範例4：將公用 IP 和標籤新增至新的虛擬機器
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

這個命令會建立虛擬機器設定物件，然後將該物件傳遞給 **AzureProvisioningConfig** ，以提供額外的配置。
目前的 Cmdlet 會新增公用 IP 名稱 ftpip 和標籤 ipname。
命令會建立虛擬機器。

## 參數

### -DomainNameLabel
指定用於公用 IP 位址之對應 DNS 專案的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
指定 TCP 空閒超時時間（以分鐘為單位）。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### -PublicIPName
指定公用 IP 名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
指定此 Cmdlet 新增公用 IP 的虛擬機器。

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

### WindowsAzure. ServiceManagement. IPersistentVM

## 筆記

## 相關連結

[AzurePublicIP](./Get-AzurePublicIP.md)

[Add-azurevm](./Get-AzureVM.md)

[Add-azurevm](./New-AzureVM.md)

[新-AzureVMConfig](./New-AzureVMConfig.md)

[移除-AzurePublicIP](./Remove-AzurePublicIP.md)

[更新-Add-azurevm](./Update-AzureVM.md)


