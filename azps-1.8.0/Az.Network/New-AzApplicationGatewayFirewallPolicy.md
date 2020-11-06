---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 6813bf30da73f09f285151d6d309eb89b32acbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621858"
---
# <span data-ttu-id="1b2ac-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1b2ac-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="1b2ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2ac-103">建立應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="1b2ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b2ac-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2ac-106">**新的-AzApplicationGatewayFirewallPolicy** Cmdlet 會建立應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="1b2ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b2ac-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2ac-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1b2ac-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzureRmApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="1b2ac-109">這個命令會在位置 "westus" 的資源群組 "rg1" 中，建立名為 "wafResource1" 的新 Azure 應用程式閘道防火牆原則，並在 $customRule 變數中定義的自訂規則</span><span class="sxs-lookup"><span data-stu-id="1b2ac-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="1b2ac-110">參數</span><span class="sxs-lookup"><span data-stu-id="1b2ac-110">PARAMETERS</span></span>

### <span data-ttu-id="1b2ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b2ac-111">-AsJob</span></span>
<span data-ttu-id="1b2ac-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1b2ac-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b2ac-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="1b2ac-113">-CustomRule</span></span>
<span data-ttu-id="1b2ac-114">CustomRules 清單</span><span class="sxs-lookup"><span data-stu-id="1b2ac-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2ac-115">-DefaultProfile</span></span>
<span data-ttu-id="1b2ac-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b2ac-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1b2ac-117">-Force</span></span>
<span data-ttu-id="1b2ac-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="1b2ac-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1b2ac-119">-位置</span><span class="sxs-lookup"><span data-stu-id="1b2ac-119">-Location</span></span>
<span data-ttu-id="1b2ac-120">位於.</span><span class="sxs-lookup"><span data-stu-id="1b2ac-120">location.</span></span>

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

### <span data-ttu-id="1b2ac-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b2ac-121">-Name</span></span>
<span data-ttu-id="1b2ac-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-122">The resource name.</span></span>

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

### <span data-ttu-id="1b2ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="1b2ac-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-124">The resource group name.</span></span>

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

### <span data-ttu-id="1b2ac-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b2ac-125">-Tag</span></span>
<span data-ttu-id="1b2ac-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1b2ac-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1b2ac-127">-Confirm</span></span>
<span data-ttu-id="1b2ac-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b2ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2ac-129">-WhatIf</span></span>
<span data-ttu-id="1b2ac-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2ac-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b2ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2ac-132">CommonParameters</span></span>
<span data-ttu-id="1b2ac-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2ac-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b2ac-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2ac-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1b2ac-135">INPUTS</span></span>

### <span data-ttu-id="1b2ac-136">System.object</span><span class="sxs-lookup"><span data-stu-id="1b2ac-136">System.String</span></span>

### <span data-ttu-id="1b2ac-137">PSApplicationGatewayFirewallCustomRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="1b2ac-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="1b2ac-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b2ac-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b2ac-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1b2ac-139">OUTPUTS</span></span>

### <span data-ttu-id="1b2ac-140">PSApplicationGatewayWebApplicationFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1b2ac-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1b2ac-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1b2ac-141">NOTES</span></span>

## <span data-ttu-id="1b2ac-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b2ac-142">RELATED LINKS</span></span>
