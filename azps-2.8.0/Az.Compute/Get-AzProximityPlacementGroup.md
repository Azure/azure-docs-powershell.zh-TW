---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 9ec2760ba50d4ed97ebf36f5bab7c02d110d77ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613410"
---
# <span data-ttu-id="aa690-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="aa690-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="aa690-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa690-102">SYNOPSIS</span></span>
<span data-ttu-id="aa690-103">取得或列出鄰近性位置群組資源 (s) 。</span><span class="sxs-lookup"><span data-stu-id="aa690-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="aa690-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa690-104">SYNTAX</span></span>

### <span data-ttu-id="aa690-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="aa690-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa690-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="aa690-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa690-107">說明</span><span class="sxs-lookup"><span data-stu-id="aa690-107">DESCRIPTION</span></span>
<span data-ttu-id="aa690-108">這個 Cmdlet 會取得或列出鄰近性位置群組資源 (s) 。</span><span class="sxs-lookup"><span data-stu-id="aa690-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="aa690-109">示例</span><span class="sxs-lookup"><span data-stu-id="aa690-109">EXAMPLES</span></span>

### <span data-ttu-id="aa690-110">範例1</span><span class="sxs-lookup"><span data-stu-id="aa690-110">Example 1</span></span>
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

<span data-ttu-id="aa690-111">這個命令會取得鄰近性位置群組</span><span class="sxs-lookup"><span data-stu-id="aa690-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="aa690-112">範例2</span><span class="sxs-lookup"><span data-stu-id="aa690-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="aa690-113">這個命令會列出指定資源群組底下的所有鄰近性位置群組。</span><span class="sxs-lookup"><span data-stu-id="aa690-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="aa690-114">範例3</span><span class="sxs-lookup"><span data-stu-id="aa690-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="aa690-115">這個命令會列出訂閱底下的所有鄰近性位置群組。</span><span class="sxs-lookup"><span data-stu-id="aa690-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="aa690-116">參數</span><span class="sxs-lookup"><span data-stu-id="aa690-116">PARAMETERS</span></span>

### <span data-ttu-id="aa690-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa690-117">-DefaultProfile</span></span>
<span data-ttu-id="aa690-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa690-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa690-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa690-119">-Name</span></span>
<span data-ttu-id="aa690-120">鄰近性位置群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa690-120">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="aa690-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa690-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa690-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa690-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa690-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa690-123">-ResourceId</span></span>
<span data-ttu-id="aa690-124">[鄰近性位置] 群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa690-124">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="aa690-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa690-125">CommonParameters</span></span>
<span data-ttu-id="aa690-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa690-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa690-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aa690-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa690-128">輸入</span><span class="sxs-lookup"><span data-stu-id="aa690-128">INPUTS</span></span>

### <span data-ttu-id="aa690-129">System.object</span><span class="sxs-lookup"><span data-stu-id="aa690-129">System.String</span></span>

## <span data-ttu-id="aa690-130">輸出</span><span class="sxs-lookup"><span data-stu-id="aa690-130">OUTPUTS</span></span>

### <span data-ttu-id="aa690-131">PSProximityPlacementGroup 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="aa690-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="aa690-132">筆記</span><span class="sxs-lookup"><span data-stu-id="aa690-132">NOTES</span></span>

## <span data-ttu-id="aa690-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa690-133">RELATED LINKS</span></span>
