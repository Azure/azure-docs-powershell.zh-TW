---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139548"
---
# <span data-ttu-id="8e4aa-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e4aa-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="8e4aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4aa-103">刪除與 VirtualHub 相關聯的中樞路由表資源。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="8e4aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e4aa-104">SYNTAX</span></span>

### <span data-ttu-id="8e4aa-105">ByVHubRouteTableName (預設) </span><span class="sxs-lookup"><span data-stu-id="8e4aa-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4aa-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8e4aa-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4aa-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="8e4aa-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4aa-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="8e4aa-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e4aa-109">說明</span><span class="sxs-lookup"><span data-stu-id="8e4aa-109">DESCRIPTION</span></span>
<span data-ttu-id="8e4aa-110">刪除與指定的虛擬中樞相關聯的指定中樞路由表。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="8e4aa-111">示例</span><span class="sxs-lookup"><span data-stu-id="8e4aa-111">EXAMPLES</span></span>

### <span data-ttu-id="8e4aa-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8e4aa-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="8e4aa-113">這個命令會刪除虛擬中樞的中心路由表。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="8e4aa-114">參數</span><span class="sxs-lookup"><span data-stu-id="8e4aa-114">PARAMETERS</span></span>

### <span data-ttu-id="8e4aa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e4aa-115">-AsJob</span></span>
<span data-ttu-id="8e4aa-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e4aa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e4aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4aa-117">-DefaultProfile</span></span>
<span data-ttu-id="8e4aa-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e4aa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8e4aa-119">-Force</span></span>
<span data-ttu-id="8e4aa-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="8e4aa-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8e4aa-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e4aa-121">-InputObject</span></span>
<span data-ttu-id="8e4aa-122">要移除的 vhubroutetable 資源。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="8e4aa-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e4aa-123">-Name</span></span>
<span data-ttu-id="8e4aa-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-124">The resource name.</span></span>

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

### <span data-ttu-id="8e4aa-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e4aa-125">-ParentObject</span></span>
<span data-ttu-id="8e4aa-126">此資源的父虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="8e4aa-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="8e4aa-127">-ParentResourceName</span></span>
<span data-ttu-id="8e4aa-128">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-128">The parent resource name.</span></span>

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

### <span data-ttu-id="8e4aa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e4aa-129">-PassThru</span></span>
<span data-ttu-id="8e4aa-130">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="8e4aa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4aa-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e4aa-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-132">The resource group name.</span></span>

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

### <span data-ttu-id="8e4aa-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e4aa-133">-ResourceId</span></span>
<span data-ttu-id="8e4aa-134">要移除之 vhubroutetable 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="8e4aa-135">-確認</span><span class="sxs-lookup"><span data-stu-id="8e4aa-135">-Confirm</span></span>
<span data-ttu-id="8e4aa-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e4aa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e4aa-137">-WhatIf</span></span>
<span data-ttu-id="8e4aa-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e4aa-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e4aa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4aa-140">CommonParameters</span></span>
<span data-ttu-id="8e4aa-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4aa-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e4aa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4aa-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8e4aa-143">INPUTS</span></span>

### <span data-ttu-id="8e4aa-144">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e4aa-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="8e4aa-145">PSVHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e4aa-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="8e4aa-146">System.object</span><span class="sxs-lookup"><span data-stu-id="8e4aa-146">System.String</span></span>

## <span data-ttu-id="8e4aa-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8e4aa-147">OUTPUTS</span></span>

### <span data-ttu-id="8e4aa-148">System.object</span><span class="sxs-lookup"><span data-stu-id="8e4aa-148">System.Boolean</span></span>

## <span data-ttu-id="8e4aa-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8e4aa-149">NOTES</span></span>

## <span data-ttu-id="8e4aa-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e4aa-150">RELATED LINKS</span></span>

[<span data-ttu-id="8e4aa-151">AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e4aa-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="8e4aa-152">新-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="8e4aa-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="8e4aa-153">新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e4aa-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="8e4aa-154">更新-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e4aa-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)