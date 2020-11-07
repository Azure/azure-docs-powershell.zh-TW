---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967378"
---
# New-AzureCertificateSetting

## 摘要
為憑證建立憑證設定物件在服務中。

## 句法

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**新的-AzureCertificateSetting** Cmdlet 會針對 Azure 服務中的憑證建立憑證設定物件。

您可以使用 [憑證設定] 物件，透過 **AzureProvisioningConfig** Cmdlet 來建立設定物件。
使用 configuration 物件，透過 **新的 add-azurevm** Cmdlet 來建立虛擬機器。
您可以使用憑證設定物件，透過 **AzureQuickVM** Cmdlet 來建立虛擬機器。

## 示例

### 範例1：建立憑證設定物件
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

這個命令會為現有的憑證建立憑證設定物件。

### 範例2：建立使用配置設定物件的虛擬機器
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

第一個命令會使用 **Add-AzureCertificate** Cmdlet，將憑證 ContosoCert 新增到名為 ContosoService 的服務。

第二個命令會建立憑證設定物件，然後將它儲存在 $CertificateSetting 變數中。

第三個命令會使用 **AzureVMImage** Cmdlet 從影像儲存庫中取得影像。
這個命令會將圖像儲存在 $Image 變數中。

最終命令會使用 **AzureVMConfig** Cmdlet，根據 $Image 中的影像建立虛擬機器設定物件。
命令會使用管線運算子，將該物件傳遞到 **AzureProvisioningConfig** Cmdlet。
該 Cmdlet 會將提供資訊新增到設定。
該命令會將物件傳遞給 **新的 add-azurevm** Cmdlet，這會建立虛擬機器。

## 參數

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

### -StoreName
指定要放入憑證的憑證存放區。
有效值為： 

- AddressBook
- AuthRoot
- CertificateAuthority
- 許可證
- 我的帳戶
- 根
- TrustedPeople
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -指紋
指定憑證的指紋。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureCertificate](./Add-AzureCertificate.md)

[附加 AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[AzureCertificate](./Get-AzureCertificate.md)

[AzureVMImage](./Get-AzureVMImage.md)

[新-AzureQuickVM](./New-AzureQuickVM.md)

[Add-azurevm](./New-AzureVM.md)

[移除-AzureCertificate](./Remove-AzureCertificate.md)


