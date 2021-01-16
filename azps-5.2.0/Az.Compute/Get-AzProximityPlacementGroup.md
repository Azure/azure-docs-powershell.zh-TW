---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277619"
---
# <span data-ttu-id="051b5-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="051b5-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="051b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="051b5-102">SYNOPSIS</span></span>
<span data-ttu-id="051b5-103">取得或列出鄰近性位置群組資源 (s) 。</span><span class="sxs-lookup"><span data-stu-id="051b5-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="051b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="051b5-104">SYNTAX</span></span>

### <span data-ttu-id="051b5-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="051b5-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="051b5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="051b5-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="051b5-107">說明</span><span class="sxs-lookup"><span data-stu-id="051b5-107">DESCRIPTION</span></span>
<span data-ttu-id="051b5-108">這個 Cmdlet 會取得或列出鄰近性位置群組資源 (s) 。</span><span class="sxs-lookup"><span data-stu-id="051b5-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="051b5-109">示例</span><span class="sxs-lookup"><span data-stu-id="051b5-109">EXAMPLES</span></span>

### <span data-ttu-id="051b5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="051b5-110">Example 1</span></span>
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

<span data-ttu-id="051b5-111">這個命令會取得鄰近性位置群組</span><span class="sxs-lookup"><span data-stu-id="051b5-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="051b5-112">範例2</span><span class="sxs-lookup"><span data-stu-id="051b5-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="051b5-113">這個命令會列出指定資源群組底下的所有鄰近性位置群組。</span><span class="sxs-lookup"><span data-stu-id="051b5-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="051b5-114">範例3</span><span class="sxs-lookup"><span data-stu-id="051b5-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="051b5-115">這個命令會列出訂閱底下的所有鄰近性位置群組。</span><span class="sxs-lookup"><span data-stu-id="051b5-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="051b5-116">參數</span><span class="sxs-lookup"><span data-stu-id="051b5-116">PARAMETERS</span></span>

### <span data-ttu-id="051b5-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="051b5-117">-ColocationStatus</span></span>
<span data-ttu-id="051b5-118">顯示 [鄰近性] 位置群組中資源的 colocation 狀態。</span><span class="sxs-lookup"><span data-stu-id="051b5-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

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

### <span data-ttu-id="051b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="051b5-119">-DefaultProfile</span></span>
<span data-ttu-id="051b5-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="051b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="051b5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="051b5-121">-Name</span></span>
<span data-ttu-id="051b5-122">鄰近性位置群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="051b5-122">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="051b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="051b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="051b5-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="051b5-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="051b5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="051b5-125">-ResourceId</span></span>
<span data-ttu-id="051b5-126">[鄰近性位置] 群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="051b5-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="051b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051b5-127">CommonParameters</span></span>
<span data-ttu-id="051b5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="051b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051b5-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="051b5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051b5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="051b5-130">INPUTS</span></span>

### <span data-ttu-id="051b5-131">System.object</span><span class="sxs-lookup"><span data-stu-id="051b5-131">System.String</span></span>

## <span data-ttu-id="051b5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="051b5-132">OUTPUTS</span></span>

### <span data-ttu-id="051b5-133">PSProximityPlacementGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="051b5-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="051b5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="051b5-134">NOTES</span></span>

## <span data-ttu-id="051b5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="051b5-135">RELATED LINKS</span></span>
