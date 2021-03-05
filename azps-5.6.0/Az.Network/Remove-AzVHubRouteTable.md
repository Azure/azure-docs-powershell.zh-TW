---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: fb7a9933a30760fe3bc33f296b93d6bc739c18eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917970"
---
# <span data-ttu-id="bdede-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdede-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="bdede-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bdede-102">SYNOPSIS</span></span>
<span data-ttu-id="bdede-103">刪除與 VirtualHub 相關聯的中樞路由資料表資源。</span><span class="sxs-lookup"><span data-stu-id="bdede-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="bdede-104">語法</span><span class="sxs-lookup"><span data-stu-id="bdede-104">SYNTAX</span></span>

### <span data-ttu-id="bdede-105">ByVHubRouteTableName (預設) </span><span class="sxs-lookup"><span data-stu-id="bdede-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdede-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="bdede-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdede-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="bdede-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdede-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="bdede-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdede-109">描述</span><span class="sxs-lookup"><span data-stu-id="bdede-109">DESCRIPTION</span></span>
<span data-ttu-id="bdede-110">刪除與指定虛擬中樞相關聯的指定中樞路由資料表。</span><span class="sxs-lookup"><span data-stu-id="bdede-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="bdede-111">例子</span><span class="sxs-lookup"><span data-stu-id="bdede-111">EXAMPLES</span></span>

### <span data-ttu-id="bdede-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="bdede-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="bdede-113">此命令會刪除虛擬中樞的中樞路由資料表。</span><span class="sxs-lookup"><span data-stu-id="bdede-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="bdede-114">參數</span><span class="sxs-lookup"><span data-stu-id="bdede-114">PARAMETERS</span></span>

### <span data-ttu-id="bdede-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdede-115">-AsJob</span></span>
<span data-ttu-id="bdede-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bdede-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdede-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdede-117">-DefaultProfile</span></span>
<span data-ttu-id="bdede-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdede-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdede-119">-強制</span><span class="sxs-lookup"><span data-stu-id="bdede-119">-Force</span></span>
<span data-ttu-id="bdede-120">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="bdede-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bdede-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdede-121">-InputObject</span></span>
<span data-ttu-id="bdede-122">要移除的 vhubroutetable 資源。</span><span class="sxs-lookup"><span data-stu-id="bdede-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdede-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdede-123">-Name</span></span>
<span data-ttu-id="bdede-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bdede-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdede-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bdede-125">-ParentObject</span></span>
<span data-ttu-id="bdede-126">此資源的父虛擬中樞物件。</span><span class="sxs-lookup"><span data-stu-id="bdede-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdede-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bdede-127">-ParentResourceName</span></span>
<span data-ttu-id="bdede-128">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bdede-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdede-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdede-129">-PassThru</span></span>
<span data-ttu-id="bdede-130">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="bdede-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="bdede-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdede-131">-ResourceGroupName</span></span>
<span data-ttu-id="bdede-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bdede-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdede-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdede-133">-ResourceId</span></span>
<span data-ttu-id="bdede-134">要移除的 vhubroutetable 資源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bdede-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdede-135">-確認</span><span class="sxs-lookup"><span data-stu-id="bdede-135">-Confirm</span></span>
<span data-ttu-id="bdede-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bdede-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdede-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdede-137">-WhatIf</span></span>
<span data-ttu-id="bdede-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bdede-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdede-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bdede-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdede-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdede-140">CommonParameters</span></span>
<span data-ttu-id="bdede-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bdede-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdede-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdede-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdede-143">輸入</span><span class="sxs-lookup"><span data-stu-id="bdede-143">INPUTS</span></span>

### <span data-ttu-id="bdede-144">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bdede-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="bdede-145">Microsoft.Azure.Commands.Network.models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdede-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="bdede-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bdede-146">System.String</span></span>

## <span data-ttu-id="bdede-147">輸出</span><span class="sxs-lookup"><span data-stu-id="bdede-147">OUTPUTS</span></span>

### <span data-ttu-id="bdede-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdede-148">System.Boolean</span></span>

## <span data-ttu-id="bdede-149">筆記</span><span class="sxs-lookup"><span data-stu-id="bdede-149">NOTES</span></span>

## <span data-ttu-id="bdede-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdede-150">RELATED LINKS</span></span>

[<span data-ttu-id="bdede-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdede-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="bdede-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="bdede-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="bdede-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdede-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="bdede-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdede-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)