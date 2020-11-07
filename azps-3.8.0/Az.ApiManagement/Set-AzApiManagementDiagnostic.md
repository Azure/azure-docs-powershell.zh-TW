---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: f3add9f35e56d4ba6d92b8438b970ddf8c682804
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959799"
---
# <span data-ttu-id="7d934-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7d934-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="7d934-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d934-102">SYNOPSIS</span></span>
<span data-ttu-id="7d934-103">在全域或 Api 範圍修改 API 管理診斷。</span><span class="sxs-lookup"><span data-stu-id="7d934-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="7d934-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d934-104">SYNTAX</span></span>

### <span data-ttu-id="7d934-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="7d934-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d934-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7d934-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d934-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d934-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d934-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d934-108">DESCRIPTION</span></span>
<span data-ttu-id="7d934-109">Cmdlet **AzApiManagementDiagnostic** 會更新在全域或 Api 範圍內設定的診斷。</span><span class="sxs-lookup"><span data-stu-id="7d934-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="7d934-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d934-110">EXAMPLES</span></span>

### <span data-ttu-id="7d934-111">範例1：修改全域範圍中的診斷</span><span class="sxs-lookup"><span data-stu-id="7d934-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="7d934-112">這個命令會將指定的診斷採樣百分比從100修改為50%</span><span class="sxs-lookup"><span data-stu-id="7d934-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="7d934-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d934-113">PARAMETERS</span></span>

### <span data-ttu-id="7d934-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="7d934-114">-AlwaysLog</span></span>
<span data-ttu-id="7d934-115">指定不應套用 [採樣] 設定的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="7d934-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="7d934-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7d934-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d934-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7d934-117">-ApiId</span></span>
<span data-ttu-id="7d934-118">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d934-118">Identifier of existing API.</span></span>
<span data-ttu-id="7d934-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7d934-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d934-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="7d934-120">-BackendSetting</span></span>
<span data-ttu-id="7d934-121">將傳入/傳出 Http 訊息的診斷設定設為後端。</span><span class="sxs-lookup"><span data-stu-id="7d934-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="7d934-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7d934-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d934-123">-內容</span><span class="sxs-lookup"><span data-stu-id="7d934-123">-Context</span></span>
<span data-ttu-id="7d934-124">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="7d934-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7d934-125">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7d934-125">This parameter is required.</span></span>

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

### <span data-ttu-id="7d934-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d934-126">-DefaultProfile</span></span>
<span data-ttu-id="7d934-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d934-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d934-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="7d934-128">-DiagnosticId</span></span>
<span data-ttu-id="7d934-129">現有診斷的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d934-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="7d934-130">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7d934-130">This parameter is required.</span></span>

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

### <span data-ttu-id="7d934-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="7d934-131">-FrontEndSetting</span></span>
<span data-ttu-id="7d934-132">傳入/傳出 Http 訊息的診斷設定至閘道。</span><span class="sxs-lookup"><span data-stu-id="7d934-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="7d934-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7d934-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d934-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d934-134">-InputObject</span></span>
<span data-ttu-id="7d934-135">PsApiManagementDiagnostic 的實例。</span><span class="sxs-lookup"><span data-stu-id="7d934-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="7d934-136">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7d934-136">This parameter is required.</span></span>

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

### <span data-ttu-id="7d934-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="7d934-137">-LoggerId</span></span>
<span data-ttu-id="7d934-138">要將診斷推送至其中的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d934-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="7d934-139">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7d934-139">This parameter is required.</span></span>

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

### <span data-ttu-id="7d934-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d934-140">-PassThru</span></span>
<span data-ttu-id="7d934-141">如果已指定，則 ServiceManagement PsApiManagementDiagnostic 類型的 ApiManagement，代表 set 診斷。</span><span class="sxs-lookup"><span data-stu-id="7d934-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="7d934-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d934-142">-ResourceId</span></span>
<span data-ttu-id="7d934-143">[Arm] 診斷程式或 Api 診斷的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="7d934-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="7d934-144">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7d934-144">This parameter is required.</span></span>

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

### <span data-ttu-id="7d934-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="7d934-145">-SamplingSetting</span></span>
<span data-ttu-id="7d934-146">診斷的採樣設定。</span><span class="sxs-lookup"><span data-stu-id="7d934-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="7d934-147">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7d934-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d934-148">-確認</span><span class="sxs-lookup"><span data-stu-id="7d934-148">-Confirm</span></span>
<span data-ttu-id="7d934-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d934-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d934-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d934-150">-WhatIf</span></span>
<span data-ttu-id="7d934-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d934-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d934-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d934-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d934-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d934-153">CommonParameters</span></span>
<span data-ttu-id="7d934-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d934-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d934-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7d934-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d934-156">輸入</span><span class="sxs-lookup"><span data-stu-id="7d934-156">INPUTS</span></span>

### <span data-ttu-id="7d934-157">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7d934-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7d934-158">System.object</span><span class="sxs-lookup"><span data-stu-id="7d934-158">System.String</span></span>

### <span data-ttu-id="7d934-159">ServiceManagement. PsApiManagementDiagnostic （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7d934-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="7d934-160">ServiceManagement. PsApiManagementSamplingSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7d934-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="7d934-161">ServiceManagement. PsApiManagementPipelineDiagnosticSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7d934-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="7d934-162">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7d934-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d934-163">輸出</span><span class="sxs-lookup"><span data-stu-id="7d934-163">OUTPUTS</span></span>

### <span data-ttu-id="7d934-164">ServiceManagement. PsApiManagementDiagnostic （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7d934-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="7d934-165">筆記</span><span class="sxs-lookup"><span data-stu-id="7d934-165">NOTES</span></span>

## <span data-ttu-id="7d934-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d934-166">RELATED LINKS</span></span>
