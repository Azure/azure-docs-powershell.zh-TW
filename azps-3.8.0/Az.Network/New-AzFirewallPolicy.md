---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796662"
---
# <span data-ttu-id="bcbbf-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bcbbf-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="bcbbf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbbf-103">建立新的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="bcbbf-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="bcbbf-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcbbf-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcbbf-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcbbf-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbbf-106">**新的-AzFirewallPolicy** Cmdlet 會建立 Azure 防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="bcbbf-107">示例</span><span class="sxs-lookup"><span data-stu-id="bcbbf-107">EXAMPLES</span></span>

### <span data-ttu-id="bcbbf-108">1. 建立空白原則</span><span class="sxs-lookup"><span data-stu-id="bcbbf-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="bcbbf-109">這個範例會建立 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="bcbbf-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="bcbbf-110">2. 使用 ThreatIntel 模式建立空原則</span><span class="sxs-lookup"><span data-stu-id="bcbbf-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="bcbbf-111">這個範例會建立含威脅英特爾模式的 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="bcbbf-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="bcbbf-112">參數</span><span class="sxs-lookup"><span data-stu-id="bcbbf-112">PARAMETERS</span></span>

### <span data-ttu-id="bcbbf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcbbf-113">-AsJob</span></span>
<span data-ttu-id="bcbbf-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bcbbf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcbbf-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="bcbbf-115">-BasePolicy</span></span>
<span data-ttu-id="bcbbf-116">威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-116">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="bcbbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbbf-117">-DefaultProfile</span></span>
<span data-ttu-id="bcbbf-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcbbf-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bcbbf-119">-Force</span></span>
<span data-ttu-id="bcbbf-120">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="bcbbf-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bcbbf-121">-位置</span><span class="sxs-lookup"><span data-stu-id="bcbbf-121">-Location</span></span>
<span data-ttu-id="bcbbf-122">位於.</span><span class="sxs-lookup"><span data-stu-id="bcbbf-122">location.</span></span>

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

### <span data-ttu-id="bcbbf-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcbbf-123">-Name</span></span>
<span data-ttu-id="bcbbf-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-124">The resource name.</span></span>

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

### <span data-ttu-id="bcbbf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbbf-125">-ResourceGroupName</span></span>
<span data-ttu-id="bcbbf-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-126">The resource group name.</span></span>

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

### <span data-ttu-id="bcbbf-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="bcbbf-127">-Tag</span></span>
<span data-ttu-id="bcbbf-128">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bcbbf-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="bcbbf-129">-ThreatIntelMode</span></span>
<span data-ttu-id="bcbbf-130">威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-130">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="bcbbf-131">-確認</span><span class="sxs-lookup"><span data-stu-id="bcbbf-131">-Confirm</span></span>
<span data-ttu-id="bcbbf-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcbbf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcbbf-133">-WhatIf</span></span>
<span data-ttu-id="bcbbf-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcbbf-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcbbf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbbf-136">CommonParameters</span></span>
<span data-ttu-id="bcbbf-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbbf-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bcbbf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbbf-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bcbbf-139">INPUTS</span></span>

### <span data-ttu-id="bcbbf-140">System.object</span><span class="sxs-lookup"><span data-stu-id="bcbbf-140">System.String</span></span>

### <span data-ttu-id="bcbbf-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bcbbf-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bcbbf-142">輸出</span><span class="sxs-lookup"><span data-stu-id="bcbbf-142">OUTPUTS</span></span>

### <span data-ttu-id="bcbbf-143">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bcbbf-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="bcbbf-144">筆記</span><span class="sxs-lookup"><span data-stu-id="bcbbf-144">NOTES</span></span>

## <span data-ttu-id="bcbbf-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcbbf-145">RELATED LINKS</span></span>
