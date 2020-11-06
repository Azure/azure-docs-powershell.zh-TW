---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450470"
---
# Get-AzureRmSiteRecoveryJob

## 摘要
取得目前網站復原電子倉庫的操作資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByParam (預設) 
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmSiteRecoveryJob** Cmdlet 會取得 Azure 網站恢復作業。
您可以使用這個 Cmdlet 來查看目前網站復原電子倉庫的操作資訊。

## 示例

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -EndTime
指定作業的結束時間。
這個 Cmdlet 會取得在指定時間之前所啟動的所有作業。
若要取得此參數的 **DateTime** 物件，請使用 Get-Date Cmdlet。
如需詳細資訊，請輸入 `Get-Help Get-Date` 。

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -工作
指定網站還原作業。

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定識別作業的唯一名稱。

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
指定作業的開始時間。
這個 Cmdlet 會取得在指定時間之後所啟動的所有作業。

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
指定網站還原作業的輸入狀態。
這個 Cmdlet 會取得符合指定狀態的所有作業。
此參數可接受的值為：

- NotStarted
- 正在
- 成功
- 換句話說
- 成功
- 取消
- 封存

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
指定作業目標物件的識別碼。

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### ASRJob
參數「作業」接受管道中類型 ' ASRJob」的值

## 輸出

### System.object. IEnumerable ' 1 [SiteRecovery. ASRJob] （）

## 筆記

## 相關連結

[重新開機-AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[Resume-AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[停止 AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
