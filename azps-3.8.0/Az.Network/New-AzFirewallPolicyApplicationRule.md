---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796641"
---
# <span data-ttu-id="a09d6-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="a09d6-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="a09d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a09d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a09d6-103">建立新的 Azure 防火牆原則應用程式規則</span><span class="sxs-lookup"><span data-stu-id="a09d6-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="a09d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a09d6-104">SYNTAX</span></span>

### <span data-ttu-id="a09d6-105">TargetFqdn (預設) </span><span class="sxs-lookup"><span data-stu-id="a09d6-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a09d6-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="a09d6-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a09d6-107">說明</span><span class="sxs-lookup"><span data-stu-id="a09d6-107">DESCRIPTION</span></span>
<span data-ttu-id="a09d6-108">**新的-AzFirewallPolicyApplicationRule** Cmdlet 會建立 Azure 防火牆原則的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="a09d6-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="a09d6-109">示例</span><span class="sxs-lookup"><span data-stu-id="a09d6-109">EXAMPLES</span></span>

### <span data-ttu-id="a09d6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a09d6-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="a09d6-111">這個範例會建立含來源位址、通訊協定和目標 fqdn 的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="a09d6-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="a09d6-112">參數</span><span class="sxs-lookup"><span data-stu-id="a09d6-112">PARAMETERS</span></span>

### <span data-ttu-id="a09d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09d6-113">-DefaultProfile</span></span>
<span data-ttu-id="a09d6-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a09d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-115">-描述</span><span class="sxs-lookup"><span data-stu-id="a09d6-115">-Description</span></span>
<span data-ttu-id="a09d6-116">規則的描述</span><span class="sxs-lookup"><span data-stu-id="a09d6-116">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="a09d6-117">-FqdnTag</span></span>
<span data-ttu-id="a09d6-118">規則的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="a09d6-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a09d6-119">-Name</span></span>
<span data-ttu-id="a09d6-120">應用程式規則的名稱</span><span class="sxs-lookup"><span data-stu-id="a09d6-120">The name of the Application Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-121">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a09d6-121">-Protocol</span></span>
<span data-ttu-id="a09d6-122">規則的通訊協定</span><span class="sxs-lookup"><span data-stu-id="a09d6-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="a09d6-123">-SourceAddress</span></span>
<span data-ttu-id="a09d6-124">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="a09d6-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="a09d6-125">-TargetFqdn</span></span>
<span data-ttu-id="a09d6-126">規則的目標 Fqdn</span><span class="sxs-lookup"><span data-stu-id="a09d6-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a09d6-127">-Confirm</span></span>
<span data-ttu-id="a09d6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a09d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09d6-129">-WhatIf</span></span>
<span data-ttu-id="a09d6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a09d6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a09d6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a09d6-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09d6-132">CommonParameters</span></span>
<span data-ttu-id="a09d6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a09d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09d6-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a09d6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09d6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a09d6-135">INPUTS</span></span>

### <span data-ttu-id="a09d6-136">所有</span><span class="sxs-lookup"><span data-stu-id="a09d6-136">None</span></span>

## <span data-ttu-id="a09d6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a09d6-137">OUTPUTS</span></span>

### <span data-ttu-id="a09d6-138">PSAzureFirewallPolicyApplicationRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a09d6-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="a09d6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a09d6-139">NOTES</span></span>

## <span data-ttu-id="a09d6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a09d6-140">RELATED LINKS</span></span>
