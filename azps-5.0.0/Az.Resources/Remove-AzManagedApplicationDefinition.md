---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286264"
---
# <span data-ttu-id="b1f98-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b1f98-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="b1f98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1f98-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f98-103">移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="b1f98-103">Removes a managed application definition</span></span>

## <span data-ttu-id="b1f98-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1f98-104">SYNTAX</span></span>

### <span data-ttu-id="b1f98-105">RemoveByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="b1f98-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1f98-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="b1f98-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f98-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1f98-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f98-108">**AzManagedApplicationDefinition** Cmdlet 會移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="b1f98-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="b1f98-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1f98-109">EXAMPLES</span></span>

### <span data-ttu-id="b1f98-110">範例1：以資源識別碼移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="b1f98-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="b1f98-111">第一個命令會使用 Get-AzManagedApplicationDefinition Cmdlet 來取得名為 myAppDef 的管理應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="b1f98-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="b1f98-112">該命令會將它儲存在 $ApplicationDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1f98-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="b1f98-113">第二個命令會移除由 $ApplicationDefinition 的 **ResourceId** 屬性所識別的受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="b1f98-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="b1f98-114">參數</span><span class="sxs-lookup"><span data-stu-id="b1f98-114">PARAMETERS</span></span>

### <span data-ttu-id="b1f98-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1f98-115">-ApiVersion</span></span>
<span data-ttu-id="b1f98-116">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b1f98-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b1f98-117">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="b1f98-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b1f98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f98-118">-DefaultProfile</span></span>
<span data-ttu-id="b1f98-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1f98-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1f98-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b1f98-120">-Force</span></span>
<span data-ttu-id="b1f98-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b1f98-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b1f98-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b1f98-122">-Id</span></span>
<span data-ttu-id="b1f98-123">完全限定的管理應用程式定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1f98-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="b1f98-124">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b1f98-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b1f98-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1f98-125">-Name</span></span>
<span data-ttu-id="b1f98-126">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="b1f98-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="b1f98-127">-預先</span><span class="sxs-lookup"><span data-stu-id="b1f98-127">-Pre</span></span>
<span data-ttu-id="b1f98-128">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="b1f98-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b1f98-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f98-129">-ResourceGroupName</span></span>
<span data-ttu-id="b1f98-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1f98-130">The resource group name.</span></span>

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

### <span data-ttu-id="b1f98-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b1f98-131">-Confirm</span></span>
<span data-ttu-id="b1f98-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1f98-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f98-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f98-133">-WhatIf</span></span>
<span data-ttu-id="b1f98-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1f98-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f98-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1f98-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f98-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f98-136">CommonParameters</span></span>
<span data-ttu-id="b1f98-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1f98-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f98-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1f98-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f98-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b1f98-139">INPUTS</span></span>

### <span data-ttu-id="b1f98-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b1f98-140">System.String</span></span>

## <span data-ttu-id="b1f98-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b1f98-141">OUTPUTS</span></span>

### <span data-ttu-id="b1f98-142">System.object</span><span class="sxs-lookup"><span data-stu-id="b1f98-142">System.Boolean</span></span>

## <span data-ttu-id="b1f98-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b1f98-143">NOTES</span></span>

## <span data-ttu-id="b1f98-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1f98-144">RELATED LINKS</span></span>
