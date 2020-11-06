---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449671"
---
# Get-AzureRmDeletedWebApp

## 摘要
在訂閱中取得已刪除的 web 應用程式。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmDeletedWebApp** Cmdlet 會傳回訂閱中所有已刪除的 web 應用程式。 您可以選擇性地依據 [資源] 群組、[名稱] 和 [槽] 篩選刪除的應用程式。 您可以有多個已刪除的應用程式，其名稱和資源群組都相同。 檢查 DeletionTime，以辨別共用相同名稱的已刪除 app。

## 示例

### 範例1
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

這個命令會取得名為 ContosoSite 的已刪除應用程式，其名稱為「資源群組預設-Web-WestUS」。

## 參數

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

### -名稱
Web 應用程式的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

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

### -槽
Web 應用程式槽的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。
如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### WebApps WebApps. PSAzureDeletedWebApp （）

## 筆記

## 相關連結

[Restore-AzureRmDeletedWebApp](./Restore-AzureRmDeletedWebApp.md)
