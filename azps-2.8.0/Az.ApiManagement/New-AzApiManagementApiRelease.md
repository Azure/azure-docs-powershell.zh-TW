---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5a5d155b8c9127d330a1f53d1fe53d42d60d46a8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406599"
---
# <span data-ttu-id="82207-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="82207-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="82207-102">簡介</span><span class="sxs-lookup"><span data-stu-id="82207-102">SYNOPSIS</span></span>
<span data-ttu-id="82207-103">建立 API 修訂的 API 版本</span><span class="sxs-lookup"><span data-stu-id="82207-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="82207-104">語法</span><span class="sxs-lookup"><span data-stu-id="82207-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82207-105">描述</span><span class="sxs-lookup"><span data-stu-id="82207-105">DESCRIPTION</span></span>

<span data-ttu-id="82207-106">**New-AzApiManagementApiRelease** Cmdlet 會針對 API 管理內容中的 API 修訂建立 API 版本。</span><span class="sxs-lookup"><span data-stu-id="82207-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="82207-107">發行用來將 Api 修訂製作為目前修訂。</span><span class="sxs-lookup"><span data-stu-id="82207-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="82207-108">例子</span><span class="sxs-lookup"><span data-stu-id="82207-108">EXAMPLES</span></span>

### <span data-ttu-id="82207-109">範例 1：建立 API 修訂的 API 版本</span><span class="sxs-lookup"><span data-stu-id="82207-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="82207-110">此命令會建立 API 版本的修訂 `2` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="82207-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="82207-111">參數</span><span class="sxs-lookup"><span data-stu-id="82207-111">PARAMETERS</span></span>

### <span data-ttu-id="82207-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="82207-112">-ApiId</span></span>
<span data-ttu-id="82207-113">新 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="82207-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="82207-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="82207-114">-ApiRevision</span></span>
<span data-ttu-id="82207-115">Api 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="82207-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="82207-116">-內容</span><span class="sxs-lookup"><span data-stu-id="82207-116">-Context</span></span>
<span data-ttu-id="82207-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="82207-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="82207-118">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="82207-118">This parameter is required.</span></span>

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

### <span data-ttu-id="82207-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82207-119">-DefaultProfile</span></span>
<span data-ttu-id="82207-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="82207-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82207-121">-注意</span><span class="sxs-lookup"><span data-stu-id="82207-121">-Note</span></span>
<span data-ttu-id="82207-122">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="82207-122">Api Release Notes.</span></span> <span data-ttu-id="82207-123">此參數為選擇性</span><span class="sxs-lookup"><span data-stu-id="82207-123">This parameter is optional</span></span>

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

### <span data-ttu-id="82207-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="82207-124">-ReleaseId</span></span>
<span data-ttu-id="82207-125">Api 發行識別碼。</span><span class="sxs-lookup"><span data-stu-id="82207-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="82207-126">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="82207-126">This parameter is optional.</span></span>
<span data-ttu-id="82207-127">如果未指定識別碼，將會產生。</span><span class="sxs-lookup"><span data-stu-id="82207-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="82207-128">-確認</span><span class="sxs-lookup"><span data-stu-id="82207-128">-Confirm</span></span>
<span data-ttu-id="82207-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="82207-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82207-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82207-130">-WhatIf</span></span>
<span data-ttu-id="82207-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82207-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82207-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82207-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82207-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82207-133">CommonParameters</span></span>
<span data-ttu-id="82207-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="82207-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82207-135">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82207-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82207-136">輸入</span><span class="sxs-lookup"><span data-stu-id="82207-136">INPUTS</span></span>

### <span data-ttu-id="82207-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="82207-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="82207-138">System.String</span><span class="sxs-lookup"><span data-stu-id="82207-138">System.String</span></span>

## <span data-ttu-id="82207-139">輸出</span><span class="sxs-lookup"><span data-stu-id="82207-139">OUTPUTS</span></span>

### <span data-ttu-id="82207-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="82207-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="82207-141">筆記</span><span class="sxs-lookup"><span data-stu-id="82207-141">NOTES</span></span>

## <span data-ttu-id="82207-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="82207-142">RELATED LINKS</span></span>

[<span data-ttu-id="82207-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="82207-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="82207-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="82207-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="82207-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="82207-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)