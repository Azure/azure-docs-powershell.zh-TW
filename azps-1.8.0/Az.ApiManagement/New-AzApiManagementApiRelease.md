---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611589"
---
# <span data-ttu-id="3d193-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3d193-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="3d193-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d193-102">SYNOPSIS</span></span>
<span data-ttu-id="3d193-103">建立 API 版本的 API 發行</span><span class="sxs-lookup"><span data-stu-id="3d193-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="3d193-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d193-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d193-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d193-105">DESCRIPTION</span></span>

<span data-ttu-id="3d193-106">**新的-AzApiManagementApiRelease** Cmdlet 會在 api 管理內容中建立 api 版本的 api 發行。</span><span class="sxs-lookup"><span data-stu-id="3d193-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="3d193-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d193-107">EXAMPLES</span></span>

### <span data-ttu-id="3d193-108">範例1：建立 API 版本的 API 版本</span><span class="sxs-lookup"><span data-stu-id="3d193-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="3d193-109">這個命令會建立的 API 發行版本本 `2` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="3d193-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="3d193-110">參數</span><span class="sxs-lookup"><span data-stu-id="3d193-110">PARAMETERS</span></span>

### <span data-ttu-id="3d193-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3d193-111">-ApiId</span></span>
<span data-ttu-id="3d193-112">新 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d193-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="3d193-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3d193-113">-ApiRevision</span></span>
<span data-ttu-id="3d193-114">Api 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d193-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="3d193-115">-內容</span><span class="sxs-lookup"><span data-stu-id="3d193-115">-Context</span></span>
<span data-ttu-id="3d193-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="3d193-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3d193-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="3d193-117">This parameter is required.</span></span>

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

### <span data-ttu-id="3d193-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d193-118">-DefaultProfile</span></span>
<span data-ttu-id="3d193-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d193-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d193-120">-記事</span><span class="sxs-lookup"><span data-stu-id="3d193-120">-Note</span></span>
<span data-ttu-id="3d193-121">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="3d193-121">Api Release Notes.</span></span> <span data-ttu-id="3d193-122">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="3d193-122">This parameter is optional</span></span>

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

### <span data-ttu-id="3d193-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="3d193-123">-ReleaseId</span></span>
<span data-ttu-id="3d193-124">Api 發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d193-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="3d193-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3d193-125">This parameter is optional.</span></span>
<span data-ttu-id="3d193-126">如果未指定識別碼，將會產生。</span><span class="sxs-lookup"><span data-stu-id="3d193-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="3d193-127">-確認</span><span class="sxs-lookup"><span data-stu-id="3d193-127">-Confirm</span></span>
<span data-ttu-id="3d193-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d193-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d193-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d193-129">-WhatIf</span></span>
<span data-ttu-id="3d193-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d193-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d193-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d193-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d193-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d193-132">CommonParameters</span></span>
<span data-ttu-id="3d193-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d193-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d193-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d193-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d193-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3d193-135">INPUTS</span></span>

### <span data-ttu-id="3d193-136">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3d193-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d193-137">System.object</span><span class="sxs-lookup"><span data-stu-id="3d193-137">System.String</span></span>

## <span data-ttu-id="3d193-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3d193-138">OUTPUTS</span></span>

### <span data-ttu-id="3d193-139">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3d193-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="3d193-140">筆記</span><span class="sxs-lookup"><span data-stu-id="3d193-140">NOTES</span></span>

## <span data-ttu-id="3d193-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d193-141">RELATED LINKS</span></span>

[<span data-ttu-id="3d193-142">AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3d193-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="3d193-143">移除-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3d193-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="3d193-144">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3d193-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)