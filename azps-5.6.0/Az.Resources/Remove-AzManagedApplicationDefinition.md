---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 285acdcd7e913d4fb502fb656057f1fc81d6dfcd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905858"
---
# <span data-ttu-id="2e625-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="2e625-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="2e625-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2e625-102">SYNOPSIS</span></span>
<span data-ttu-id="2e625-103">移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="2e625-103">Removes a managed application definition</span></span>

## <span data-ttu-id="2e625-104">語法</span><span class="sxs-lookup"><span data-stu-id="2e625-104">SYNTAX</span></span>

### <span data-ttu-id="2e625-105">RemoveByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="2e625-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e625-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="2e625-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e625-107">描述</span><span class="sxs-lookup"><span data-stu-id="2e625-107">DESCRIPTION</span></span>
<span data-ttu-id="2e625-108">**Remove-AzManagedApplicationDefinition** Cmdlet 會移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="2e625-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="2e625-109">例子</span><span class="sxs-lookup"><span data-stu-id="2e625-109">EXAMPLES</span></span>

### <span data-ttu-id="2e625-110">範例 1：根據資源識別碼移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="2e625-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="2e625-111">第一個命令會使用 Get-AzManagedApplicationDefinition Cmdlet，獲得名為 myAppDef 的受管理應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="2e625-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="2e625-112">命令會儲存在$ApplicationDefinition變數中。</span><span class="sxs-lookup"><span data-stu-id="2e625-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="2e625-113">第二個命令會移除由 **resourceId** 屬性識別的受管理應用程式定義$ApplicationDefinition。</span><span class="sxs-lookup"><span data-stu-id="2e625-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="2e625-114">參數</span><span class="sxs-lookup"><span data-stu-id="2e625-114">PARAMETERS</span></span>

### <span data-ttu-id="2e625-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2e625-115">-ApiVersion</span></span>
<span data-ttu-id="2e625-116">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="2e625-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2e625-117">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="2e625-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e625-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e625-118">-DefaultProfile</span></span>
<span data-ttu-id="2e625-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e625-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e625-120">-強制</span><span class="sxs-lookup"><span data-stu-id="2e625-120">-Force</span></span>
<span data-ttu-id="2e625-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="2e625-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e625-122">-Id</span><span class="sxs-lookup"><span data-stu-id="2e625-122">-Id</span></span>
<span data-ttu-id="2e625-123">完整受管理的應用程式定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e625-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="2e625-124">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="2e625-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e625-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e625-125">-Name</span></span>
<span data-ttu-id="2e625-126">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="2e625-126">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e625-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="2e625-127">-Pre</span></span>
<span data-ttu-id="2e625-128">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2e625-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2e625-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e625-129">-ResourceGroupName</span></span>
<span data-ttu-id="2e625-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2e625-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e625-131">-確認</span><span class="sxs-lookup"><span data-stu-id="2e625-131">-Confirm</span></span>
<span data-ttu-id="2e625-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2e625-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e625-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e625-133">-WhatIf</span></span>
<span data-ttu-id="2e625-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e625-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e625-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e625-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e625-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e625-136">CommonParameters</span></span>
<span data-ttu-id="2e625-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2e625-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e625-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e625-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e625-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2e625-139">INPUTS</span></span>

### <span data-ttu-id="2e625-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2e625-140">System.String</span></span>

## <span data-ttu-id="2e625-141">輸出</span><span class="sxs-lookup"><span data-stu-id="2e625-141">OUTPUTS</span></span>

### <span data-ttu-id="2e625-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e625-142">System.Boolean</span></span>

## <span data-ttu-id="2e625-143">筆記</span><span class="sxs-lookup"><span data-stu-id="2e625-143">NOTES</span></span>

## <span data-ttu-id="2e625-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e625-144">RELATED LINKS</span></span>
