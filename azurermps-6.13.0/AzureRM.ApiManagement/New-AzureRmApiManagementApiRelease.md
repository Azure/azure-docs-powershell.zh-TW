---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: cb7fbfe4ba4fdf09b9012ddc5be8028af0bd80c1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93457696"
---
# <span data-ttu-id="88325-101">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="88325-101">New-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="88325-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88325-102">SYNOPSIS</span></span>
<span data-ttu-id="88325-103">建立 API 版本的 API 發行</span><span class="sxs-lookup"><span data-stu-id="88325-103">Creates an API Release of an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88325-104">句法</span><span class="sxs-lookup"><span data-stu-id="88325-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88325-105">說明</span><span class="sxs-lookup"><span data-stu-id="88325-105">DESCRIPTION</span></span>

<span data-ttu-id="88325-106">**新的-AzureRmApiManagementApiRelease** Cmdlet 會在 api 管理內容中建立 api 版本的 api 發行。</span><span class="sxs-lookup"><span data-stu-id="88325-106">The **New-AzureRmApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="88325-107">示例</span><span class="sxs-lookup"><span data-stu-id="88325-107">EXAMPLES</span></span>

### <span data-ttu-id="88325-108">範例1：建立 API 版本的 API 版本</span><span class="sxs-lookup"><span data-stu-id="88325-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


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

<span data-ttu-id="88325-109">這個命令會建立的 API 發行版本本 `2` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="88325-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="88325-110">參數</span><span class="sxs-lookup"><span data-stu-id="88325-110">PARAMETERS</span></span>

### <span data-ttu-id="88325-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="88325-111">-ApiId</span></span>
<span data-ttu-id="88325-112">新 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88325-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="88325-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="88325-113">-ApiRevision</span></span>
<span data-ttu-id="88325-114">Api 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88325-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="88325-115">-內容</span><span class="sxs-lookup"><span data-stu-id="88325-115">-Context</span></span>
<span data-ttu-id="88325-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="88325-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="88325-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="88325-117">This parameter is required.</span></span>

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

### <span data-ttu-id="88325-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88325-118">-DefaultProfile</span></span>
<span data-ttu-id="88325-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88325-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88325-120">-記事</span><span class="sxs-lookup"><span data-stu-id="88325-120">-Note</span></span>
<span data-ttu-id="88325-121">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="88325-121">Api Release Notes.</span></span> <span data-ttu-id="88325-122">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="88325-122">This parameter is optional</span></span>

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

### <span data-ttu-id="88325-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="88325-123">-ReleaseId</span></span>
<span data-ttu-id="88325-124">Api 發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88325-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="88325-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="88325-125">This parameter is optional.</span></span>
<span data-ttu-id="88325-126">如果未指定識別碼，將會產生。</span><span class="sxs-lookup"><span data-stu-id="88325-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="88325-127">-確認</span><span class="sxs-lookup"><span data-stu-id="88325-127">-Confirm</span></span>
<span data-ttu-id="88325-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88325-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88325-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88325-129">-WhatIf</span></span>
<span data-ttu-id="88325-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88325-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88325-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88325-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88325-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88325-132">CommonParameters</span></span>
<span data-ttu-id="88325-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88325-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88325-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88325-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88325-135">輸入</span><span class="sxs-lookup"><span data-stu-id="88325-135">INPUTS</span></span>

### <span data-ttu-id="88325-136">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="88325-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="88325-137">參數：內容 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="88325-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="88325-138">System.object</span><span class="sxs-lookup"><span data-stu-id="88325-138">System.String</span></span>

## <span data-ttu-id="88325-139">輸出</span><span class="sxs-lookup"><span data-stu-id="88325-139">OUTPUTS</span></span>

### <span data-ttu-id="88325-140">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="88325-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="88325-141">筆記</span><span class="sxs-lookup"><span data-stu-id="88325-141">NOTES</span></span>

## <span data-ttu-id="88325-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="88325-142">RELATED LINKS</span></span>

[<span data-ttu-id="88325-143">AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="88325-143">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="88325-144">移除-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="88325-144">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="88325-145">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="88325-145">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
