---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966894"
---
# Select-AzureStorSimpleResource

## 摘要
將資源設定為目前的資源。

## 句法

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureStorSimpleResource** Cmdlet 會將資源設定為目前的資源。
選取資源之後，其他 Cmdlet 會套用在該資源內容中。

## 示例

### 範例1：第一次選取資源
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

這個命令會選取名為 Contoso64-Tsqa 的資源作為目前的內容。
在這個範例中，電腦先前沒有初始化此內容，因此您必須指定 *RegistrationKey* 參數的值。

### 範例2：嘗試選取資源
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### 範例3：選取先前選取的資源
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

這個命令會選取名為 Contoso64-Tsqa 的資源作為目前的內容。
在這個範例中，先前已選取該內容，因此您不需要指定 *RegistrationKey* 參數的值。

## 參數

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

### -RegistrationKey
指定註冊金鑰。
第一次選取資源時，請指定索引鍵。
在這個 Cmdlet 選取目前的資源之後，Cmdlet 會根據需要使用此金鑰。
如需詳細資訊，請參閱取得 Microsoft 開發人員網路上 [的服務註冊金鑰](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) 。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CoNtext.resourcename
指定要選取為目前資源之資源的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### StorSimpleResourceCoNtext
這個 Cmdlet 會傳回 **StorSimpleResourceCoNtext** 物件，其中包含資源內容的詳細資料。

## 筆記

## 相關連結

[AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[AzureStorSimpleResourceCoNtext](./Get-AzureStorSimpleResourceContext.md)


