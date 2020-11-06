---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3d4867e33fe388195904d31fa7e83abe26dde474
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447433"
---
# Get-AzureRmVMAEMExtension

## 摘要
取得 AEM 延伸的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVMAEMExtension** Cmdlet 會取得 Azure 增強型監視 (AEM) 延伸的相關資訊。

## 示例

### 範例1：取得 AEM 延伸
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

這個命令會取得名為 contoso-server 的虛擬機器的 AEM 延伸資訊。

## 參數

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

### -名稱
指定虛擬機器的名稱。
這個 Cmdlet 會取得此 Cmdlet 所指定之虛擬機器上的 AEM 延伸資訊。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSType
指定作業系統磁片作業系統的類型。
如果作業系統磁片沒有類型，您必須指定此參數。
此參數可接受的值為： Windows 和 Linux。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。
這個 Cmdlet 會取得該虛擬機器上 AEM 延伸的資訊。

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

### -狀態
表示此 Cmdlet 只會取得 AEM 延伸的 [實例] 視圖。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定虛擬機器的名稱。
這個 Cmdlet 會針對此參數指定的虛擬機器，取得 AEM 延伸的相關資訊。

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

### SwitchParameter 的系統管理功能

## 輸出

### PSVirtualMachineExtension 中的 [計算] 命令

## 筆記

## 相關連結

[移除-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Set-AzureRmVMAEMExtension](./Set-AzureRmVMAEMExtension.md)

[Test-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


