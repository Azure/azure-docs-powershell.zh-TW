---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: 2201a1ed8b09ae57f7595d22ee3565cb0d39483f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915701"
---
# <span data-ttu-id="bb1d6-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bb1d6-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="bb1d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1d6-103">取得在服務層級或 Api 層級所配置的診斷詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="bb1d6-104">診斷是用來記錄 Api 管理閘道的要求/回應。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="bb1d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb1d6-105">SYNTAX</span></span>

### <span data-ttu-id="bb1d6-106">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bb1d6-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb1d6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb1d6-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb1d6-108">描述</span><span class="sxs-lookup"><span data-stu-id="bb1d6-108">DESCRIPTION</span></span>
<span data-ttu-id="bb1d6-109">**Get-AzApiManagementDiagnostic** 會取得特定範圍內 Api 管理服務中所配置的診斷詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="bb1d6-110">例子</span><span class="sxs-lookup"><span data-stu-id="bb1d6-110">EXAMPLES</span></span>

### <span data-ttu-id="bb1d6-111">範例 1：在租使用者範圍中取得所有診斷。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
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

<span data-ttu-id="bb1d6-112">此命令會獲得 Api 管理服務中所有已配置的診斷。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="bb1d6-113">範例 2：在 Api 範圍中取得所有診斷</span><span class="sxs-lookup"><span data-stu-id="bb1d6-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
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

<span data-ttu-id="bb1d6-114">此命令會以 Api 範圍進行所有 `echo-api` 診斷</span><span class="sxs-lookup"><span data-stu-id="bb1d6-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="bb1d6-115">範例 3：取得 Id 指定的 API 範圍診斷</span><span class="sxs-lookup"><span data-stu-id="bb1d6-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
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

<span data-ttu-id="bb1d6-116">此命令會以 `applicationinsights` api 進行診斷 `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="bb1d6-117">參數</span><span class="sxs-lookup"><span data-stu-id="bb1d6-117">PARAMETERS</span></span>

### <span data-ttu-id="bb1d6-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bb1d6-118">-ApiId</span></span>
<span data-ttu-id="bb1d6-119">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-119">Identifier of existing API.</span></span>
<span data-ttu-id="bb1d6-120">如果指定，會返回 API 範圍診斷。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="bb1d6-121">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-121">This parameters is required.</span></span>

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

### <span data-ttu-id="bb1d6-122">-內容</span><span class="sxs-lookup"><span data-stu-id="bb1d6-122">-Context</span></span>
<span data-ttu-id="bb1d6-123">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bb1d6-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-124">This parameter is required.</span></span>

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

### <span data-ttu-id="bb1d6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1d6-125">-DefaultProfile</span></span>
<span data-ttu-id="bb1d6-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb1d6-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="bb1d6-127">-DiagnosticId</span></span>
<span data-ttu-id="bb1d6-128">現有診斷的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="bb1d6-129">如果指定，會返回產品範圍策略。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="bb1d6-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="bb1d6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb1d6-131">-ResourceId</span></span>
<span data-ttu-id="bb1d6-132">診斷或 Api 診斷的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="bb1d6-133">如果指定，會嘗試尋找識別碼的診斷。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="bb1d6-134">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-134">This parameter is required.</span></span>

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

### <span data-ttu-id="bb1d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1d6-135">CommonParameters</span></span>
<span data-ttu-id="bb1d6-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb1d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1d6-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb1d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1d6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bb1d6-138">INPUTS</span></span>

### <span data-ttu-id="bb1d6-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="bb1d6-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bb1d6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bb1d6-140">System.String</span></span>

## <span data-ttu-id="bb1d6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bb1d6-141">OUTPUTS</span></span>

### <span data-ttu-id="bb1d6-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bb1d6-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="bb1d6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bb1d6-143">NOTES</span></span>

## <span data-ttu-id="bb1d6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb1d6-144">RELATED LINKS</span></span>
