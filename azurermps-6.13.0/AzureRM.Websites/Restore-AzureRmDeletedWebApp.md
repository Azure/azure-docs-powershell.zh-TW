---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449652"
---
# Restore-AzureRmDeletedWebApp

## 摘要
將已刪除的 web 應用程式還原到新的或現有的 web 應用程式。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### FromDeletedResourceName
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedApp
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## 說明
**Restore-AzureRmDeletedWebApp** Cmdlet 會還原已刪除的 web 應用程式。 TargetResourceGroupName、TargetName 和 TargetSlot 所指定的 web app 將會覆寫已刪除 web 應用程式的內容和設定。 如果未指定目標參數，則會自動使用已刪除的 web 應用程式的資源群組、名稱和槽來填入它們。 如果目標 web 應用程式不存在，則會自動在 TargetAppServicePlanName 指定的 app 服務方案中建立它。 RestoreContentOnly 切換參數只能用來還原已刪除 app 的檔案，而不需要 app 設定。

## 示例

### 範例1
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

還原名為 ContosoApp 的已刪除應用程式，其名稱為「資源群組預設-Web-WestUS」。 將會在名為 ContosoPlan 的應用程式服務方案中建立具有相同名稱和資源群組的新應用程式，並將已刪除的應用程式的檔案和設定還原到其中。

### 範例2
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

還原名為 ContosoApp 的已刪除應用程式的暫存槽，其名稱為「資源群組預設-WestUS」。 ContosoRestore 屬於資源群組的 web app （預設為 [網頁-EastUS]）將會被覆蓋。 已刪除的 web 應用程式設定將無法還原。

## 參數

### -AsJob
在背景中執行 Cmdlet

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

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
在不提示確認的情況下執行還原。

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

### -InputObject
已刪除的 Azure Web App。

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
已刪除的 Azure Web 應用程式的名稱。

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
已刪除的 Azure Web App 的 [資源] 群組。

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreContentOnly
還原 web 應用程式的檔案，但不要還原設定。

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

### -槽
已刪除的 Azure Web App 槽。

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAppServicePlanName
新 Azure Web App 的 App 服務規劃。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetName
新的 Azure Web App 名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName
包含新 Azure Web App 的資源群組。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetSlot
新的 Azure Web App 槽的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。
如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### WebApps WebApps. PSAzureDeletedWebApp （）

## 輸出

### PSSite 中的 WebApps。

## 筆記

## 相關連結

[AzureRmDeletedWebApp](./Get-AzureRmDeletedWebApp.md)
