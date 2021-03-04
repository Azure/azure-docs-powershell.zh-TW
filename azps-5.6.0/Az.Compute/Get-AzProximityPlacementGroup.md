---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 7a69b47cef0d1f2ad11dcbe1c2bd191149d127df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917410"
---
# <span data-ttu-id="6630d-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6630d-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="6630d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6630d-102">SYNOPSIS</span></span>
<span data-ttu-id="6630d-103">取得或列出鄰近位置群組資源 () 。</span><span class="sxs-lookup"><span data-stu-id="6630d-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="6630d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6630d-104">SYNTAX</span></span>

### <span data-ttu-id="6630d-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="6630d-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6630d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6630d-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6630d-107">描述</span><span class="sxs-lookup"><span data-stu-id="6630d-107">DESCRIPTION</span></span>
<span data-ttu-id="6630d-108">此 Cmdlet 會取得或列出鄰近位置群組 (資源) 。</span><span class="sxs-lookup"><span data-stu-id="6630d-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="6630d-109">例子</span><span class="sxs-lookup"><span data-stu-id="6630d-109">EXAMPLES</span></span>

### <span data-ttu-id="6630d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="6630d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="6630d-111">此命令會獲得鄰近位置群組</span><span class="sxs-lookup"><span data-stu-id="6630d-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="6630d-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="6630d-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="6630d-113">此命令會列出給定資源群組下的所有鄰近位置群組。</span><span class="sxs-lookup"><span data-stu-id="6630d-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="6630d-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="6630d-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="6630d-115">此命令會列出訂閱下的所有鄰近位置群組。</span><span class="sxs-lookup"><span data-stu-id="6630d-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="6630d-116">參數</span><span class="sxs-lookup"><span data-stu-id="6630d-116">PARAMETERS</span></span>

### <span data-ttu-id="6630d-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="6630d-117">-ColocationStatus</span></span>
<span data-ttu-id="6630d-118">顯示鄰近位置群組中資源的共置狀態。</span><span class="sxs-lookup"><span data-stu-id="6630d-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6630d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6630d-119">-DefaultProfile</span></span>
<span data-ttu-id="6630d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6630d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6630d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6630d-121">-Name</span></span>
<span data-ttu-id="6630d-122">鄰近位置組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6630d-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6630d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6630d-123">-ResourceGroupName</span></span>
<span data-ttu-id="6630d-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6630d-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6630d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6630d-125">-ResourceId</span></span>
<span data-ttu-id="6630d-126">鄰近位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6630d-126">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6630d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6630d-127">CommonParameters</span></span>
<span data-ttu-id="6630d-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6630d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6630d-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6630d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6630d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6630d-130">INPUTS</span></span>

### <span data-ttu-id="6630d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6630d-131">System.String</span></span>

## <span data-ttu-id="6630d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6630d-132">OUTPUTS</span></span>

### <span data-ttu-id="6630d-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6630d-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="6630d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6630d-134">NOTES</span></span>

## <span data-ttu-id="6630d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6630d-135">RELATED LINKS</span></span>
