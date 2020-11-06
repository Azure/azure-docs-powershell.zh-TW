---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: f9f0808db919ad5d1d38b29daa720fb9b8a5baee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447171"
---
# Get-AzureRmBackupJobDetails

## 摘要
取得備份作業的詳細資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### JobsFiltersSet (預設) 
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdFiltersSet
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmBackupJobDetails** Cmdlet 會取得 Azure 備份作業的詳細資料。
您可以使用這個 Cmdlet 來收集失敗作業的相關資訊。

## 示例

### 範例1：顯示失敗作業的詳細資料
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。
該命令會將該物件儲存在 $Vault 變數中。

第二個命令會從 $Vault 中的 vault 取得失敗的作業，然後將它們儲存在 $Jobs 陣列變數中。

第三個作業會取得 $Jobs 變數中第一個工作的詳細資料，然後將這些詳細資料儲存在 $JobDetails 變數中。

Final 命令會使用標準的點語法來顯示 $JobDetails 的 **ErrorDetails** 屬性。

### 範例2：針對失敗的工作顯示建議的動作
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

這個命令會顯示第一個範例中建立的 $JobDetails 變數所建議的動作。

## 參數

### -工作
指定此 Cmdlet 取得詳細資料的作業。
若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -作業 Id
指定此 Cmdlet 所取得之詳細資料的作業識別碼。
識別碼是 **AzureRmBackupJob** 物件的 **InstanceId** 屬性。
若要取得 **AzureRmBackupJob** 物件，請使用 AzureRmBackupJob。

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -保存庫
指定此 Cmdlet 取得作業詳細資料的備份保存庫。
若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### AzureRmBackupJobDetails

## 筆記
* 所有

## 相關連結

[AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[AzureRmBackupVault](./Get-AzureRmBackupVault.md)


