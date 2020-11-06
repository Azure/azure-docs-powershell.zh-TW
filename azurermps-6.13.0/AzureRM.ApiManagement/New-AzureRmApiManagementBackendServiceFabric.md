---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447522"
---
# New-AzureRmApiManagementBackendServiceFabric

## 摘要
建立物件 `PsApiManagementServiceFabric`

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明

**新的-AzureRmApiManagementBackendServiceFabric** Cmdlet `PsApiManagementServiceFabric` 會建立要在 Cmdlet **New-AzureRmApiManagementBackend** 和 **Set AzureRmApiManagementBackend** 中使用的物件。

## 示例

### 範例1：建立後端服務結構 In-Memory 物件
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

建立後端服務結構合約

## 參數

### -ClientCertificateThumbprint
管理端點的用戶端憑證指紋。
這個參數是必要的。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -ManagementEndpoint
Service Fabric 群集管理端點。
這個參數是必要的。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPartitionResolutionRetry
解析 Service Fabric 分區時的最大重試次數。
此參數為 optional，且預設值為5。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerCertificateThumbprint
[憑證群集管理服務] 用來進行 tls 通訊的指紋。這個參數是選用的。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerX509Name
Server X509 憑證名稱集合。
這個參數是選用的。

```yaml
Type: System.Collections.Hashtable
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

### System.object

## 輸出

### ServiceManagement. PsApiManagementServiceFabric （ApiManagement）

## 筆記

## 相關連結

[AzureRmApiManagementBackend](./Get-AzureRmApiManagementBackend)

[新-AzureRmApiManagementBackend](./New-AzureRmApiManagementBackend.md)

[新-AzureRmApiManagementBackendProxy](./New-AzureRmApiManagementBackendProxy.md)

[Set-AzureRmApiManagementBackend](./Set-AzureRmApiManagementBackend.md)

[移除-AzureRmApiManagementBackend](./Remove-AzureRmApiManagementBackend.md)
