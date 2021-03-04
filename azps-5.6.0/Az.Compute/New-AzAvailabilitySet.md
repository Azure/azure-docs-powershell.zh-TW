---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 8ae2a7acef3459ff1f9310511a3114a609cc6459
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904742"
---
# <span data-ttu-id="acdd3-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acdd3-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="acdd3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="acdd3-102">SYNOPSIS</span></span>
<span data-ttu-id="acdd3-103">建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="acdd3-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="acdd3-104">語法</span><span class="sxs-lookup"><span data-stu-id="acdd3-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acdd3-105">描述</span><span class="sxs-lookup"><span data-stu-id="acdd3-105">DESCRIPTION</span></span>
<span data-ttu-id="acdd3-106">**New-AzAvailabilitySet** Cmdlet 會建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="acdd3-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="acdd3-107">例子</span><span class="sxs-lookup"><span data-stu-id="acdd3-107">EXAMPLES</span></span>

### <span data-ttu-id="acdd3-108">範例 1：建立可用性集</span><span class="sxs-lookup"><span data-stu-id="acdd3-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="acdd3-109">此命令在名為 ResourceGroup11 的資源群組中，建立一個名為 AvailabilitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="acdd3-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="acdd3-110">參數</span><span class="sxs-lookup"><span data-stu-id="acdd3-110">PARAMETERS</span></span>

### <span data-ttu-id="acdd3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acdd3-111">-AsJob</span></span>
<span data-ttu-id="acdd3-112">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="acdd3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="acdd3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdd3-113">-DefaultProfile</span></span>
<span data-ttu-id="acdd3-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="acdd3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acdd3-115">-位置</span><span class="sxs-lookup"><span data-stu-id="acdd3-115">-Location</span></span>
<span data-ttu-id="acdd3-116">指定可用性集的位置。</span><span class="sxs-lookup"><span data-stu-id="acdd3-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="acdd3-117">-Name</span></span>
<span data-ttu-id="acdd3-118">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="acdd3-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="acdd3-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="acdd3-120">指定平臺故障網域計數。</span><span class="sxs-lookup"><span data-stu-id="acdd3-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="acdd3-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="acdd3-122">指定平臺更新網域計數。</span><span class="sxs-lookup"><span data-stu-id="acdd3-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="acdd3-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="acdd3-124">要用於此可用性集的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="acdd3-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acdd3-125">-ResourceGroupName</span></span>
<span data-ttu-id="acdd3-126">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="acdd3-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="acdd3-127">-Sku</span></span>
<span data-ttu-id="acdd3-128">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="acdd3-128">The Name of Sku.</span></span>
<span data-ttu-id="acdd3-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="acdd3-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="acdd3-130">對齊：適用于受管理的磁片</span><span class="sxs-lookup"><span data-stu-id="acdd3-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="acdd3-131">傳統：適用于未管理磁片</span><span class="sxs-lookup"><span data-stu-id="acdd3-131">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-132">-標記</span><span class="sxs-lookup"><span data-stu-id="acdd3-132">-Tag</span></span>
<span data-ttu-id="acdd3-133">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="acdd3-133">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdd3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdd3-134">CommonParameters</span></span>
<span data-ttu-id="acdd3-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="acdd3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdd3-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acdd3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdd3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="acdd3-137">INPUTS</span></span>

### <span data-ttu-id="acdd3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="acdd3-138">System.String</span></span>

### <span data-ttu-id="acdd3-139">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="acdd3-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="acdd3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="acdd3-140">OUTPUTS</span></span>

### <span data-ttu-id="acdd3-141">Microsoft.Azure.Commands.Compute.models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acdd3-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="acdd3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="acdd3-142">NOTES</span></span>

## <span data-ttu-id="acdd3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="acdd3-143">RELATED LINKS</span></span>

[<span data-ttu-id="acdd3-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acdd3-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="acdd3-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acdd3-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


