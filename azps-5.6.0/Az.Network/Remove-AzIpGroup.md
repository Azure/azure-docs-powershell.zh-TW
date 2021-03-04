---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: f1c8589663008b0ebc640a052199a11c82d3b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913425"
---
# <span data-ttu-id="df870-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="df870-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="df870-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df870-102">SYNOPSIS</span></span>
<span data-ttu-id="df870-103">刪除 Azure IpGroup。</span><span class="sxs-lookup"><span data-stu-id="df870-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="df870-104">語法</span><span class="sxs-lookup"><span data-stu-id="df870-104">SYNTAX</span></span>

### <span data-ttu-id="df870-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="df870-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df870-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df870-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df870-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df870-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df870-108">描述</span><span class="sxs-lookup"><span data-stu-id="df870-108">DESCRIPTION</span></span>
<span data-ttu-id="df870-109">**Remove-AzIpGroup** Cmdlet 會刪除 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="df870-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="df870-110">例子</span><span class="sxs-lookup"><span data-stu-id="df870-110">EXAMPLES</span></span>

### <span data-ttu-id="df870-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="df870-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="df870-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="df870-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="df870-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="df870-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="df870-114">參數</span><span class="sxs-lookup"><span data-stu-id="df870-114">PARAMETERS</span></span>

### <span data-ttu-id="df870-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df870-115">-AsJob</span></span>
<span data-ttu-id="df870-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="df870-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df870-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df870-117">-DefaultProfile</span></span>
<span data-ttu-id="df870-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="df870-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df870-119">-強制</span><span class="sxs-lookup"><span data-stu-id="df870-119">-Force</span></span>
<span data-ttu-id="df870-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="df870-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df870-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="df870-121">-IpGroup</span></span>
<span data-ttu-id="df870-122">ipGroup 輸入物件。</span><span class="sxs-lookup"><span data-stu-id="df870-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df870-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="df870-123">-Name</span></span>
<span data-ttu-id="df870-124">ipgroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="df870-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df870-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df870-125">-PassThru</span></span>
<span data-ttu-id="df870-126">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="df870-126">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df870-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df870-127">-ResourceGroupName</span></span>
<span data-ttu-id="df870-128">ipgroup 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="df870-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df870-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df870-129">-ResourceId</span></span>
<span data-ttu-id="df870-130">ipgroup 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="df870-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df870-131">-確認</span><span class="sxs-lookup"><span data-stu-id="df870-131">-Confirm</span></span>
<span data-ttu-id="df870-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="df870-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df870-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df870-133">-WhatIf</span></span>
<span data-ttu-id="df870-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df870-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df870-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df870-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df870-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df870-136">CommonParameters</span></span>
<span data-ttu-id="df870-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df870-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df870-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df870-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df870-139">輸入</span><span class="sxs-lookup"><span data-stu-id="df870-139">INPUTS</span></span>

### <span data-ttu-id="df870-140">System.String</span><span class="sxs-lookup"><span data-stu-id="df870-140">System.String</span></span>

### <span data-ttu-id="df870-141">Microsoft.Azure.Commands.Network.models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="df870-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="df870-142">輸出</span><span class="sxs-lookup"><span data-stu-id="df870-142">OUTPUTS</span></span>

### <span data-ttu-id="df870-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df870-143">System.Boolean</span></span>

## <span data-ttu-id="df870-144">筆記</span><span class="sxs-lookup"><span data-stu-id="df870-144">NOTES</span></span>

## <span data-ttu-id="df870-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="df870-145">RELATED LINKS</span></span>
