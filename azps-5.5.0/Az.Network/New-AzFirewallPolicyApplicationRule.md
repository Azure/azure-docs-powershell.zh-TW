---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 25a81344d9d8d5b8af8eed907bce7977408515ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131266"
---
# <span data-ttu-id="e8ed4-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e8ed4-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="e8ed4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ed4-103">建立新的 Azure 防火牆原則應用程式規則</span><span class="sxs-lookup"><span data-stu-id="e8ed4-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="e8ed4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8ed4-104">SYNTAX</span></span>

### <span data-ttu-id="e8ed4-105">SourceAddressAndTargetFqdn (預設) </span><span class="sxs-lookup"><span data-stu-id="e8ed4-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ed4-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e8ed4-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ed4-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="e8ed4-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ed4-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="e8ed4-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ed4-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="e8ed4-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ed4-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e8ed4-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ed4-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e8ed4-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ed4-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="e8ed4-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ed4-113">說明</span><span class="sxs-lookup"><span data-stu-id="e8ed4-113">DESCRIPTION</span></span>
<span data-ttu-id="e8ed4-114">**新的-AzFirewallPolicyApplicationRule** Cmdlet 會建立 Azure 防火牆原則的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="e8ed4-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e8ed4-115">示例</span><span class="sxs-lookup"><span data-stu-id="e8ed4-115">EXAMPLES</span></span>

### <span data-ttu-id="e8ed4-116">範例1</span><span class="sxs-lookup"><span data-stu-id="e8ed4-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="e8ed4-117">這個範例會建立含來源位址、通訊協定和目標 fqdn 的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="e8ed4-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="e8ed4-118">範例2</span><span class="sxs-lookup"><span data-stu-id="e8ed4-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="e8ed4-119">這個範例會建立含來源位址、通訊協定和網頁類別的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="e8ed4-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="e8ed4-120">參數</span><span class="sxs-lookup"><span data-stu-id="e8ed4-120">PARAMETERS</span></span>

### <span data-ttu-id="e8ed4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ed4-121">-DefaultProfile</span></span>
<span data-ttu-id="e8ed4-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8ed4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ed4-123">-描述</span><span class="sxs-lookup"><span data-stu-id="e8ed4-123">-Description</span></span>
<span data-ttu-id="e8ed4-124">規則的描述</span><span class="sxs-lookup"><span data-stu-id="e8ed4-124">The description of the rule</span></span>

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

### <span data-ttu-id="e8ed4-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e8ed4-125">-FqdnTag</span></span>
<span data-ttu-id="e8ed4-126">規則的 FQDN 標記</span><span class="sxs-lookup"><span data-stu-id="e8ed4-126">The FQDN Tags of the rule</span></span>

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

### <span data-ttu-id="e8ed4-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8ed4-127">-Name</span></span>
<span data-ttu-id="e8ed4-128">應用程式規則的名稱</span><span class="sxs-lookup"><span data-stu-id="e8ed4-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="e8ed4-129">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="e8ed4-129">-Protocol</span></span>
<span data-ttu-id="e8ed4-130">規則的通訊協定</span><span class="sxs-lookup"><span data-stu-id="e8ed4-130">The protocols of the rule</span></span>

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

### <span data-ttu-id="e8ed4-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e8ed4-131">-SourceAddress</span></span>
<span data-ttu-id="e8ed4-132">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="e8ed4-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="e8ed4-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e8ed4-133">-SourceIpGroup</span></span>
<span data-ttu-id="e8ed4-134">規則的來源 ipgroups</span><span class="sxs-lookup"><span data-stu-id="e8ed4-134">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="e8ed4-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e8ed4-135">-TargetFqdn</span></span>
<span data-ttu-id="e8ed4-136">規則的目標 Fqdn</span><span class="sxs-lookup"><span data-stu-id="e8ed4-136">The target FQDNs of the rule</span></span>

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

### <span data-ttu-id="e8ed4-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="e8ed4-137">-WebCategory</span></span>
<span data-ttu-id="e8ed4-138">規則的網頁類別</span><span class="sxs-lookup"><span data-stu-id="e8ed4-138">The Web Categories of the rule</span></span>

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

### <span data-ttu-id="e8ed4-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e8ed4-139">-TargetUrl</span></span>
<span data-ttu-id="e8ed4-140">規則的目標 Url</span><span class="sxs-lookup"><span data-stu-id="e8ed4-140">The Target Url of the rule</span></span>

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

### <span data-ttu-id="e8ed4-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="e8ed4-141">-TerminateTLS</span></span>
<span data-ttu-id="e8ed4-142">指示端接 TLS</span><span class="sxs-lookup"><span data-stu-id="e8ed4-142">Indicates terminating TLS</span></span>

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

### <span data-ttu-id="e8ed4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ed4-143">CommonParameters</span></span>
<span data-ttu-id="e8ed4-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8ed4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ed4-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8ed4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ed4-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e8ed4-146">INPUTS</span></span>

### <span data-ttu-id="e8ed4-147">所有</span><span class="sxs-lookup"><span data-stu-id="e8ed4-147">None</span></span>

## <span data-ttu-id="e8ed4-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e8ed4-148">OUTPUTS</span></span>

### <span data-ttu-id="e8ed4-149">PSAzureFirewallPolicyApplicationRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8ed4-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="e8ed4-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e8ed4-150">NOTES</span></span>

## <span data-ttu-id="e8ed4-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8ed4-151">RELATED LINKS</span></span>
