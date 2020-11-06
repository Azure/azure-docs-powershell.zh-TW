---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 2d1c4fe635e6d4bc509f82f1af376ee0f662217a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449665"
---
# Restart-AzureRmWebAppSlot

## 摘要

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### S1
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Restart-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Restart AzureRmWebAppSlot** Cmdlet 會停止，然後啟動 Azure Web App 槽。
如果 Web 應用程式槽處於停止狀態，請使用 Start-AzureRmWebAppSlot Cmdlet。

## 示例

### 範例1
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

這個命令會重新開機與資源群組 Slot001 相關聯之 web app ContosoWebApp 的槽，其預設為 Web-WestUS

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
WebApp 名稱

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組名稱

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -槽
WebApp 槽名稱

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
WebApp 物件

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### [Microsoft Azure. 管理] 網站
參數： WebApp (ByValue) 

## 輸出

### [Microsoft Azure. 管理] 網站

## 筆記

## 相關連結

[AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[新-AzureRMWebAppSlot](./New-AzureRMWebAppSlot.md)

[移除-AzureRMWebAppSlot](./Remove-AzureRMWebAppSlot.md)

[Set-AzureRMWebAppSlot](./Set-AzureRMWebAppSlot.md)

[開始-AzureRMWebAppSlot](./Start-AzureRMWebAppSlot.md)

[停止 AzureRMWebAppSlot](./Stop-AzureRMWebAppSlot.md)

[AzureRmWebApp](./Get-AzureRmWebApp.md)
