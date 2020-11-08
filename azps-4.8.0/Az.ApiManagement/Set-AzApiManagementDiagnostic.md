---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969981"
---
# <span data-ttu-id="fb562-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fb562-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="fb562-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb562-102">SYNOPSIS</span></span>
<span data-ttu-id="fb562-103">在全域或 Api 範圍修改 API 管理診斷。</span><span class="sxs-lookup"><span data-stu-id="fb562-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="fb562-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb562-104">SYNTAX</span></span>

### <span data-ttu-id="fb562-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="fb562-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb562-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb562-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb562-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb562-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb562-108">說明</span><span class="sxs-lookup"><span data-stu-id="fb562-108">DESCRIPTION</span></span>
<span data-ttu-id="fb562-109">Cmdlet **AzApiManagementDiagnostic** 會更新在全域或 Api 範圍內設定的診斷。</span><span class="sxs-lookup"><span data-stu-id="fb562-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="fb562-110">示例</span><span class="sxs-lookup"><span data-stu-id="fb562-110">EXAMPLES</span></span>

### <span data-ttu-id="fb562-111">範例1：修改全域範圍中的診斷</span><span class="sxs-lookup"><span data-stu-id="fb562-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="fb562-112">這個命令會將指定的診斷採樣百分比從100修改為50%</span><span class="sxs-lookup"><span data-stu-id="fb562-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="fb562-113">範例2</span><span class="sxs-lookup"><span data-stu-id="fb562-113">Example 2</span></span>

<span data-ttu-id="fb562-114">在全域或 Api 範圍修改 API 管理診斷。</span><span class="sxs-lookup"><span data-stu-id="fb562-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="fb562-115"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="fb562-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="fb562-116">參數</span><span class="sxs-lookup"><span data-stu-id="fb562-116">PARAMETERS</span></span>

### <span data-ttu-id="fb562-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="fb562-117">-AlwaysLog</span></span>
<span data-ttu-id="fb562-118">指定不應套用 [採樣] 設定的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="fb562-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="fb562-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fb562-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb562-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fb562-120">-ApiId</span></span>
<span data-ttu-id="fb562-121">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb562-121">Identifier of existing API.</span></span>
<span data-ttu-id="fb562-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fb562-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb562-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="fb562-123">-BackendSetting</span></span>
<span data-ttu-id="fb562-124">將傳入/傳出 Http 訊息的診斷設定設為後端。</span><span class="sxs-lookup"><span data-stu-id="fb562-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="fb562-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fb562-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb562-126">-內容</span><span class="sxs-lookup"><span data-stu-id="fb562-126">-Context</span></span>
<span data-ttu-id="fb562-127">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="fb562-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fb562-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fb562-128">This parameter is required.</span></span>

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

### <span data-ttu-id="fb562-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb562-129">-DefaultProfile</span></span>
<span data-ttu-id="fb562-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb562-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb562-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="fb562-131">-DiagnosticId</span></span>
<span data-ttu-id="fb562-132">現有診斷的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb562-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="fb562-133">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fb562-133">This parameter is required.</span></span>

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

### <span data-ttu-id="fb562-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="fb562-134">-FrontEndSetting</span></span>
<span data-ttu-id="fb562-135">傳入/傳出 Http 訊息的診斷設定至閘道。</span><span class="sxs-lookup"><span data-stu-id="fb562-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="fb562-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fb562-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb562-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb562-137">-InputObject</span></span>
<span data-ttu-id="fb562-138">PsApiManagementDiagnostic 的實例。</span><span class="sxs-lookup"><span data-stu-id="fb562-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="fb562-139">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fb562-139">This parameter is required.</span></span>

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

### <span data-ttu-id="fb562-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="fb562-140">-LoggerId</span></span>
<span data-ttu-id="fb562-141">要將診斷推送至其中的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb562-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="fb562-142">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fb562-142">This parameter is required.</span></span>

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

### <span data-ttu-id="fb562-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb562-143">-PassThru</span></span>
<span data-ttu-id="fb562-144">如果已指定，則 ServiceManagement PsApiManagementDiagnostic 類型的 ApiManagement，代表 set 診斷。</span><span class="sxs-lookup"><span data-stu-id="fb562-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="fb562-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb562-145">-ResourceId</span></span>
<span data-ttu-id="fb562-146">[Arm] 診斷程式或 Api 診斷的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="fb562-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="fb562-147">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fb562-147">This parameter is required.</span></span>

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

### <span data-ttu-id="fb562-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="fb562-148">-SamplingSetting</span></span>
<span data-ttu-id="fb562-149">診斷的採樣設定。</span><span class="sxs-lookup"><span data-stu-id="fb562-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="fb562-150">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fb562-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb562-151">-確認</span><span class="sxs-lookup"><span data-stu-id="fb562-151">-Confirm</span></span>
<span data-ttu-id="fb562-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb562-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb562-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb562-153">-WhatIf</span></span>
<span data-ttu-id="fb562-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb562-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb562-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb562-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb562-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb562-156">CommonParameters</span></span>
<span data-ttu-id="fb562-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb562-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb562-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb562-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb562-159">輸入</span><span class="sxs-lookup"><span data-stu-id="fb562-159">INPUTS</span></span>

### <span data-ttu-id="fb562-160">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fb562-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fb562-161">System.object</span><span class="sxs-lookup"><span data-stu-id="fb562-161">System.String</span></span>

### <span data-ttu-id="fb562-162">ServiceManagement. PsApiManagementDiagnostic （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fb562-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="fb562-163">ServiceManagement. PsApiManagementSamplingSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fb562-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="fb562-164">ServiceManagement. PsApiManagementPipelineDiagnosticSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fb562-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="fb562-165">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fb562-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb562-166">輸出</span><span class="sxs-lookup"><span data-stu-id="fb562-166">OUTPUTS</span></span>

### <span data-ttu-id="fb562-167">ServiceManagement. PsApiManagementDiagnostic （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fb562-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="fb562-168">筆記</span><span class="sxs-lookup"><span data-stu-id="fb562-168">NOTES</span></span>

## <span data-ttu-id="fb562-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb562-169">RELATED LINKS</span></span>