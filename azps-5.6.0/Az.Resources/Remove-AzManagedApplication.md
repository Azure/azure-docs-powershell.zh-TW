---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 41f59b46595d45932010b1fcbedae07cdeca5f78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906866"
---
# <span data-ttu-id="2edb6-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="2edb6-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="2edb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2edb6-102">SYNOPSIS</span></span>
<span data-ttu-id="2edb6-103">移除受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="2edb6-103">Removes a managed application</span></span>

## <span data-ttu-id="2edb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="2edb6-104">SYNTAX</span></span>

### <span data-ttu-id="2edb6-105">RemoveByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="2edb6-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2edb6-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="2edb6-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2edb6-107">描述</span><span class="sxs-lookup"><span data-stu-id="2edb6-107">DESCRIPTION</span></span>
<span data-ttu-id="2edb6-108">**Remove-AzManagedApplication** Cmdlet 會移除受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="2edb6-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="2edb6-109">例子</span><span class="sxs-lookup"><span data-stu-id="2edb6-109">EXAMPLES</span></span>

### <span data-ttu-id="2edb6-110">範例 1：根據資源識別碼移除受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="2edb6-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="2edb6-111">第一個命令會使用 Get-AzManagedApplication Cmdlet，獲得名為 myApp 的受管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="2edb6-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="2edb6-112">命令會儲存在$Application變數中。</span><span class="sxs-lookup"><span data-stu-id="2edb6-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="2edb6-113">第二個命令會移除 **由 resourceId** 屬性識別的 managed $Application。</span><span class="sxs-lookup"><span data-stu-id="2edb6-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="2edb6-114">參數</span><span class="sxs-lookup"><span data-stu-id="2edb6-114">PARAMETERS</span></span>

### <span data-ttu-id="2edb6-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2edb6-115">-ApiVersion</span></span>
<span data-ttu-id="2edb6-116">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="2edb6-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2edb6-117">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="2edb6-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2edb6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edb6-118">-DefaultProfile</span></span>
<span data-ttu-id="2edb6-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2edb6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2edb6-120">-強制</span><span class="sxs-lookup"><span data-stu-id="2edb6-120">-Force</span></span>
<span data-ttu-id="2edb6-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="2edb6-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2edb6-122">-Id</span><span class="sxs-lookup"><span data-stu-id="2edb6-122">-Id</span></span>
<span data-ttu-id="2edb6-123">完整受管理的應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="2edb6-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="2edb6-124">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="2edb6-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="2edb6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2edb6-125">-Name</span></span>
<span data-ttu-id="2edb6-126">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2edb6-126">The managed application name.</span></span>

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

### <span data-ttu-id="2edb6-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="2edb6-127">-Pre</span></span>
<span data-ttu-id="2edb6-128">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2edb6-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2edb6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edb6-129">-ResourceGroupName</span></span>
<span data-ttu-id="2edb6-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2edb6-130">The resource group name.</span></span>

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

### <span data-ttu-id="2edb6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="2edb6-131">-Confirm</span></span>
<span data-ttu-id="2edb6-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2edb6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2edb6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edb6-133">-WhatIf</span></span>
<span data-ttu-id="2edb6-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2edb6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2edb6-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2edb6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2edb6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edb6-136">CommonParameters</span></span>
<span data-ttu-id="2edb6-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2edb6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edb6-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2edb6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edb6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2edb6-139">INPUTS</span></span>

### <span data-ttu-id="2edb6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2edb6-140">System.String</span></span>

## <span data-ttu-id="2edb6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="2edb6-141">OUTPUTS</span></span>

### <span data-ttu-id="2edb6-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2edb6-142">System.Boolean</span></span>

## <span data-ttu-id="2edb6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="2edb6-143">NOTES</span></span>

## <span data-ttu-id="2edb6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="2edb6-144">RELATED LINKS</span></span>
