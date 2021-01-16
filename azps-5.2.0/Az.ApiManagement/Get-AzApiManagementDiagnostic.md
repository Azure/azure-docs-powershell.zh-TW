---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283676"
---
# <span data-ttu-id="56b2d-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="56b2d-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="56b2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="56b2d-103">取得在服務層級或 Api 層級設定的診斷詳細資料。</span><span class="sxs-lookup"><span data-stu-id="56b2d-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="56b2d-104">診斷用於記錄來自 Api 管理閘道的要求/回應。</span><span class="sxs-lookup"><span data-stu-id="56b2d-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="56b2d-105">句法</span><span class="sxs-lookup"><span data-stu-id="56b2d-105">SYNTAX</span></span>

### <span data-ttu-id="56b2d-106">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="56b2d-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56b2d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56b2d-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56b2d-108">說明</span><span class="sxs-lookup"><span data-stu-id="56b2d-108">DESCRIPTION</span></span>
<span data-ttu-id="56b2d-109">**AzApiManagementDiagnostic** 會取得 Api 管理服務中指定範圍內所設定之診斷程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="56b2d-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="56b2d-110">示例</span><span class="sxs-lookup"><span data-stu-id="56b2d-110">EXAMPLES</span></span>

### <span data-ttu-id="56b2d-111">範例1：取得租使用者範圍內設定的所有診斷。</span><span class="sxs-lookup"><span data-stu-id="56b2d-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
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

<span data-ttu-id="56b2d-112">這個命令會取得 Api 管理服務中設定的所有診斷程式。</span><span class="sxs-lookup"><span data-stu-id="56b2d-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="56b2d-113">範例2：取得在 Api 作用中設定的所有診斷</span><span class="sxs-lookup"><span data-stu-id="56b2d-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
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

<span data-ttu-id="56b2d-114">這個命令會取得在 Api 作用中設定的所有診斷 `echo-api`</span><span class="sxs-lookup"><span data-stu-id="56b2d-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="56b2d-115">範例3：取得 Id 指定的 API 範圍診斷</span><span class="sxs-lookup"><span data-stu-id="56b2d-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
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

<span data-ttu-id="56b2d-116">這個命令會取得 `applicationinsights` 在 api 中設定的診斷程式 `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="56b2d-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="56b2d-117">參數</span><span class="sxs-lookup"><span data-stu-id="56b2d-117">PARAMETERS</span></span>

### <span data-ttu-id="56b2d-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="56b2d-118">-ApiId</span></span>
<span data-ttu-id="56b2d-119">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="56b2d-119">Identifier of existing API.</span></span>
<span data-ttu-id="56b2d-120">如果已指定，則會傳回 API 範圍診斷。</span><span class="sxs-lookup"><span data-stu-id="56b2d-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="56b2d-121">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="56b2d-121">This parameters is required.</span></span>

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

### <span data-ttu-id="56b2d-122">-內容</span><span class="sxs-lookup"><span data-stu-id="56b2d-122">-Context</span></span>
<span data-ttu-id="56b2d-123">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="56b2d-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="56b2d-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="56b2d-124">This parameter is required.</span></span>

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

### <span data-ttu-id="56b2d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b2d-125">-DefaultProfile</span></span>
<span data-ttu-id="56b2d-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56b2d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b2d-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="56b2d-127">-DiagnosticId</span></span>
<span data-ttu-id="56b2d-128">現有診斷的識別碼。</span><span class="sxs-lookup"><span data-stu-id="56b2d-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="56b2d-129">如果已指定，將會傳回產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="56b2d-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="56b2d-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="56b2d-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="56b2d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56b2d-131">-ResourceId</span></span>
<span data-ttu-id="56b2d-132">診斷或 Api 診斷的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="56b2d-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="56b2d-133">如果已指定，將會嘗試透過識別碼尋找診斷。</span><span class="sxs-lookup"><span data-stu-id="56b2d-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="56b2d-134">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="56b2d-134">This parameter is required.</span></span>

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

### <span data-ttu-id="56b2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b2d-135">CommonParameters</span></span>
<span data-ttu-id="56b2d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56b2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b2d-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56b2d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b2d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="56b2d-138">INPUTS</span></span>

### <span data-ttu-id="56b2d-139">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="56b2d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="56b2d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="56b2d-140">System.String</span></span>

## <span data-ttu-id="56b2d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="56b2d-141">OUTPUTS</span></span>

### <span data-ttu-id="56b2d-142">ServiceManagement. PsApiManagementDiagnostic （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="56b2d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="56b2d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="56b2d-143">NOTES</span></span>

## <span data-ttu-id="56b2d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="56b2d-144">RELATED LINKS</span></span>
