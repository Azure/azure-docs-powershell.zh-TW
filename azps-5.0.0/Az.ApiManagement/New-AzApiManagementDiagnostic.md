---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139323"
---
# <span data-ttu-id="20b04-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20b04-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="20b04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20b04-102">SYNOPSIS</span></span>
<span data-ttu-id="20b04-103">在全域範圍或 Api 範圍中建立新的診斷。</span><span class="sxs-lookup"><span data-stu-id="20b04-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="20b04-104">句法</span><span class="sxs-lookup"><span data-stu-id="20b04-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b04-105">說明</span><span class="sxs-lookup"><span data-stu-id="20b04-105">DESCRIPTION</span></span>
<span data-ttu-id="20b04-106">Cmdlet **AzApiManagementDiagnostic** 會建立全域範圍或特定 Api 範圍中的診斷實體。</span><span class="sxs-lookup"><span data-stu-id="20b04-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="20b04-107">示例</span><span class="sxs-lookup"><span data-stu-id="20b04-107">EXAMPLES</span></span>

### <span data-ttu-id="20b04-108">範例1：建立新的全域範圍診斷</span><span class="sxs-lookup"><span data-stu-id="20b04-108">Example 1: Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="20b04-109">這個範例會在全域範圍中建立診斷實體。</span><span class="sxs-lookup"><span data-stu-id="20b04-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="20b04-110">範例2：在 Api 範圍建立診斷</span><span class="sxs-lookup"><span data-stu-id="20b04-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="20b04-111">上述範例會建立 API 的診斷程式，以將本文的 `httpbin` 標頭與100位元組記錄在 `azuremonitor` 記錄器中。</span><span class="sxs-lookup"><span data-stu-id="20b04-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="20b04-112">參數</span><span class="sxs-lookup"><span data-stu-id="20b04-112">PARAMETERS</span></span>

### <span data-ttu-id="20b04-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="20b04-113">-AlwaysLog</span></span>
<span data-ttu-id="20b04-114">指定不應套用 [採樣] 設定的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="20b04-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="20b04-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="20b04-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="20b04-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="20b04-116">-ApiId</span></span>
<span data-ttu-id="20b04-117">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20b04-117">Identifier of existing API.</span></span>
<span data-ttu-id="20b04-118">如果已指定，將會設定 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="20b04-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="20b04-119">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="20b04-119">This parameters is required.</span></span>

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

### <span data-ttu-id="20b04-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="20b04-120">-BackendSetting</span></span>
<span data-ttu-id="20b04-121">將傳入/傳出 Http 訊息的診斷設定設為後端。</span><span class="sxs-lookup"><span data-stu-id="20b04-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="20b04-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="20b04-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="20b04-123">-內容</span><span class="sxs-lookup"><span data-stu-id="20b04-123">-Context</span></span>
<span data-ttu-id="20b04-124">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="20b04-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="20b04-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="20b04-125">This parameter is required.</span></span>

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

### <span data-ttu-id="20b04-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b04-126">-DefaultProfile</span></span>
<span data-ttu-id="20b04-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20b04-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b04-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="20b04-128">-DiagnosticId</span></span>
<span data-ttu-id="20b04-129">診斷實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20b04-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="20b04-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="20b04-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="20b04-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="20b04-131">-FrontEndSetting</span></span>
<span data-ttu-id="20b04-132">傳入/傳出 Http 訊息的診斷設定至閘道。</span><span class="sxs-lookup"><span data-stu-id="20b04-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="20b04-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="20b04-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="20b04-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="20b04-134">-LoggerId</span></span>
<span data-ttu-id="20b04-135">要將診斷推送至其中的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="20b04-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="20b04-136">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="20b04-136">This parameter is required.</span></span>

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

### <span data-ttu-id="20b04-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="20b04-137">-SamplingSetting</span></span>
<span data-ttu-id="20b04-138">診斷的採樣設定。</span><span class="sxs-lookup"><span data-stu-id="20b04-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="20b04-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="20b04-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="20b04-140">-確認</span><span class="sxs-lookup"><span data-stu-id="20b04-140">-Confirm</span></span>
<span data-ttu-id="20b04-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20b04-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b04-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b04-142">-WhatIf</span></span>
<span data-ttu-id="20b04-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20b04-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b04-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20b04-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b04-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b04-145">CommonParameters</span></span>
<span data-ttu-id="20b04-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20b04-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b04-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="20b04-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b04-148">輸入</span><span class="sxs-lookup"><span data-stu-id="20b04-148">INPUTS</span></span>

### <span data-ttu-id="20b04-149">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="20b04-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20b04-150">System.object</span><span class="sxs-lookup"><span data-stu-id="20b04-150">System.String</span></span>

### <span data-ttu-id="20b04-151">ServiceManagement. PsApiManagementSamplingSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="20b04-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="20b04-152">ServiceManagement. PsApiManagementPipelineDiagnosticSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="20b04-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="20b04-153">輸出</span><span class="sxs-lookup"><span data-stu-id="20b04-153">OUTPUTS</span></span>

### <span data-ttu-id="20b04-154">ServiceManagement. PsApiManagementDiagnostic （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="20b04-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="20b04-155">筆記</span><span class="sxs-lookup"><span data-stu-id="20b04-155">NOTES</span></span>

## <span data-ttu-id="20b04-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="20b04-156">RELATED LINKS</span></span>

[<span data-ttu-id="20b04-157">AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20b04-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="20b04-158">移除-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20b04-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="20b04-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20b04-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="20b04-160">新-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20b04-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="20b04-161">新-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="20b04-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)