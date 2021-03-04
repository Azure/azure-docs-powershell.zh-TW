---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: 69d9e49c83b2f1231be4fe2b1ffc3cba25c2cf2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912701"
---
# <span data-ttu-id="9cb94-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9cb94-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="9cb94-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9cb94-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb94-103">移除 Azure 防火牆政策</span><span class="sxs-lookup"><span data-stu-id="9cb94-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="9cb94-104">語法</span><span class="sxs-lookup"><span data-stu-id="9cb94-104">SYNTAX</span></span>

### <span data-ttu-id="9cb94-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cb94-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb94-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cb94-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb94-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cb94-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb94-108">描述</span><span class="sxs-lookup"><span data-stu-id="9cb94-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb94-109">**Remove-AzFirewallPolicy** Cmdlet 會移除 Azure 防火牆政策。</span><span class="sxs-lookup"><span data-stu-id="9cb94-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="9cb94-110">例子</span><span class="sxs-lookup"><span data-stu-id="9cb94-110">EXAMPLES</span></span>

### <span data-ttu-id="9cb94-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9cb94-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="9cb94-112">此範例會移除資源組 "TestRg" 中名為 "firewallpolicy" 的防火牆策略</span><span class="sxs-lookup"><span data-stu-id="9cb94-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="9cb94-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="9cb94-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="9cb94-114">此範例會以識別碼移除防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="9cb94-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="9cb94-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="9cb94-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="9cb94-116">此範例會移除防火牆$fp</span><span class="sxs-lookup"><span data-stu-id="9cb94-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="9cb94-117">參數</span><span class="sxs-lookup"><span data-stu-id="9cb94-117">PARAMETERS</span></span>

### <span data-ttu-id="9cb94-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cb94-118">-AsJob</span></span>
<span data-ttu-id="9cb94-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9cb94-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cb94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb94-120">-DefaultProfile</span></span>
<span data-ttu-id="9cb94-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cb94-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb94-122">-強制</span><span class="sxs-lookup"><span data-stu-id="9cb94-122">-Force</span></span>
<span data-ttu-id="9cb94-123">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="9cb94-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9cb94-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb94-124">-InputObject</span></span>
<span data-ttu-id="9cb94-125">AzureFirewall 政策</span><span class="sxs-lookup"><span data-stu-id="9cb94-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb94-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9cb94-126">-Name</span></span>
<span data-ttu-id="9cb94-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9cb94-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb94-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cb94-128">-PassThru</span></span>
<span data-ttu-id="9cb94-129">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9cb94-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cb94-130">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9cb94-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9cb94-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb94-131">-ResourceGroupName</span></span>
<span data-ttu-id="9cb94-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9cb94-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb94-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb94-133">-ResourceId</span></span>
<span data-ttu-id="9cb94-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9cb94-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb94-135">-確認</span><span class="sxs-lookup"><span data-stu-id="9cb94-135">-Confirm</span></span>
<span data-ttu-id="9cb94-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9cb94-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb94-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb94-137">-WhatIf</span></span>
<span data-ttu-id="9cb94-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9cb94-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb94-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cb94-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb94-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb94-140">CommonParameters</span></span>
<span data-ttu-id="9cb94-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9cb94-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb94-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cb94-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb94-143">輸入</span><span class="sxs-lookup"><span data-stu-id="9cb94-143">INPUTS</span></span>

### <span data-ttu-id="9cb94-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9cb94-144">System.String</span></span>

### <span data-ttu-id="9cb94-145">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9cb94-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="9cb94-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9cb94-146">OUTPUTS</span></span>

### <span data-ttu-id="9cb94-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9cb94-147">System.Boolean</span></span>

## <span data-ttu-id="9cb94-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9cb94-148">NOTES</span></span>

## <span data-ttu-id="9cb94-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cb94-149">RELATED LINKS</span></span>
