---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: a330aa6df0da0be08de925d59e72018a028e7d82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911217"
---
# <span data-ttu-id="8a808-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a808-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="8a808-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a808-102">SYNOPSIS</span></span>
<span data-ttu-id="8a808-103">在全域範圍或 Api 範圍中建立新診斷。</span><span class="sxs-lookup"><span data-stu-id="8a808-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="8a808-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a808-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a808-105">描述</span><span class="sxs-lookup"><span data-stu-id="8a808-105">DESCRIPTION</span></span>
<span data-ttu-id="8a808-106">Cmdlet **New-AzApiManagementDiagnostic** 會以全域範圍或特定的 Api 範圍建立診斷實體。</span><span class="sxs-lookup"><span data-stu-id="8a808-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="8a808-107">例子</span><span class="sxs-lookup"><span data-stu-id="8a808-107">EXAMPLES</span></span>

### <span data-ttu-id="8a808-108">範例 1：建立新的全域範圍診斷</span><span class="sxs-lookup"><span data-stu-id="8a808-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="8a808-109">此範例在全域範圍中建立診斷實體。</span><span class="sxs-lookup"><span data-stu-id="8a808-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="8a808-110">範例 2：在 Api 範圍中建立診斷</span><span class="sxs-lookup"><span data-stu-id="8a808-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="8a808-111">上述範例會針對 API 建立診斷 `httpbin` ，以記錄要記錄之標頭和 100 位元組的內 `azuremonitor` 體。</span><span class="sxs-lookup"><span data-stu-id="8a808-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="8a808-112">參數</span><span class="sxs-lookup"><span data-stu-id="8a808-112">PARAMETERS</span></span>

### <span data-ttu-id="8a808-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="8a808-113">-AlwaysLog</span></span>
<span data-ttu-id="8a808-114">指定不應使用的郵件抽樣設定類型。</span><span class="sxs-lookup"><span data-stu-id="8a808-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="8a808-115">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="8a808-115">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8a808-116">-ApiId</span></span>
<span data-ttu-id="8a808-117">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a808-117">Identifier of existing API.</span></span>
<span data-ttu-id="8a808-118">如果指定，將會設定 API 範圍策略。</span><span class="sxs-lookup"><span data-stu-id="8a808-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="8a808-119">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="8a808-119">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-120">-後端設定</span><span class="sxs-lookup"><span data-stu-id="8a808-120">-BackendSetting</span></span>
<span data-ttu-id="8a808-121">內建/待發 Http 訊息到後端的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="8a808-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="8a808-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="8a808-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-123">-內容</span><span class="sxs-lookup"><span data-stu-id="8a808-123">-Context</span></span>
<span data-ttu-id="8a808-124">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="8a808-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8a808-125">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="8a808-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a808-126">-DefaultProfile</span></span>
<span data-ttu-id="8a808-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a808-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a808-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="8a808-128">-DiagnosticId</span></span>
<span data-ttu-id="8a808-129">診斷實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a808-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="8a808-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="8a808-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="8a808-131">-FrontEndSetting</span></span>
<span data-ttu-id="8a808-132">內建/待發 Http 訊息到閘道的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="8a808-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="8a808-133">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="8a808-133">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8a808-134">-LoggerId</span></span>
<span data-ttu-id="8a808-135">要推送診斷的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a808-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="8a808-136">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="8a808-136">This parameter is required.</span></span>

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

### <span data-ttu-id="8a808-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8a808-137">-SamplingSetting</span></span>
<span data-ttu-id="8a808-138">診斷的抽樣設定。</span><span class="sxs-lookup"><span data-stu-id="8a808-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="8a808-139">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="8a808-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-140">-確認</span><span class="sxs-lookup"><span data-stu-id="8a808-140">-Confirm</span></span>
<span data-ttu-id="8a808-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8a808-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a808-142">-WhatIf</span></span>
<span data-ttu-id="8a808-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a808-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a808-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a808-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a808-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a808-145">CommonParameters</span></span>
<span data-ttu-id="8a808-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a808-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a808-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a808-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a808-148">輸入</span><span class="sxs-lookup"><span data-stu-id="8a808-148">INPUTS</span></span>

### <span data-ttu-id="8a808-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="8a808-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8a808-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8a808-150">System.String</span></span>

### <span data-ttu-id="8a808-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8a808-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="8a808-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8a808-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="8a808-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8a808-153">OUTPUTS</span></span>

### <span data-ttu-id="8a808-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a808-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="8a808-155">筆記</span><span class="sxs-lookup"><span data-stu-id="8a808-155">NOTES</span></span>

## <span data-ttu-id="8a808-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a808-156">RELATED LINKS</span></span>

[<span data-ttu-id="8a808-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a808-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8a808-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a808-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8a808-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a808-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8a808-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a808-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="8a808-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8a808-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)