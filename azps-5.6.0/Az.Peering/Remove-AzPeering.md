---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: ba6817928751c67e87f6641a6362a1fbf84eece8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911429"
---
# <span data-ttu-id="908be-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="908be-101">Remove-AzPeering</span></span>

## <span data-ttu-id="908be-102">簡介</span><span class="sxs-lookup"><span data-stu-id="908be-102">SYNOPSIS</span></span>
<span data-ttu-id="908be-103">刪除或移除對等。</span><span class="sxs-lookup"><span data-stu-id="908be-103">Delete or remove a peering.</span></span> <span data-ttu-id="908be-104">這會刪除所有子資源或提醒資源。</span><span class="sxs-lookup"><span data-stu-id="908be-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="908be-105">語法</span><span class="sxs-lookup"><span data-stu-id="908be-105">SYNTAX</span></span>

### <span data-ttu-id="908be-106">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="908be-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="908be-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="908be-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="908be-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="908be-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="908be-109">描述</span><span class="sxs-lookup"><span data-stu-id="908be-109">DESCRIPTION</span></span>
<span data-ttu-id="908be-110">明顯刪除對等資源。</span><span class="sxs-lookup"><span data-stu-id="908be-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="908be-111">例子</span><span class="sxs-lookup"><span data-stu-id="908be-111">EXAMPLES</span></span>

### <span data-ttu-id="908be-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="908be-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="908be-113">根據資源識別碼移除對等。</span><span class="sxs-lookup"><span data-stu-id="908be-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="908be-114">參數</span><span class="sxs-lookup"><span data-stu-id="908be-114">PARAMETERS</span></span>

### <span data-ttu-id="908be-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="908be-115">-AsJob</span></span>
<span data-ttu-id="908be-116">在背景執行。</span><span class="sxs-lookup"><span data-stu-id="908be-116">Run in the background.</span></span>

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

### <span data-ttu-id="908be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908be-117">-DefaultProfile</span></span>
<span data-ttu-id="908be-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="908be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="908be-119">-強制</span><span class="sxs-lookup"><span data-stu-id="908be-119">-Force</span></span>
<span data-ttu-id="908be-120">強制完成作業</span><span class="sxs-lookup"><span data-stu-id="908be-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="908be-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="908be-121">-InputObject</span></span>
<span data-ttu-id="908be-122">使用Get-AzPeering來取回此物件。</span><span class="sxs-lookup"><span data-stu-id="908be-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="908be-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="908be-123">-Name</span></span>
<span data-ttu-id="908be-124">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="908be-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908be-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="908be-125">-PassThru</span></span>
<span data-ttu-id="908be-126">如果已完成，請返回 True</span><span class="sxs-lookup"><span data-stu-id="908be-126">Return true if complete</span></span>

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

### <span data-ttu-id="908be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908be-127">-ResourceGroupName</span></span>
<span data-ttu-id="908be-128">建立或使用現有的資源組名。</span><span class="sxs-lookup"><span data-stu-id="908be-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908be-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="908be-129">-ResourceId</span></span>
<span data-ttu-id="908be-130">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="908be-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="908be-131">-確認</span><span class="sxs-lookup"><span data-stu-id="908be-131">-Confirm</span></span>
<span data-ttu-id="908be-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="908be-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="908be-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="908be-133">-WhatIf</span></span>
<span data-ttu-id="908be-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="908be-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="908be-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="908be-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="908be-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908be-136">CommonParameters</span></span>
<span data-ttu-id="908be-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="908be-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908be-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="908be-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908be-139">輸入</span><span class="sxs-lookup"><span data-stu-id="908be-139">INPUTS</span></span>

### <span data-ttu-id="908be-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="908be-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="908be-141">System.String</span><span class="sxs-lookup"><span data-stu-id="908be-141">System.String</span></span>

## <span data-ttu-id="908be-142">輸出</span><span class="sxs-lookup"><span data-stu-id="908be-142">OUTPUTS</span></span>

### <span data-ttu-id="908be-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="908be-143">System.Boolean</span></span>

## <span data-ttu-id="908be-144">筆記</span><span class="sxs-lookup"><span data-stu-id="908be-144">NOTES</span></span>

## <span data-ttu-id="908be-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="908be-145">RELATED LINKS</span></span>
