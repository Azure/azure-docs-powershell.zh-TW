---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 784480b56a868f84f8f79a35bf7ab2c1ba2e9fbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614015"
---
# <span data-ttu-id="3f864-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3f864-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="3f864-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f864-102">SYNOPSIS</span></span>
<span data-ttu-id="3f864-103">建立 API 版本的 API 發行</span><span class="sxs-lookup"><span data-stu-id="3f864-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="3f864-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f864-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f864-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f864-105">DESCRIPTION</span></span>

<span data-ttu-id="3f864-106">**新的-AzApiManagementApiRelease** Cmdlet 會在 api 管理內容中建立 api 版本的 api 發行。</span><span class="sxs-lookup"><span data-stu-id="3f864-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="3f864-107">發行版本是用來將 Api 修訂設為目前的修正版本。</span><span class="sxs-lookup"><span data-stu-id="3f864-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="3f864-108">示例</span><span class="sxs-lookup"><span data-stu-id="3f864-108">EXAMPLES</span></span>

### <span data-ttu-id="3f864-109">範例1：建立 API 版本的 API 版本</span><span class="sxs-lookup"><span data-stu-id="3f864-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="3f864-110">這個命令會建立的 API 發行版本本 `2` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="3f864-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="3f864-111">參數</span><span class="sxs-lookup"><span data-stu-id="3f864-111">PARAMETERS</span></span>

### <span data-ttu-id="3f864-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3f864-112">-ApiId</span></span>
<span data-ttu-id="3f864-113">新 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f864-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="3f864-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3f864-114">-ApiRevision</span></span>
<span data-ttu-id="3f864-115">Api 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f864-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="3f864-116">-內容</span><span class="sxs-lookup"><span data-stu-id="3f864-116">-Context</span></span>
<span data-ttu-id="3f864-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="3f864-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3f864-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="3f864-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3f864-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f864-119">-DefaultProfile</span></span>
<span data-ttu-id="3f864-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f864-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f864-121">-記事</span><span class="sxs-lookup"><span data-stu-id="3f864-121">-Note</span></span>
<span data-ttu-id="3f864-122">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="3f864-122">Api Release Notes.</span></span> <span data-ttu-id="3f864-123">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="3f864-123">This parameter is optional</span></span>

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

### <span data-ttu-id="3f864-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="3f864-124">-ReleaseId</span></span>
<span data-ttu-id="3f864-125">Api 發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f864-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="3f864-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3f864-126">This parameter is optional.</span></span>
<span data-ttu-id="3f864-127">如果未指定識別碼，將會產生。</span><span class="sxs-lookup"><span data-stu-id="3f864-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="3f864-128">-確認</span><span class="sxs-lookup"><span data-stu-id="3f864-128">-Confirm</span></span>
<span data-ttu-id="3f864-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3f864-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f864-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f864-130">-WhatIf</span></span>
<span data-ttu-id="3f864-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f864-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f864-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f864-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f864-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f864-133">CommonParameters</span></span>
<span data-ttu-id="3f864-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f864-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f864-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3f864-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f864-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3f864-136">INPUTS</span></span>

### <span data-ttu-id="3f864-137">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3f864-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3f864-138">System.object</span><span class="sxs-lookup"><span data-stu-id="3f864-138">System.String</span></span>

## <span data-ttu-id="3f864-139">輸出</span><span class="sxs-lookup"><span data-stu-id="3f864-139">OUTPUTS</span></span>

### <span data-ttu-id="3f864-140">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3f864-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="3f864-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3f864-141">NOTES</span></span>

## <span data-ttu-id="3f864-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f864-142">RELATED LINKS</span></span>

[<span data-ttu-id="3f864-143">AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3f864-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="3f864-144">移除-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3f864-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="3f864-145">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3f864-145">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)