---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621127"
---
# Get-AzRecoveryServicesVault

## 摘要
取得恢復服務電子倉庫的清單。

## 句法

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzRecoveryServicesVault** Cmdlet 會在目前的訂閱中取得恢復服務電子倉庫的清單。

## 示例

### 範例1
```
PS C:\> Get-AzRecoveryServicesVault
```

在選取的訂閱中取得保存庫清單。

### 範例2
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

在 [資源群組] 中取得選取訂閱的電子倉庫清單。

### 範例3
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

在資源群組中取得具有指定名稱的電子倉庫。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
指定要查詢之保存庫的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定 Azure 資源群組的名稱，以在其中建立指定的復原服務物件，或從該資源群組中取得。

```yaml
Type: System.String
Parameter Sets: (All)
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

### 所有

## 輸出

### ARSVault 中的 RecoveryServices

## 筆記

## 相關連結

[AzRecoveryServicesVaultSettingsFile](./Get-AzRecoveryServicesVaultSettingsFile.md)

[新-AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[移除-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)


