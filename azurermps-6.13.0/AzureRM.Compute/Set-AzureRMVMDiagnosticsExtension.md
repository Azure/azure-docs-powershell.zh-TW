---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 14687cf48f8f091a3902640655b3ac60893d8a8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449239"
---
# Set-AzureRmVMDiagnosticsExtension

## 摘要
在虛擬機器上配置 Azure diagnostics 延伸。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
AzureRmVMDiagnosticsExtension Cmdlet 會 **設定** 虛擬機器上的 Azure diagnostics 延伸。

## 示例

### 範例1：使用在診斷設定檔中指定的儲存空間帳戶來啟用診斷
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

這個命令使用診斷設定檔來啟用診斷。
檔案 diagnostics_publicconfig.xml 包含診斷延伸的公用 XML 配置，包括要傳送診斷資料之儲存空間帳戶的名稱。
診斷儲存空間帳戶必須與虛擬機器在同一個訂閱中。

### 範例2：使用儲存空間帳戶名稱啟用診斷
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

這個命令會使用儲存空間帳戶名稱來啟用診斷。
如果診斷設定未指定儲存空間帳戶名稱，或您想要覆寫設定檔中指定的診斷儲存空間帳戶名稱，請使用 *StorageAccountName* 參數。
診斷儲存空間帳戶必須與虛擬機器在同一個訂閱中。

### 範例3：使用儲存空間帳戶名稱和金鑰啟用診斷
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

這個命令會使用儲存空間帳戶名稱和金鑰來啟用診斷。
如果診斷儲存空間帳戶與虛擬機器的訂閱不同，則請明確指定其名稱和金鑰，以啟用將診斷資料傳送至該儲存空間帳戶。

## 參數

### -AutoUpgradeMinorVersion
指示此 Cmdlet 是否允許 Azure 來賓代理程式自動將延伸更新為較新的次要版本。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiagnosticsConfigurationPath
指定設定檔的路徑。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定虛擬機器的位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定延伸的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountEndpoint
指定 [儲存空間帳戶] 端點。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
指定儲存空間帳戶金鑰。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
指定儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageCoNtext
指定 Azure 儲存區內容。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
指定此虛擬機器要使用的副檔名版本。
若要取得版本，請使用 Microsoft 的值來執行 Get-AzureRmVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定此 Cmdlet 作用中的虛擬機器名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### IStorageCoNtext 中的 [Common.]

### System.object

## 輸出

### PSAzureOperationResponse 中的 [計算] 命令

## 筆記

## 相關連結

[AzureRmVMDiagnosticsExtension](./Get-AzureRMVMDiagnosticsExtension.md)

[AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[移除-AzureRmVMDiagnosticsExtension](./Remove-AzureRmVMDiagnosticsExtension.md)


