---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278559"
---
# <span data-ttu-id="4324f-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="4324f-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="4324f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4324f-102">SYNOPSIS</span></span>
<span data-ttu-id="4324f-103">建立 Azure IpAllocation。</span><span class="sxs-lookup"><span data-stu-id="4324f-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="4324f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4324f-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4324f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4324f-105">DESCRIPTION</span></span>
<span data-ttu-id="4324f-106">**新的-AzIpAllocation** Cmdlet 會建立 Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="4324f-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="4324f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4324f-107">EXAMPLES</span></span>

### <span data-ttu-id="4324f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4324f-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="4324f-109">範例2</span><span class="sxs-lookup"><span data-stu-id="4324f-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="4324f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4324f-110">PARAMETERS</span></span>

### <span data-ttu-id="4324f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4324f-111">-AsJob</span></span>
<span data-ttu-id="4324f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4324f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4324f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4324f-113">-DefaultProfile</span></span>
<span data-ttu-id="4324f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4324f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4324f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4324f-115">-Force</span></span>
<span data-ttu-id="4324f-116">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="4324f-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="4324f-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="4324f-117">-IpAllocationTag</span></span>
<span data-ttu-id="4324f-118">IP 分配的分攤標記</span><span class="sxs-lookup"><span data-stu-id="4324f-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="4324f-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="4324f-119">-IpAllocationType</span></span>
<span data-ttu-id="4324f-120">IP 分配的類型</span><span class="sxs-lookup"><span data-stu-id="4324f-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="4324f-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="4324f-121">-IpamAllocationId</span></span>
<span data-ttu-id="4324f-122">IP 分配的 ipam 配置識別碼</span><span class="sxs-lookup"><span data-stu-id="4324f-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="4324f-123">-位置</span><span class="sxs-lookup"><span data-stu-id="4324f-123">-Location</span></span>
<span data-ttu-id="4324f-124">位於.</span><span class="sxs-lookup"><span data-stu-id="4324f-124">location.</span></span>

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

### <span data-ttu-id="4324f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4324f-125">-Name</span></span>
<span data-ttu-id="4324f-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4324f-126">The resource name.</span></span>

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

### <span data-ttu-id="4324f-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4324f-127">-Prefix</span></span>
<span data-ttu-id="4324f-128">IP 分配的首碼</span><span class="sxs-lookup"><span data-stu-id="4324f-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="4324f-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="4324f-129">-PrefixLength</span></span>
<span data-ttu-id="4324f-130">IP 分配的前置長度</span><span class="sxs-lookup"><span data-stu-id="4324f-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="4324f-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="4324f-131">-PrefixType</span></span>
<span data-ttu-id="4324f-132">IP 分配的首碼類型</span><span class="sxs-lookup"><span data-stu-id="4324f-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="4324f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4324f-133">-ResourceGroupName</span></span>
<span data-ttu-id="4324f-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4324f-134">The resource group name.</span></span>

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

### <span data-ttu-id="4324f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="4324f-135">-Tag</span></span>
<span data-ttu-id="4324f-136">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="4324f-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4324f-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4324f-137">-Confirm</span></span>
<span data-ttu-id="4324f-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4324f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4324f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4324f-139">-WhatIf</span></span>
<span data-ttu-id="4324f-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4324f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4324f-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4324f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4324f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4324f-142">CommonParameters</span></span>
<span data-ttu-id="4324f-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4324f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4324f-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4324f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4324f-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4324f-145">INPUTS</span></span>

### <span data-ttu-id="4324f-146">System.object</span><span class="sxs-lookup"><span data-stu-id="4324f-146">System.String</span></span>

### <span data-ttu-id="4324f-147">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4324f-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4324f-148">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4324f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4324f-149">輸出</span><span class="sxs-lookup"><span data-stu-id="4324f-149">OUTPUTS</span></span>

### <span data-ttu-id="4324f-150">PSIpAllocation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4324f-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="4324f-151">筆記</span><span class="sxs-lookup"><span data-stu-id="4324f-151">NOTES</span></span>

## <span data-ttu-id="4324f-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="4324f-152">RELATED LINKS</span></span>
