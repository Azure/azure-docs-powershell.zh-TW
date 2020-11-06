---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 61899a50c857fc3e8852d362d5905b0ca2fedf6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450639"
---
# Get-AzureRmDataLakeStoreAccount

## 摘要
取得 Data Lake Store 帳戶的詳細資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### GetAllInSubscription (預設) 
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySpecificAccount
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmDataLakeStoreAccount** Cmdlet 會取得資料 Lake store 帳戶的詳細資料。

## 示例

### 範例1：取得資料 Lake Store 帳戶
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

這個命令會取得名為 ContosoADL 的帳戶。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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
指定要取得的帳戶名稱。

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要取得之 Data Lake Store 帳戶的資源群組的名稱。

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSDataLakeStoreAccount
要求的特定 Data Lake Store 帳戶。

### 清單<PSDataLakeStoreAccountBasic>
指定的資源群組或訂閱中的 Data Lake Store 帳戶清單。

## 筆記

## 相關連結

[新-AzureRmDataLakeStoreAccount](./New-AzureRmDataLakeStoreAccount.md)

[移除-AzureRmDataLakeStoreAccount](./Remove-AzureRmDataLakeStoreAccount.md)

[Set-AzureRmDataLakeStoreAccount](./Set-AzureRmDataLakeStoreAccount.md)

[Test-AzureRmDataLakeStoreAccount](./Test-AzureRmDataLakeStoreAccount.md)


