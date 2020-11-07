---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958452"
---
# <span data-ttu-id="afb3f-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="afb3f-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="afb3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="afb3f-103">儲存已修改的 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="afb3f-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="afb3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="afb3f-104">SYNTAX</span></span>

### <span data-ttu-id="afb3f-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="afb3f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb3f-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afb3f-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb3f-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afb3f-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afb3f-108">說明</span><span class="sxs-lookup"><span data-stu-id="afb3f-108">DESCRIPTION</span></span>
<span data-ttu-id="afb3f-109">**AzFirewallPolicy** Cmdlet 會更新 Azure 防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="afb3f-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="afb3f-110">示例</span><span class="sxs-lookup"><span data-stu-id="afb3f-110">EXAMPLES</span></span>

### <span data-ttu-id="afb3f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="afb3f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="afb3f-112">這個範例會將防火牆原則設定為新的防火牆原則值</span><span class="sxs-lookup"><span data-stu-id="afb3f-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="afb3f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="afb3f-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="afb3f-114">這個範例會將防火牆原則設定為新的威脅（英特爾）模式</span><span class="sxs-lookup"><span data-stu-id="afb3f-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="afb3f-115">參數</span><span class="sxs-lookup"><span data-stu-id="afb3f-115">PARAMETERS</span></span>

### <span data-ttu-id="afb3f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afb3f-116">-AsJob</span></span>
<span data-ttu-id="afb3f-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="afb3f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afb3f-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="afb3f-118">-BasePolicy</span></span>
<span data-ttu-id="afb3f-119">要從其繼承的基本原則</span><span class="sxs-lookup"><span data-stu-id="afb3f-119">The base policy to inherit from</span></span>

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

### <span data-ttu-id="afb3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb3f-120">-DefaultProfile</span></span>
<span data-ttu-id="afb3f-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="afb3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb3f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afb3f-122">-InputObject</span></span>
<span data-ttu-id="afb3f-123">AzureFirewall 原則</span><span class="sxs-lookup"><span data-stu-id="afb3f-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afb3f-124">-位置</span><span class="sxs-lookup"><span data-stu-id="afb3f-124">-Location</span></span>
<span data-ttu-id="afb3f-125">位於.</span><span class="sxs-lookup"><span data-stu-id="afb3f-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb3f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="afb3f-126">-Name</span></span>
<span data-ttu-id="afb3f-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="afb3f-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb3f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb3f-128">-ResourceGroupName</span></span>
<span data-ttu-id="afb3f-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="afb3f-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb3f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afb3f-130">-ResourceId</span></span>
<span data-ttu-id="afb3f-131">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="afb3f-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb3f-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="afb3f-132">-Tag</span></span>
<span data-ttu-id="afb3f-133">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="afb3f-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="afb3f-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="afb3f-134">-ThreatIntelMode</span></span>
<span data-ttu-id="afb3f-135">威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="afb3f-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb3f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="afb3f-136">-Confirm</span></span>
<span data-ttu-id="afb3f-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="afb3f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb3f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb3f-138">-WhatIf</span></span>
<span data-ttu-id="afb3f-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afb3f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb3f-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afb3f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb3f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb3f-141">CommonParameters</span></span>
<span data-ttu-id="afb3f-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afb3f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb3f-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="afb3f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb3f-144">輸入</span><span class="sxs-lookup"><span data-stu-id="afb3f-144">INPUTS</span></span>

### <span data-ttu-id="afb3f-145">System.object</span><span class="sxs-lookup"><span data-stu-id="afb3f-145">System.String</span></span>

### <span data-ttu-id="afb3f-146">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="afb3f-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="afb3f-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="afb3f-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="afb3f-148">輸出</span><span class="sxs-lookup"><span data-stu-id="afb3f-148">OUTPUTS</span></span>

### <span data-ttu-id="afb3f-149">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="afb3f-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="afb3f-150">筆記</span><span class="sxs-lookup"><span data-stu-id="afb3f-150">NOTES</span></span>

## <span data-ttu-id="afb3f-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="afb3f-151">RELATED LINKS</span></span>
