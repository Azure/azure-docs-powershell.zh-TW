---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623440"
---
# <span data-ttu-id="688bf-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="688bf-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="688bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="688bf-102">SYNOPSIS</span></span>
<span data-ttu-id="688bf-103">移除特定 Api 版本集</span><span class="sxs-lookup"><span data-stu-id="688bf-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="688bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="688bf-104">SYNTAX</span></span>

### <span data-ttu-id="688bf-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="688bf-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688bf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="688bf-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="688bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="688bf-107">DESCRIPTION</span></span>

<span data-ttu-id="688bf-108">AzureRmApiManagementApiVersionSet Cmdlet 會移除現有 **的** API 版本集。</span><span class="sxs-lookup"><span data-stu-id="688bf-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="688bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="688bf-109">EXAMPLES</span></span>

### <span data-ttu-id="688bf-110">範例1：移除 API 版本集</span><span class="sxs-lookup"><span data-stu-id="688bf-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="688bf-111">這個命令會以指定的 ApiVersionSetId 移除 API 版本設定。</span><span class="sxs-lookup"><span data-stu-id="688bf-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="688bf-112">參數</span><span class="sxs-lookup"><span data-stu-id="688bf-112">PARAMETERS</span></span>

### <span data-ttu-id="688bf-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="688bf-113">-ApiVersionSetId</span></span>
<span data-ttu-id="688bf-114">API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="688bf-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="688bf-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="688bf-115">This parameter is required.</span></span>

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

### <span data-ttu-id="688bf-116">-內容</span><span class="sxs-lookup"><span data-stu-id="688bf-116">-Context</span></span>
<span data-ttu-id="688bf-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="688bf-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="688bf-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="688bf-118">This parameter is required.</span></span>

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

### <span data-ttu-id="688bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="688bf-119">-DefaultProfile</span></span>
<span data-ttu-id="688bf-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="688bf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="688bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="688bf-121">-InputObject</span></span>
<span data-ttu-id="688bf-122">PsApiManagementApiVersionSet 的實例。</span><span class="sxs-lookup"><span data-stu-id="688bf-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="688bf-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="688bf-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="688bf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="688bf-124">-PassThru</span></span>
<span data-ttu-id="688bf-125">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="688bf-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="688bf-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="688bf-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="688bf-127">-確認</span><span class="sxs-lookup"><span data-stu-id="688bf-127">-Confirm</span></span>
<span data-ttu-id="688bf-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="688bf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="688bf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="688bf-129">-WhatIf</span></span>
<span data-ttu-id="688bf-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="688bf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="688bf-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="688bf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="688bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="688bf-132">CommonParameters</span></span>
<span data-ttu-id="688bf-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="688bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="688bf-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="688bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="688bf-135">輸入</span><span class="sxs-lookup"><span data-stu-id="688bf-135">INPUTS</span></span>

### <span data-ttu-id="688bf-136">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="688bf-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="688bf-137">參數：內容 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="688bf-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="688bf-138">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="688bf-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="688bf-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="688bf-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="688bf-140">System.object</span><span class="sxs-lookup"><span data-stu-id="688bf-140">System.String</span></span>

## <span data-ttu-id="688bf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="688bf-141">OUTPUTS</span></span>

### <span data-ttu-id="688bf-142">System.object</span><span class="sxs-lookup"><span data-stu-id="688bf-142">System.Boolean</span></span>

## <span data-ttu-id="688bf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="688bf-143">NOTES</span></span>

## <span data-ttu-id="688bf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="688bf-144">RELATED LINKS</span></span>

[<span data-ttu-id="688bf-145">AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="688bf-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="688bf-146">新-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="688bf-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="688bf-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="688bf-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
