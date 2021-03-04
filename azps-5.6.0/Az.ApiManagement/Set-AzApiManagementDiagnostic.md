---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c9cb592713f7a24739651d36855fdf595ffc7eeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905278"
---
# <span data-ttu-id="6bbcc-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bbcc-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="6bbcc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6bbcc-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbcc-103">在全域或 Api 範圍中修改 API 管理診斷。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="6bbcc-104">語法</span><span class="sxs-lookup"><span data-stu-id="6bbcc-104">SYNTAX</span></span>

### <span data-ttu-id="6bbcc-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="6bbcc-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bbcc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6bbcc-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bbcc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bbcc-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bbcc-108">描述</span><span class="sxs-lookup"><span data-stu-id="6bbcc-108">DESCRIPTION</span></span>
<span data-ttu-id="6bbcc-109">Cmdlet **Set-AzApiManagementDiagnostic** 會更新全域或 Api 範圍中設定診斷。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="6bbcc-110">例子</span><span class="sxs-lookup"><span data-stu-id="6bbcc-110">EXAMPLES</span></span>

### <span data-ttu-id="6bbcc-111">範例 1：在全域範圍中修改診斷</span><span class="sxs-lookup"><span data-stu-id="6bbcc-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="6bbcc-112">此命令會修改指定的診斷抽樣百分比，從 100% 到 50%</span><span class="sxs-lookup"><span data-stu-id="6bbcc-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="6bbcc-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="6bbcc-113">Example 2</span></span>

<span data-ttu-id="6bbcc-114">在全域或 Api 範圍中修改 API 管理診斷。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="6bbcc-115"> (自動) </span><span class="sxs-lookup"><span data-stu-id="6bbcc-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="6bbcc-116">參數</span><span class="sxs-lookup"><span data-stu-id="6bbcc-116">PARAMETERS</span></span>

### <span data-ttu-id="6bbcc-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="6bbcc-117">-AlwaysLog</span></span>
<span data-ttu-id="6bbcc-118">指定不應使用的郵件抽樣設定類型。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="6bbcc-119">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bbcc-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6bbcc-120">-ApiId</span></span>
<span data-ttu-id="6bbcc-121">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-121">Identifier of existing API.</span></span>
<span data-ttu-id="6bbcc-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbcc-123">-後端設定</span><span class="sxs-lookup"><span data-stu-id="6bbcc-123">-BackendSetting</span></span>
<span data-ttu-id="6bbcc-124">內建/待發 Http 訊息到後端的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="6bbcc-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bbcc-126">-內容</span><span class="sxs-lookup"><span data-stu-id="6bbcc-126">-Context</span></span>
<span data-ttu-id="6bbcc-127">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6bbcc-128">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbcc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbcc-129">-DefaultProfile</span></span>
<span data-ttu-id="6bbcc-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bbcc-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="6bbcc-131">-DiagnosticId</span></span>
<span data-ttu-id="6bbcc-132">現有診斷的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="6bbcc-133">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbcc-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="6bbcc-134">-FrontEndSetting</span></span>
<span data-ttu-id="6bbcc-135">內建/待發 Http 訊息到閘道的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="6bbcc-136">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bbcc-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bbcc-137">-InputObject</span></span>
<span data-ttu-id="6bbcc-138">PsApiManagementDiagnostic 的實例。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="6bbcc-139">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbcc-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="6bbcc-140">-LoggerId</span></span>
<span data-ttu-id="6bbcc-141">要推送診斷的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="6bbcc-142">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-142">This parameter is required.</span></span>

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

### <span data-ttu-id="6bbcc-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bbcc-143">-PassThru</span></span>
<span data-ttu-id="6bbcc-144">如果指定的話，代表診斷集的 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic 類型實例。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbcc-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bbcc-145">-ResourceId</span></span>
<span data-ttu-id="6bbcc-146">診斷或 Api 診斷的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="6bbcc-147">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bbcc-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="6bbcc-148">-SamplingSetting</span></span>
<span data-ttu-id="6bbcc-149">診斷的抽樣設定。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="6bbcc-150">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="6bbcc-151">-確認</span><span class="sxs-lookup"><span data-stu-id="6bbcc-151">-Confirm</span></span>
<span data-ttu-id="6bbcc-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bbcc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bbcc-153">-WhatIf</span></span>
<span data-ttu-id="6bbcc-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bbcc-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bbcc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbcc-156">CommonParameters</span></span>
<span data-ttu-id="6bbcc-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6bbcc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbcc-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bbcc-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbcc-159">輸入</span><span class="sxs-lookup"><span data-stu-id="6bbcc-159">INPUTS</span></span>

### <span data-ttu-id="6bbcc-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="6bbcc-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6bbcc-161">System.String</span><span class="sxs-lookup"><span data-stu-id="6bbcc-161">System.String</span></span>

### <span data-ttu-id="6bbcc-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bbcc-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="6bbcc-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="6bbcc-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="6bbcc-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6bbcc-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="6bbcc-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bbcc-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bbcc-166">輸出</span><span class="sxs-lookup"><span data-stu-id="6bbcc-166">OUTPUTS</span></span>

### <span data-ttu-id="6bbcc-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6bbcc-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="6bbcc-168">筆記</span><span class="sxs-lookup"><span data-stu-id="6bbcc-168">NOTES</span></span>

## <span data-ttu-id="6bbcc-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bbcc-169">RELATED LINKS</span></span>
