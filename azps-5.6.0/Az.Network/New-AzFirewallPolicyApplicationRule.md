---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 0c7e29b0c9b59842e885cf8763da63c2d65cfff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914733"
---
# <span data-ttu-id="dfb41-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="dfb41-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="dfb41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dfb41-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb41-103">建立新 Azure 防火牆原則應用程式規則</span><span class="sxs-lookup"><span data-stu-id="dfb41-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="dfb41-104">語法</span><span class="sxs-lookup"><span data-stu-id="dfb41-104">SYNTAX</span></span>

### <span data-ttu-id="dfb41-105">SourceAddressAndTargetFqdn (預設) </span><span class="sxs-lookup"><span data-stu-id="dfb41-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb41-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="dfb41-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb41-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="dfb41-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb41-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="dfb41-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb41-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="dfb41-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb41-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="dfb41-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb41-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="dfb41-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb41-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="dfb41-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfb41-113">描述</span><span class="sxs-lookup"><span data-stu-id="dfb41-113">DESCRIPTION</span></span>
<span data-ttu-id="dfb41-114">**New-AzFirewallPolicyApplicationRule** Cmdlet 會建立 Azure 防火牆原則的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="dfb41-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="dfb41-115">例子</span><span class="sxs-lookup"><span data-stu-id="dfb41-115">EXAMPLES</span></span>

### <span data-ttu-id="dfb41-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="dfb41-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="dfb41-117">此範例會建立具有來源位址、通訊協定和目標 fqdns 的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="dfb41-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="dfb41-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="dfb41-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="dfb41-119">此範例會建立具有來源位址、通訊協定和 Web 類別的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="dfb41-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="dfb41-120">參數</span><span class="sxs-lookup"><span data-stu-id="dfb41-120">PARAMETERS</span></span>

### <span data-ttu-id="dfb41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb41-121">-DefaultProfile</span></span>
<span data-ttu-id="dfb41-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfb41-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb41-123">-描述</span><span class="sxs-lookup"><span data-stu-id="dfb41-123">-Description</span></span>
<span data-ttu-id="dfb41-124">規則的描述</span><span class="sxs-lookup"><span data-stu-id="dfb41-124">The description of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="dfb41-125">-FqdnTag</span></span>
<span data-ttu-id="dfb41-126">規則的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="dfb41-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="dfb41-127">-Name</span></span>
<span data-ttu-id="dfb41-128">應用程式規則的名稱</span><span class="sxs-lookup"><span data-stu-id="dfb41-128">The name of the Application Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-129">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfb41-129">-Protocol</span></span>
<span data-ttu-id="dfb41-130">規則的通訊協定</span><span class="sxs-lookup"><span data-stu-id="dfb41-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="dfb41-131">-SourceAddress</span></span>
<span data-ttu-id="dfb41-132">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="dfb41-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="dfb41-133">-SourceIpGroup</span></span>
<span data-ttu-id="dfb41-134">規則的來源 ipgroups</span><span class="sxs-lookup"><span data-stu-id="dfb41-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="dfb41-135">-TargetFqdn</span></span>
<span data-ttu-id="dfb41-136">規則的目標 FQNS</span><span class="sxs-lookup"><span data-stu-id="dfb41-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="dfb41-137">-WebCategory</span></span>
<span data-ttu-id="dfb41-138">規則的 Web 類別</span><span class="sxs-lookup"><span data-stu-id="dfb41-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="dfb41-139">-TargetUrl</span></span>
<span data-ttu-id="dfb41-140">規則的目標 URL</span><span class="sxs-lookup"><span data-stu-id="dfb41-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-141">-終止TLS</span><span class="sxs-lookup"><span data-stu-id="dfb41-141">-TerminateTLS</span></span>
<span data-ttu-id="dfb41-142">表示終止 TLS</span><span class="sxs-lookup"><span data-stu-id="dfb41-142">Indicates terminating TLS</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb41-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb41-143">CommonParameters</span></span>
<span data-ttu-id="dfb41-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dfb41-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb41-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfb41-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb41-146">輸入</span><span class="sxs-lookup"><span data-stu-id="dfb41-146">INPUTS</span></span>

### <span data-ttu-id="dfb41-147">沒有</span><span class="sxs-lookup"><span data-stu-id="dfb41-147">None</span></span>

## <span data-ttu-id="dfb41-148">輸出</span><span class="sxs-lookup"><span data-stu-id="dfb41-148">OUTPUTS</span></span>

### <span data-ttu-id="dfb41-149">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="dfb41-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="dfb41-150">筆記</span><span class="sxs-lookup"><span data-stu-id="dfb41-150">NOTES</span></span>

## <span data-ttu-id="dfb41-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfb41-151">RELATED LINKS</span></span>
