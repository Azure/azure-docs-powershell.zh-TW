---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: ecec3482c06c77063ebac71788d5bf2058c9ce64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915977"
---
# <span data-ttu-id="361e6-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="361e6-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="361e6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="361e6-102">SYNOPSIS</span></span>
<span data-ttu-id="361e6-103">刪除與虛擬中樞相關聯的虛擬中樞路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="361e6-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="361e6-104">語法</span><span class="sxs-lookup"><span data-stu-id="361e6-104">SYNTAX</span></span>

### <span data-ttu-id="361e6-105">ByVirtualHubRouteTableName (預設) </span><span class="sxs-lookup"><span data-stu-id="361e6-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="361e6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="361e6-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="361e6-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="361e6-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="361e6-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="361e6-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="361e6-109">描述</span><span class="sxs-lookup"><span data-stu-id="361e6-109">DESCRIPTION</span></span>
<span data-ttu-id="361e6-110">刪除與指定虛擬中樞相關聯的指定路由資料表。</span><span class="sxs-lookup"><span data-stu-id="361e6-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="361e6-111">例子</span><span class="sxs-lookup"><span data-stu-id="361e6-111">EXAMPLES</span></span>

### <span data-ttu-id="361e6-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="361e6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="361e6-113">此命令會刪除虛擬中樞 westushub 的 RouteTable1。</span><span class="sxs-lookup"><span data-stu-id="361e6-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="361e6-114">參數</span><span class="sxs-lookup"><span data-stu-id="361e6-114">PARAMETERS</span></span>

### <span data-ttu-id="361e6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="361e6-115">-AsJob</span></span>
<span data-ttu-id="361e6-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="361e6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="361e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361e6-117">-DefaultProfile</span></span>
<span data-ttu-id="361e6-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="361e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="361e6-119">-強制</span><span class="sxs-lookup"><span data-stu-id="361e6-119">-Force</span></span>
<span data-ttu-id="361e6-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="361e6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="361e6-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="361e6-121">-HubName</span></span>
<span data-ttu-id="361e6-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="361e6-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="361e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="361e6-123">-InputObject</span></span>
<span data-ttu-id="361e6-124">要移除的 virtualhubroutetable 資源。</span><span class="sxs-lookup"><span data-stu-id="361e6-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="361e6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="361e6-125">-Name</span></span>
<span data-ttu-id="361e6-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="361e6-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="361e6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="361e6-127">-PassThru</span></span>
<span data-ttu-id="361e6-128">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="361e6-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="361e6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="361e6-129">-ResourceGroupName</span></span>
<span data-ttu-id="361e6-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="361e6-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="361e6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="361e6-131">-ResourceId</span></span>
<span data-ttu-id="361e6-132">要移除的 virtualhubroutetable 資源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="361e6-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="361e6-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="361e6-133">-VirtualHub</span></span>
<span data-ttu-id="361e6-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="361e6-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="361e6-135">-確認</span><span class="sxs-lookup"><span data-stu-id="361e6-135">-Confirm</span></span>
<span data-ttu-id="361e6-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="361e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="361e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="361e6-137">-WhatIf</span></span>
<span data-ttu-id="361e6-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="361e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="361e6-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="361e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="361e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361e6-140">CommonParameters</span></span>
<span data-ttu-id="361e6-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="361e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361e6-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="361e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361e6-143">輸入</span><span class="sxs-lookup"><span data-stu-id="361e6-143">INPUTS</span></span>

### <span data-ttu-id="361e6-144">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="361e6-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="361e6-145">Microsoft.Azure.Commands.Network.models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="361e6-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="361e6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="361e6-146">System.String</span></span>

## <span data-ttu-id="361e6-147">輸出</span><span class="sxs-lookup"><span data-stu-id="361e6-147">OUTPUTS</span></span>

### <span data-ttu-id="361e6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="361e6-148">System.Boolean</span></span>

## <span data-ttu-id="361e6-149">筆記</span><span class="sxs-lookup"><span data-stu-id="361e6-149">NOTES</span></span>

## <span data-ttu-id="361e6-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="361e6-150">RELATED LINKS</span></span>
