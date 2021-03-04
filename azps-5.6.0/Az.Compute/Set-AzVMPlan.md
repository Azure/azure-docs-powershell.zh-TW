---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 9d3897b52d59c85caac3f68b9904878f14014606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915593"
---
# Set-AzVMPlan

## 簡介
設定虛擬機器上的 Marketplace 方案資訊。

## 語法

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Set-Az VIRTUALPlan** Cmdlet 會設定虛擬機器的 Azure Marketplace 方案資訊。
必須先啟用程式設計存取，或是使用 Azure 入口網站部署虛擬機器，才能透過命令列部署 Marketplace 映射。

## 例子

## 參數

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

### -名稱
指定來自 Marketplace 的影像名稱。
這是 Cmdlet 所Get-AzVMImageSku的值。
若要瞭解如何尋找影像資訊，請參閱在 Microsoft Azure 檔中使用 PowerShell 和 Azure CLI (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ 流覽及 https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) 選取 Azure 虛擬機器圖像。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -產品
指定來自 Marketplace 之圖像的產品。
此資訊與 **imageReference** 元素的 **Offer 值相同** 。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PromotionCode
指定促銷代碼。

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

### -Publisher
指定影像的發行者。
您可以使用 Cmdlet 找到Get-AzVMImagePublisher資訊。

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

### -VM
指定要設定 Marketplace 計畫的虛擬機器物件。
您可以使用 Get-AzVM Cmdlet 來取得虛擬機器物件。
您可以使用 New-AzVMConfig Cmdlet 來建立虛擬機器物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

### System.String

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

## 筆記

## 相關連結

[Get-AzMS](./Get-AzVM.md)

[Get-AzMSIMagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzKUImageSku](./Get-AzVMImageSku.md)

[New-AzMSCONFIG](./New-AzVMConfig.md)
