---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 0c7325d43ca1e1aefa2ee4751cc90369e06beca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907093"
---
# <span data-ttu-id="1f8c8-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="1f8c8-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="1f8c8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8c8-103">建立 Azure IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="1f8c8-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f8c8-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f8c8-105">描述</span><span class="sxs-lookup"><span data-stu-id="1f8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="1f8c8-106">**New-AzIpAllocation** Cmdlet 會建立 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="1f8c8-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="1f8c8-107">例子</span><span class="sxs-lookup"><span data-stu-id="1f8c8-107">EXAMPLES</span></span>

### <span data-ttu-id="1f8c8-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1f8c8-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="1f8c8-109">範例 2</span><span class="sxs-lookup"><span data-stu-id="1f8c8-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="1f8c8-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f8c8-110">PARAMETERS</span></span>

### <span data-ttu-id="1f8c8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f8c8-111">-AsJob</span></span>
<span data-ttu-id="1f8c8-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1f8c8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f8c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8c8-113">-DefaultProfile</span></span>
<span data-ttu-id="1f8c8-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f8c8-115">-強制</span><span class="sxs-lookup"><span data-stu-id="1f8c8-115">-Force</span></span>
<span data-ttu-id="1f8c8-116">如果您想要覆蓋資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="1f8c8-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="1f8c8-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="1f8c8-117">-IpAllocationTag</span></span>
<span data-ttu-id="1f8c8-118">IP 配置的配置標記</span><span class="sxs-lookup"><span data-stu-id="1f8c8-118">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="1f8c8-119">-IpAllocationType</span></span>
<span data-ttu-id="1f8c8-120">IP 配置的類型</span><span class="sxs-lookup"><span data-stu-id="1f8c8-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="1f8c8-121">-IpamAllocationId</span></span>
<span data-ttu-id="1f8c8-122">IP 配置的 ipam 分配識別碼</span><span class="sxs-lookup"><span data-stu-id="1f8c8-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="1f8c8-123">-位置</span><span class="sxs-lookup"><span data-stu-id="1f8c8-123">-Location</span></span>
<span data-ttu-id="1f8c8-124">位置。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-124">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f8c8-125">-Name</span></span>
<span data-ttu-id="1f8c8-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-127">-首碼</span><span class="sxs-lookup"><span data-stu-id="1f8c8-127">-Prefix</span></span>
<span data-ttu-id="1f8c8-128">IP 配置的首碼</span><span class="sxs-lookup"><span data-stu-id="1f8c8-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="1f8c8-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="1f8c8-129">-PrefixLength</span></span>
<span data-ttu-id="1f8c8-130">IP 配置的前置長度</span><span class="sxs-lookup"><span data-stu-id="1f8c8-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="1f8c8-131">-PrefixType</span></span>
<span data-ttu-id="1f8c8-132">IP 配置的首碼類型</span><span class="sxs-lookup"><span data-stu-id="1f8c8-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f8c8-133">-ResourceGroupName</span></span>
<span data-ttu-id="1f8c8-134">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-135">-標記</span><span class="sxs-lookup"><span data-stu-id="1f8c8-135">-Tag</span></span>
<span data-ttu-id="1f8c8-136">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-137">-確認</span><span class="sxs-lookup"><span data-stu-id="1f8c8-137">-Confirm</span></span>
<span data-ttu-id="1f8c8-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f8c8-139">-WhatIf</span></span>
<span data-ttu-id="1f8c8-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f8c8-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8c8-142">CommonParameters</span></span>
<span data-ttu-id="1f8c8-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f8c8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8c8-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f8c8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8c8-145">輸入</span><span class="sxs-lookup"><span data-stu-id="1f8c8-145">INPUTS</span></span>

### <span data-ttu-id="1f8c8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1f8c8-146">System.String</span></span>

### <span data-ttu-id="1f8c8-147">System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1f8c8-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1f8c8-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f8c8-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f8c8-149">輸出</span><span class="sxs-lookup"><span data-stu-id="1f8c8-149">OUTPUTS</span></span>

### <span data-ttu-id="1f8c8-150">Microsoft.Azure.Commands.Network.models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="1f8c8-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="1f8c8-151">筆記</span><span class="sxs-lookup"><span data-stu-id="1f8c8-151">NOTES</span></span>

## <span data-ttu-id="1f8c8-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f8c8-152">RELATED LINKS</span></span>
