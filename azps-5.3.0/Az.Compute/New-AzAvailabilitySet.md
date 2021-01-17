---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449829"
---
# <span data-ttu-id="e5b07-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e5b07-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="e5b07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5b07-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b07-103">建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="e5b07-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="e5b07-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5b07-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5b07-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5b07-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b07-106">**新的-AzAvailabilitySet** Cmdlet 會建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="e5b07-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="e5b07-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5b07-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b07-108">範例1：建立可用性集</span><span class="sxs-lookup"><span data-stu-id="e5b07-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="e5b07-109">這個命令會在名為 [ResourceGroup11] 的資源群組中建立名為 AvailabilitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="e5b07-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e5b07-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5b07-110">PARAMETERS</span></span>

### <span data-ttu-id="e5b07-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5b07-111">-AsJob</span></span>
<span data-ttu-id="e5b07-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="e5b07-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e5b07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b07-113">-DefaultProfile</span></span>
<span data-ttu-id="e5b07-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5b07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5b07-115">-位置</span><span class="sxs-lookup"><span data-stu-id="e5b07-115">-Location</span></span>
<span data-ttu-id="e5b07-116">指定可用性集的位置。</span><span class="sxs-lookup"><span data-stu-id="e5b07-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="e5b07-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5b07-117">-Name</span></span>
<span data-ttu-id="e5b07-118">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5b07-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="e5b07-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="e5b07-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="e5b07-120">指定平臺容錯網域計數。</span><span class="sxs-lookup"><span data-stu-id="e5b07-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="e5b07-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="e5b07-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="e5b07-122">指定平臺更新網域計數。</span><span class="sxs-lookup"><span data-stu-id="e5b07-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="e5b07-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e5b07-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e5b07-124">要與此可用性集搭配使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5b07-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="e5b07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5b07-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5b07-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5b07-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5b07-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="e5b07-127">-Sku</span></span>
<span data-ttu-id="e5b07-128">Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5b07-128">The Name of Sku.</span></span>
<span data-ttu-id="e5b07-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e5b07-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5b07-130">已對齊：適用于受管理的磁片</span><span class="sxs-lookup"><span data-stu-id="e5b07-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="e5b07-131">傳統：適用于非託管磁片</span><span class="sxs-lookup"><span data-stu-id="e5b07-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="e5b07-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5b07-132">-Tag</span></span>
<span data-ttu-id="e5b07-133">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e5b07-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="e5b07-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b07-134">CommonParameters</span></span>
<span data-ttu-id="e5b07-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5b07-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b07-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5b07-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b07-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e5b07-137">INPUTS</span></span>

### <span data-ttu-id="e5b07-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e5b07-138">System.String</span></span>

### <span data-ttu-id="e5b07-139">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5b07-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e5b07-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e5b07-140">OUTPUTS</span></span>

### <span data-ttu-id="e5b07-141">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="e5b07-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e5b07-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e5b07-142">NOTES</span></span>

## <span data-ttu-id="e5b07-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5b07-143">RELATED LINKS</span></span>

[<span data-ttu-id="e5b07-144">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e5b07-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="e5b07-145">移除-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e5b07-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


