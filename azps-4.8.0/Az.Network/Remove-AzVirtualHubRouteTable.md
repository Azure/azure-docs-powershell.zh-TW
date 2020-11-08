---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970321"
---
# <span data-ttu-id="d2f07-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d2f07-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="d2f07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2f07-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f07-103">刪除與虛擬中樞相關聯的虛擬中心路由表資源。</span><span class="sxs-lookup"><span data-stu-id="d2f07-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="d2f07-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2f07-104">SYNTAX</span></span>

### <span data-ttu-id="d2f07-105">ByVirtualHubRouteTableName (預設) </span><span class="sxs-lookup"><span data-stu-id="d2f07-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f07-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d2f07-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f07-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="d2f07-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f07-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="d2f07-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f07-109">說明</span><span class="sxs-lookup"><span data-stu-id="d2f07-109">DESCRIPTION</span></span>
<span data-ttu-id="d2f07-110">刪除與指定的虛擬中樞相關聯的指定路由表。</span><span class="sxs-lookup"><span data-stu-id="d2f07-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="d2f07-111">示例</span><span class="sxs-lookup"><span data-stu-id="d2f07-111">EXAMPLES</span></span>

### <span data-ttu-id="d2f07-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d2f07-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="d2f07-113">這個命令會刪除虛擬中樞 westushub 的 routeTable1。</span><span class="sxs-lookup"><span data-stu-id="d2f07-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="d2f07-114">參數</span><span class="sxs-lookup"><span data-stu-id="d2f07-114">PARAMETERS</span></span>

### <span data-ttu-id="d2f07-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2f07-115">-AsJob</span></span>
<span data-ttu-id="d2f07-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d2f07-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2f07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f07-117">-DefaultProfile</span></span>
<span data-ttu-id="d2f07-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2f07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f07-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d2f07-119">-Force</span></span>
<span data-ttu-id="d2f07-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="d2f07-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d2f07-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="d2f07-121">-HubName</span></span>
<span data-ttu-id="d2f07-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f07-122">The parent resource name.</span></span>

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

### <span data-ttu-id="d2f07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2f07-123">-InputObject</span></span>
<span data-ttu-id="d2f07-124">要移除的 virtualhubroutetable 資源。</span><span class="sxs-lookup"><span data-stu-id="d2f07-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="d2f07-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2f07-125">-Name</span></span>
<span data-ttu-id="d2f07-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f07-126">The resource name.</span></span>

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

### <span data-ttu-id="d2f07-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2f07-127">-PassThru</span></span>
<span data-ttu-id="d2f07-128">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d2f07-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="d2f07-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f07-129">-ResourceGroupName</span></span>
<span data-ttu-id="d2f07-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2f07-130">The resource group name.</span></span>

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

### <span data-ttu-id="d2f07-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2f07-131">-ResourceId</span></span>
<span data-ttu-id="d2f07-132">要移除之 virtualhubroutetable 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2f07-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="d2f07-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d2f07-133">-VirtualHub</span></span>
<span data-ttu-id="d2f07-134">{{Fill VirtualHub 說明}}</span><span class="sxs-lookup"><span data-stu-id="d2f07-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="d2f07-135">-確認</span><span class="sxs-lookup"><span data-stu-id="d2f07-135">-Confirm</span></span>
<span data-ttu-id="d2f07-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2f07-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f07-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f07-137">-WhatIf</span></span>
<span data-ttu-id="d2f07-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2f07-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f07-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2f07-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f07-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f07-140">CommonParameters</span></span>
<span data-ttu-id="d2f07-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2f07-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f07-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d2f07-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f07-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d2f07-143">INPUTS</span></span>

### <span data-ttu-id="d2f07-144">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d2f07-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d2f07-145">PSVirtualHubRouteTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d2f07-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="d2f07-146">System.object</span><span class="sxs-lookup"><span data-stu-id="d2f07-146">System.String</span></span>

## <span data-ttu-id="d2f07-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d2f07-147">OUTPUTS</span></span>

### <span data-ttu-id="d2f07-148">System.object</span><span class="sxs-lookup"><span data-stu-id="d2f07-148">System.Boolean</span></span>

## <span data-ttu-id="d2f07-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d2f07-149">NOTES</span></span>

## <span data-ttu-id="d2f07-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2f07-150">RELATED LINKS</span></span>
