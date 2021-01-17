---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286900"
---
# <span data-ttu-id="dacd0-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="dacd0-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="dacd0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dacd0-102">SYNOPSIS</span></span>
<span data-ttu-id="dacd0-103">建立 Azure IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="dacd0-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="dacd0-104">句法</span><span class="sxs-lookup"><span data-stu-id="dacd0-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dacd0-105">說明</span><span class="sxs-lookup"><span data-stu-id="dacd0-105">DESCRIPTION</span></span>
<span data-ttu-id="dacd0-106">**新的-AzIpAllocation** Cmdlet 會建立 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="dacd0-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="dacd0-107">示例</span><span class="sxs-lookup"><span data-stu-id="dacd0-107">EXAMPLES</span></span>

### <span data-ttu-id="dacd0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dacd0-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="dacd0-109">範例2</span><span class="sxs-lookup"><span data-stu-id="dacd0-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="dacd0-110">參數</span><span class="sxs-lookup"><span data-stu-id="dacd0-110">PARAMETERS</span></span>

### <span data-ttu-id="dacd0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dacd0-111">-AsJob</span></span>
<span data-ttu-id="dacd0-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dacd0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dacd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacd0-113">-DefaultProfile</span></span>
<span data-ttu-id="dacd0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dacd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dacd0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dacd0-115">-Force</span></span>
<span data-ttu-id="dacd0-116">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="dacd0-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="dacd0-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="dacd0-117">-IpAllocationTag</span></span>
<span data-ttu-id="dacd0-118">IP 分配的分攤標記</span><span class="sxs-lookup"><span data-stu-id="dacd0-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="dacd0-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="dacd0-119">-IpAllocationType</span></span>
<span data-ttu-id="dacd0-120">IP 分配的類型</span><span class="sxs-lookup"><span data-stu-id="dacd0-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="dacd0-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="dacd0-121">-IpamAllocationId</span></span>
<span data-ttu-id="dacd0-122">IP 分配的 ipam 配置識別碼</span><span class="sxs-lookup"><span data-stu-id="dacd0-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="dacd0-123">-位置</span><span class="sxs-lookup"><span data-stu-id="dacd0-123">-Location</span></span>
<span data-ttu-id="dacd0-124">位於.</span><span class="sxs-lookup"><span data-stu-id="dacd0-124">location.</span></span>

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

### <span data-ttu-id="dacd0-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="dacd0-125">-Name</span></span>
<span data-ttu-id="dacd0-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dacd0-126">The resource name.</span></span>

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

### <span data-ttu-id="dacd0-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="dacd0-127">-Prefix</span></span>
<span data-ttu-id="dacd0-128">IP 分配的首碼</span><span class="sxs-lookup"><span data-stu-id="dacd0-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="dacd0-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="dacd0-129">-PrefixLength</span></span>
<span data-ttu-id="dacd0-130">IP 分配的前置長度</span><span class="sxs-lookup"><span data-stu-id="dacd0-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="dacd0-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="dacd0-131">-PrefixType</span></span>
<span data-ttu-id="dacd0-132">IP 分配的首碼類型</span><span class="sxs-lookup"><span data-stu-id="dacd0-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="dacd0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacd0-133">-ResourceGroupName</span></span>
<span data-ttu-id="dacd0-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dacd0-134">The resource group name.</span></span>

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

### <span data-ttu-id="dacd0-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="dacd0-135">-Tag</span></span>
<span data-ttu-id="dacd0-136">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="dacd0-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="dacd0-137">-確認</span><span class="sxs-lookup"><span data-stu-id="dacd0-137">-Confirm</span></span>
<span data-ttu-id="dacd0-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dacd0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacd0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacd0-139">-WhatIf</span></span>
<span data-ttu-id="dacd0-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dacd0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dacd0-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dacd0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacd0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacd0-142">CommonParameters</span></span>
<span data-ttu-id="dacd0-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dacd0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacd0-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dacd0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacd0-145">輸入</span><span class="sxs-lookup"><span data-stu-id="dacd0-145">INPUTS</span></span>

### <span data-ttu-id="dacd0-146">System.object</span><span class="sxs-lookup"><span data-stu-id="dacd0-146">System.String</span></span>

### <span data-ttu-id="dacd0-147">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dacd0-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dacd0-148">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dacd0-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dacd0-149">輸出</span><span class="sxs-lookup"><span data-stu-id="dacd0-149">OUTPUTS</span></span>

### <span data-ttu-id="dacd0-150">PSIpAllocation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dacd0-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="dacd0-151">筆記</span><span class="sxs-lookup"><span data-stu-id="dacd0-151">NOTES</span></span>

## <span data-ttu-id="dacd0-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="dacd0-152">RELATED LINKS</span></span>
