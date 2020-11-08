---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139333"
---
# Get-AzApiManagementDiagnostic

## 摘要
取得在服務層級或 Api 層級設定的診斷詳細資料。 診斷用於記錄來自 Api 管理閘道的要求/回應。

## 句法

### CoNtextParameterSet (預設) 
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzApiManagementDiagnostic** 會取得 Api 管理服務中指定範圍內所設定之診斷程式的詳細資料。

## 示例

### 範例1：取得租使用者範圍內設定的所有診斷。
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

這個命令會取得 Api 管理服務中設定的所有診斷程式。

### 範例2：取得在 Api 作用中設定的所有診斷
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

這個命令會取得在 Api 作用中設定的所有診斷 `echo-api`

### 範例3：取得 Id 指定的 API 範圍診斷
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

這個命令會取得 `applicationinsights` 在 api 中設定的診斷程式 `echo-api` 。

## 參數

### -ApiId
現有 API 的識別碼。
如果已指定，則會傳回 API 範圍診斷。
此為必要參數。

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -內容
PsApiManagementCoNtext 的實例。
這個參數是必要的。

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -DiagnosticId
現有診斷的識別碼。
如果已指定，將會傳回產品範圍原則。
這個參數是選用的。

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
診斷或 Api 診斷的 Arm 資源識別碼。 如果已指定，將會嘗試透過識別碼尋找診斷。 這個參數是必要的。

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### ServiceManagement. PsApiManagementCoNtext （ApiManagement）

### System.object

## 輸出

### ServiceManagement. PsApiManagementDiagnostic （ApiManagement）

## 筆記

## 相關連結
