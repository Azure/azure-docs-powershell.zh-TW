---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444143"
---
# <span data-ttu-id="8952b-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8952b-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="8952b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8952b-102">SYNOPSIS</span></span>
<span data-ttu-id="8952b-103">已移除特定的 API 修訂版本</span><span class="sxs-lookup"><span data-stu-id="8952b-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8952b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8952b-104">SYNTAX</span></span>

### <span data-ttu-id="8952b-105">ByApiId (預設) </span><span class="sxs-lookup"><span data-stu-id="8952b-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8952b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8952b-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8952b-107">說明</span><span class="sxs-lookup"><span data-stu-id="8952b-107">DESCRIPTION</span></span>
<span data-ttu-id="8952b-108">Cmdlet **移除-AzureRmApiManagementApiRevision** 會移除特定的 API 修訂版本。</span><span class="sxs-lookup"><span data-stu-id="8952b-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="8952b-109">示例</span><span class="sxs-lookup"><span data-stu-id="8952b-109">EXAMPLES</span></span>

### <span data-ttu-id="8952b-110">範例1：移除 API 修訂</span><span class="sxs-lookup"><span data-stu-id="8952b-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="8952b-111">這個命令會 `2` `echo-api` 從 api 管理服務移除 api 的修訂版本。</span><span class="sxs-lookup"><span data-stu-id="8952b-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="8952b-112">參數</span><span class="sxs-lookup"><span data-stu-id="8952b-112">PARAMETERS</span></span>

### <span data-ttu-id="8952b-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8952b-113">-ApiId</span></span>
<span data-ttu-id="8952b-114">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8952b-114">Identifier of the API.</span></span>
<span data-ttu-id="8952b-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8952b-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8952b-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8952b-116">-ApiRevision</span></span>
<span data-ttu-id="8952b-117">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8952b-117">Identifier of the API Revision.</span></span> <span data-ttu-id="8952b-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8952b-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8952b-119">-內容</span><span class="sxs-lookup"><span data-stu-id="8952b-119">-Context</span></span>
<span data-ttu-id="8952b-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="8952b-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8952b-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8952b-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8952b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8952b-122">-DefaultProfile</span></span>
<span data-ttu-id="8952b-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8952b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8952b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8952b-124">-InputObject</span></span>
<span data-ttu-id="8952b-125">PsApiManagementApiRelease 的實例。</span><span class="sxs-lookup"><span data-stu-id="8952b-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="8952b-126">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8952b-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8952b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8952b-127">-PassThru</span></span>
<span data-ttu-id="8952b-128">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="8952b-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="8952b-129">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="8952b-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="8952b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8952b-130">-Confirm</span></span>
<span data-ttu-id="8952b-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8952b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8952b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8952b-132">-WhatIf</span></span>
<span data-ttu-id="8952b-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8952b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8952b-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8952b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8952b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8952b-135">CommonParameters</span></span>
<span data-ttu-id="8952b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8952b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8952b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8952b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8952b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8952b-138">INPUTS</span></span>

### <span data-ttu-id="8952b-139">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8952b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8952b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8952b-140">System.String</span></span>

### <span data-ttu-id="8952b-141">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8952b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="8952b-142">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="8952b-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8952b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="8952b-143">OUTPUTS</span></span>

### <span data-ttu-id="8952b-144">System.object</span><span class="sxs-lookup"><span data-stu-id="8952b-144">System.Boolean</span></span>

## <span data-ttu-id="8952b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8952b-145">NOTES</span></span>

## <span data-ttu-id="8952b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="8952b-146">RELATED LINKS</span></span>

[<span data-ttu-id="8952b-147">AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8952b-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="8952b-148">新-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8952b-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="8952b-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8952b-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
