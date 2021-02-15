---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142134"
---
# <span data-ttu-id="94053-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="94053-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="94053-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94053-102">SYNOPSIS</span></span>
<span data-ttu-id="94053-103">移除 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="94053-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="94053-104">句法</span><span class="sxs-lookup"><span data-stu-id="94053-104">SYNTAX</span></span>

### <span data-ttu-id="94053-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94053-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94053-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94053-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94053-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94053-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94053-108">說明</span><span class="sxs-lookup"><span data-stu-id="94053-108">DESCRIPTION</span></span>
<span data-ttu-id="94053-109">**AzFirewallPolicy** Cmdlet 會移除 Azure 防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="94053-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="94053-110">示例</span><span class="sxs-lookup"><span data-stu-id="94053-110">EXAMPLES</span></span>

### <span data-ttu-id="94053-111">範例1</span><span class="sxs-lookup"><span data-stu-id="94053-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="94053-112">這個範例會移除 resourcegroup "TestRg" 中名為 "firewallpolicy" 的防火牆原則</span><span class="sxs-lookup"><span data-stu-id="94053-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="94053-113">範例2</span><span class="sxs-lookup"><span data-stu-id="94053-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="94053-114">這個範例會依識別碼移除防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="94053-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="94053-115">範例3</span><span class="sxs-lookup"><span data-stu-id="94053-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="94053-116">這個範例會移除防火牆原則 $fp</span><span class="sxs-lookup"><span data-stu-id="94053-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="94053-117">參數</span><span class="sxs-lookup"><span data-stu-id="94053-117">PARAMETERS</span></span>

### <span data-ttu-id="94053-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94053-118">-AsJob</span></span>
<span data-ttu-id="94053-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94053-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94053-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94053-120">-DefaultProfile</span></span>
<span data-ttu-id="94053-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94053-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94053-122">-Force</span><span class="sxs-lookup"><span data-stu-id="94053-122">-Force</span></span>
<span data-ttu-id="94053-123">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="94053-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94053-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94053-124">-InputObject</span></span>
<span data-ttu-id="94053-125">AzureFirewall 原則</span><span class="sxs-lookup"><span data-stu-id="94053-125">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="94053-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="94053-126">-Name</span></span>
<span data-ttu-id="94053-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="94053-127">The resource name.</span></span>

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

### <span data-ttu-id="94053-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94053-128">-PassThru</span></span>
<span data-ttu-id="94053-129">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="94053-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94053-130">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="94053-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94053-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94053-131">-ResourceGroupName</span></span>
<span data-ttu-id="94053-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94053-132">The resource group name.</span></span>

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

### <span data-ttu-id="94053-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94053-133">-ResourceId</span></span>
<span data-ttu-id="94053-134">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="94053-134">The resource Id.</span></span>

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

### <span data-ttu-id="94053-135">-確認</span><span class="sxs-lookup"><span data-stu-id="94053-135">-Confirm</span></span>
<span data-ttu-id="94053-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94053-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94053-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94053-137">-WhatIf</span></span>
<span data-ttu-id="94053-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94053-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94053-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94053-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94053-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94053-140">CommonParameters</span></span>
<span data-ttu-id="94053-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94053-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94053-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="94053-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94053-143">輸入</span><span class="sxs-lookup"><span data-stu-id="94053-143">INPUTS</span></span>

### <span data-ttu-id="94053-144">System.object</span><span class="sxs-lookup"><span data-stu-id="94053-144">System.String</span></span>

### <span data-ttu-id="94053-145">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94053-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="94053-146">輸出</span><span class="sxs-lookup"><span data-stu-id="94053-146">OUTPUTS</span></span>

### <span data-ttu-id="94053-147">System.object</span><span class="sxs-lookup"><span data-stu-id="94053-147">System.Boolean</span></span>

## <span data-ttu-id="94053-148">筆記</span><span class="sxs-lookup"><span data-stu-id="94053-148">NOTES</span></span>

## <span data-ttu-id="94053-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="94053-149">RELATED LINKS</span></span>
