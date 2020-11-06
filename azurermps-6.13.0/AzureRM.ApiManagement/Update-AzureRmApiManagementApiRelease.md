---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445783"
---
# <span data-ttu-id="bcc22-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bcc22-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="bcc22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcc22-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc22-103">更新特定的 Api 版本。</span><span class="sxs-lookup"><span data-stu-id="bcc22-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcc22-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcc22-104">SYNTAX</span></span>

### <span data-ttu-id="bcc22-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="bcc22-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcc22-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bcc22-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc22-107">說明</span><span class="sxs-lookup"><span data-stu-id="bcc22-107">DESCRIPTION</span></span>
<span data-ttu-id="bcc22-108">**AzureRmApiManagementApiRelease** Cmdlet 會修改 Azure API 管理 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bcc22-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="bcc22-109">示例</span><span class="sxs-lookup"><span data-stu-id="bcc22-109">EXAMPLES</span></span>

### <span data-ttu-id="bcc22-110">範例1：更新 API 版本的 api 發行</span><span class="sxs-lookup"><span data-stu-id="bcc22-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="bcc22-111">這個命令會 `echo-api-release` 使用新的記事來更新 Api 發行 api `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="bcc22-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="bcc22-112">參數</span><span class="sxs-lookup"><span data-stu-id="bcc22-112">PARAMETERS</span></span>

### <span data-ttu-id="bcc22-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bcc22-113">-ApiId</span></span>
<span data-ttu-id="bcc22-114">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcc22-114">Identifier of existing API.</span></span>
<span data-ttu-id="bcc22-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="bcc22-115">This parameter is required.</span></span>

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

### <span data-ttu-id="bcc22-116">-內容</span><span class="sxs-lookup"><span data-stu-id="bcc22-116">-Context</span></span>
<span data-ttu-id="bcc22-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="bcc22-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bcc22-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="bcc22-118">This parameter is required.</span></span>

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

### <span data-ttu-id="bcc22-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc22-119">-DefaultProfile</span></span>
<span data-ttu-id="bcc22-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcc22-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc22-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcc22-121">-InputObject</span></span>
<span data-ttu-id="bcc22-122">ServiceManagement 的 ApiManagement 實例。） PsApiManagementApiRelease）。</span><span class="sxs-lookup"><span data-stu-id="bcc22-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="bcc22-123">-記事</span><span class="sxs-lookup"><span data-stu-id="bcc22-123">-Note</span></span>
<span data-ttu-id="bcc22-124">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="bcc22-124">Api Release Notes.</span></span>
<span data-ttu-id="bcc22-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="bcc22-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="bcc22-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcc22-126">-PassThru</span></span>
<span data-ttu-id="bcc22-127">如果已指定，則 ServiceManagement PsApiManagementApiRelease 類型的 ApiManagement，代表設定 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bcc22-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="bcc22-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="bcc22-128">-ReleaseId</span></span>
<span data-ttu-id="bcc22-129">Api Revision ReleaseId 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcc22-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="bcc22-130">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="bcc22-130">This parameter is required.</span></span>

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

### <span data-ttu-id="bcc22-131">-確認</span><span class="sxs-lookup"><span data-stu-id="bcc22-131">-Confirm</span></span>
<span data-ttu-id="bcc22-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bcc22-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc22-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc22-133">-WhatIf</span></span>
<span data-ttu-id="bcc22-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcc22-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcc22-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcc22-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc22-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc22-136">CommonParameters</span></span>
<span data-ttu-id="bcc22-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcc22-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc22-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcc22-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc22-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bcc22-139">INPUTS</span></span>

### <span data-ttu-id="bcc22-140">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bcc22-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="bcc22-141">參數：內容 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bcc22-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="bcc22-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bcc22-142">System.String</span></span>

### <span data-ttu-id="bcc22-143">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bcc22-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="bcc22-144">輸出</span><span class="sxs-lookup"><span data-stu-id="bcc22-144">OUTPUTS</span></span>

### <span data-ttu-id="bcc22-145">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bcc22-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="bcc22-146">筆記</span><span class="sxs-lookup"><span data-stu-id="bcc22-146">NOTES</span></span>

## <span data-ttu-id="bcc22-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcc22-147">RELATED LINKS</span></span>

[<span data-ttu-id="bcc22-148">AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bcc22-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="bcc22-149">新-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bcc22-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
