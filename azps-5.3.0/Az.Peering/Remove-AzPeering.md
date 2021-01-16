---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288492"
---
# <span data-ttu-id="c7177-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c7177-101">Remove-AzPeering</span></span>

## <span data-ttu-id="c7177-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7177-102">SYNOPSIS</span></span>
<span data-ttu-id="c7177-103">刪除或移除對等。</span><span class="sxs-lookup"><span data-stu-id="c7177-103">Delete or remove a peering.</span></span> <span data-ttu-id="c7177-104">這將會刪除該資源的所有子資源或警示。</span><span class="sxs-lookup"><span data-stu-id="c7177-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="c7177-105">句法</span><span class="sxs-lookup"><span data-stu-id="c7177-105">SYNTAX</span></span>

### <span data-ttu-id="c7177-106">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="c7177-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7177-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c7177-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7177-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7177-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7177-109">說明</span><span class="sxs-lookup"><span data-stu-id="c7177-109">DESCRIPTION</span></span>
<span data-ttu-id="c7177-110">Perminently [刪除對等資源]。</span><span class="sxs-lookup"><span data-stu-id="c7177-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="c7177-111">示例</span><span class="sxs-lookup"><span data-stu-id="c7177-111">EXAMPLES</span></span>

### <span data-ttu-id="c7177-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c7177-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="c7177-113">移除對等資源識別碼的對等。</span><span class="sxs-lookup"><span data-stu-id="c7177-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="c7177-114">參數</span><span class="sxs-lookup"><span data-stu-id="c7177-114">PARAMETERS</span></span>

### <span data-ttu-id="c7177-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7177-115">-AsJob</span></span>
<span data-ttu-id="c7177-116">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="c7177-116">Run in the background.</span></span>

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

### <span data-ttu-id="c7177-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7177-117">-DefaultProfile</span></span>
<span data-ttu-id="c7177-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7177-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7177-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c7177-119">-Force</span></span>
<span data-ttu-id="c7177-120">強制完成操作</span><span class="sxs-lookup"><span data-stu-id="c7177-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="c7177-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7177-121">-InputObject</span></span>
<span data-ttu-id="c7177-122">使用 Get-AzPeering 來檢索這個物件。</span><span class="sxs-lookup"><span data-stu-id="c7177-122">Use Get-AzPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="c7177-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7177-123">-Name</span></span>
<span data-ttu-id="c7177-124">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="c7177-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c7177-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7177-125">-PassThru</span></span>
<span data-ttu-id="c7177-126">如果完成，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="c7177-126">Return true if complete</span></span>

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

### <span data-ttu-id="c7177-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7177-127">-ResourceGroupName</span></span>
<span data-ttu-id="c7177-128">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c7177-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c7177-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7177-129">-ResourceId</span></span>
<span data-ttu-id="c7177-130">資源識別碼字串名稱。</span><span class="sxs-lookup"><span data-stu-id="c7177-130">The resource id string name.</span></span>

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

### <span data-ttu-id="c7177-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c7177-131">-Confirm</span></span>
<span data-ttu-id="c7177-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7177-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7177-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7177-133">-WhatIf</span></span>
<span data-ttu-id="c7177-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7177-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7177-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7177-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7177-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7177-136">CommonParameters</span></span>
<span data-ttu-id="c7177-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7177-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7177-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c7177-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7177-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c7177-139">INPUTS</span></span>

### <span data-ttu-id="c7177-140">PSPeering 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="c7177-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="c7177-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c7177-141">System.String</span></span>

## <span data-ttu-id="c7177-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c7177-142">OUTPUTS</span></span>

### <span data-ttu-id="c7177-143">System.object</span><span class="sxs-lookup"><span data-stu-id="c7177-143">System.Boolean</span></span>

## <span data-ttu-id="c7177-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c7177-144">NOTES</span></span>

## <span data-ttu-id="c7177-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7177-145">RELATED LINKS</span></span>
