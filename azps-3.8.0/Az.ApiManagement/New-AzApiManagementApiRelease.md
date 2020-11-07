---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 9b2b94fbd6a308f9d927483e78e060a273354738
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966444"
---
# <span data-ttu-id="d0f1d-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d0f1d-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="d0f1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f1d-103">建立 API 版本的 API 發行</span><span class="sxs-lookup"><span data-stu-id="d0f1d-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="d0f1d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0f1d-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0f1d-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0f1d-105">DESCRIPTION</span></span>

<span data-ttu-id="d0f1d-106">**新的-AzApiManagementApiRelease** Cmdlet 會在 api 管理內容中建立 api 版本的 api 發行。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="d0f1d-107">發行版本是用來將 Api 修訂設為目前的修正版本。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="d0f1d-108">示例</span><span class="sxs-lookup"><span data-stu-id="d0f1d-108">EXAMPLES</span></span>

### <span data-ttu-id="d0f1d-109">範例1：建立 API 版本的 API 版本</span><span class="sxs-lookup"><span data-stu-id="d0f1d-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="d0f1d-110">這個命令會建立的 API 發行版本本 `2` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="d0f1d-111">參數</span><span class="sxs-lookup"><span data-stu-id="d0f1d-111">PARAMETERS</span></span>

### <span data-ttu-id="d0f1d-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d0f1d-112">-ApiId</span></span>
<span data-ttu-id="d0f1d-113">新 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="d0f1d-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d0f1d-114">-ApiRevision</span></span>
<span data-ttu-id="d0f1d-115">Api 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="d0f1d-116">-內容</span><span class="sxs-lookup"><span data-stu-id="d0f1d-116">-Context</span></span>
<span data-ttu-id="d0f1d-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d0f1d-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d0f1d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f1d-119">-DefaultProfile</span></span>
<span data-ttu-id="d0f1d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f1d-121">-記事</span><span class="sxs-lookup"><span data-stu-id="d0f1d-121">-Note</span></span>
<span data-ttu-id="d0f1d-122">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-122">Api Release Notes.</span></span> <span data-ttu-id="d0f1d-123">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-123">This parameter is optional</span></span>

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

### <span data-ttu-id="d0f1d-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="d0f1d-124">-ReleaseId</span></span>
<span data-ttu-id="d0f1d-125">Api 發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="d0f1d-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-126">This parameter is optional.</span></span>
<span data-ttu-id="d0f1d-127">如果未指定識別碼，將會產生。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="d0f1d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d0f1d-128">-Confirm</span></span>
<span data-ttu-id="d0f1d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f1d-130">-WhatIf</span></span>
<span data-ttu-id="d0f1d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0f1d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f1d-133">CommonParameters</span></span>
<span data-ttu-id="d0f1d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f1d-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d0f1d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f1d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d0f1d-136">INPUTS</span></span>

### <span data-ttu-id="d0f1d-137">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d0f1d-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0f1d-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d0f1d-138">System.String</span></span>

## <span data-ttu-id="d0f1d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d0f1d-139">OUTPUTS</span></span>

### <span data-ttu-id="d0f1d-140">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d0f1d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="d0f1d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d0f1d-141">NOTES</span></span>

## <span data-ttu-id="d0f1d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0f1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0f1d-143">AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d0f1d-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="d0f1d-144">移除-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d0f1d-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="d0f1d-145">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d0f1d-145">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)