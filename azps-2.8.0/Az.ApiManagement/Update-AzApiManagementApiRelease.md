---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 1141d671db13c3ea44a7ed7bd003574f3c13615c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613860"
---
# <span data-ttu-id="a4a15-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a4a15-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="a4a15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4a15-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a15-103">更新特定的 Api 版本。</span><span class="sxs-lookup"><span data-stu-id="a4a15-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="a4a15-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4a15-104">SYNTAX</span></span>

### <span data-ttu-id="a4a15-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="a4a15-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4a15-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a4a15-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4a15-107">說明</span><span class="sxs-lookup"><span data-stu-id="a4a15-107">DESCRIPTION</span></span>
<span data-ttu-id="a4a15-108">**AzApiManagementApiRelease** Cmdlet 會修改 Azure API 管理 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a4a15-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="a4a15-109">示例</span><span class="sxs-lookup"><span data-stu-id="a4a15-109">EXAMPLES</span></span>

### <span data-ttu-id="a4a15-110">範例1：更新 API 版本的 api 發行</span><span class="sxs-lookup"><span data-stu-id="a4a15-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="a4a15-111">這個命令會 `echo-api-release` 使用新的記事來更新 Api 發行 api `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="a4a15-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="a4a15-112">參數</span><span class="sxs-lookup"><span data-stu-id="a4a15-112">PARAMETERS</span></span>

### <span data-ttu-id="a4a15-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a4a15-113">-ApiId</span></span>
<span data-ttu-id="a4a15-114">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4a15-114">Identifier of existing API.</span></span>
<span data-ttu-id="a4a15-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a4a15-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a4a15-116">-內容</span><span class="sxs-lookup"><span data-stu-id="a4a15-116">-Context</span></span>
<span data-ttu-id="a4a15-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="a4a15-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a4a15-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a4a15-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a4a15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a15-119">-DefaultProfile</span></span>
<span data-ttu-id="a4a15-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4a15-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a15-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4a15-121">-InputObject</span></span>
<span data-ttu-id="a4a15-122">ServiceManagement 的 ApiManagement 實例。） PsApiManagementApiRelease）。</span><span class="sxs-lookup"><span data-stu-id="a4a15-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4a15-123">-記事</span><span class="sxs-lookup"><span data-stu-id="a4a15-123">-Note</span></span>
<span data-ttu-id="a4a15-124">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="a4a15-124">Api Release Notes.</span></span>
<span data-ttu-id="a4a15-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a4a15-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4a15-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4a15-126">-PassThru</span></span>
<span data-ttu-id="a4a15-127">如果已指定，則 ServiceManagement PsApiManagementApiRelease 類型的 ApiManagement，代表設定 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a4a15-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4a15-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="a4a15-128">-ReleaseId</span></span>
<span data-ttu-id="a4a15-129">Api Revision ReleaseId 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4a15-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="a4a15-130">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a4a15-130">This parameter is required.</span></span>

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

### <span data-ttu-id="a4a15-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a4a15-131">-Confirm</span></span>
<span data-ttu-id="a4a15-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4a15-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4a15-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4a15-133">-WhatIf</span></span>
<span data-ttu-id="a4a15-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4a15-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4a15-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4a15-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4a15-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a15-136">CommonParameters</span></span>
<span data-ttu-id="a4a15-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4a15-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a15-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4a15-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a15-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a4a15-139">INPUTS</span></span>

### <span data-ttu-id="a4a15-140">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a4a15-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a4a15-141">System.object</span><span class="sxs-lookup"><span data-stu-id="a4a15-141">System.String</span></span>

### <span data-ttu-id="a4a15-142">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a4a15-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a4a15-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a4a15-143">OUTPUTS</span></span>

### <span data-ttu-id="a4a15-144">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a4a15-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a4a15-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a4a15-145">NOTES</span></span>

## <span data-ttu-id="a4a15-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4a15-146">RELATED LINKS</span></span>

[<span data-ttu-id="a4a15-147">AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a4a15-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="a4a15-148">新-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a4a15-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
