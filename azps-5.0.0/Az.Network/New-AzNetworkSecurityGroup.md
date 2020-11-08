---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139696"
---
# <span data-ttu-id="a249e-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a249e-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="a249e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a249e-102">SYNOPSIS</span></span>
<span data-ttu-id="a249e-103">建立網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a249e-103">Creates a network security group.</span></span>

## <span data-ttu-id="a249e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a249e-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a249e-105">說明</span><span class="sxs-lookup"><span data-stu-id="a249e-105">DESCRIPTION</span></span>
<span data-ttu-id="a249e-106">**新的-AzNetworkSecurityGroup** Cmdlet 會建立 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a249e-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="a249e-107">示例</span><span class="sxs-lookup"><span data-stu-id="a249e-107">EXAMPLES</span></span>

### <span data-ttu-id="a249e-108">範例1：建立新的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="a249e-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="a249e-109">這個命令會在位置 "westus" 的資源群組 "rg1" 中，建立名為 "nsg1" 的新 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a249e-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="a249e-110">範例2：建立詳細的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="a249e-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="a249e-111">步驟：1建立允許從網際網路存取到埠3389的安全規則。</span><span class="sxs-lookup"><span data-stu-id="a249e-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="a249e-112">步驟：2建立允許從網際網路存取到埠80的安全規則。</span><span class="sxs-lookup"><span data-stu-id="a249e-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="a249e-113">步驟：3將上述建立的規則新增至名為 NSG-前端的新 NSG。</span><span class="sxs-lookup"><span data-stu-id="a249e-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="a249e-114">參數</span><span class="sxs-lookup"><span data-stu-id="a249e-114">PARAMETERS</span></span>

### <span data-ttu-id="a249e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a249e-115">-AsJob</span></span>
<span data-ttu-id="a249e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a249e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a249e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a249e-117">-DefaultProfile</span></span>
<span data-ttu-id="a249e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a249e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a249e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a249e-119">-Force</span></span>
<span data-ttu-id="a249e-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a249e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a249e-121">-位置</span><span class="sxs-lookup"><span data-stu-id="a249e-121">-Location</span></span>
<span data-ttu-id="a249e-122">指定要為其建立網路安全性群組的地區。</span><span class="sxs-lookup"><span data-stu-id="a249e-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="a249e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a249e-123">-Name</span></span>
<span data-ttu-id="a249e-124">指定要建立之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a249e-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="a249e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a249e-125">-ResourceGroupName</span></span>
<span data-ttu-id="a249e-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a249e-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a249e-127">這個 Cmdlet 會在 [資源] 群組中建立此參數指定的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a249e-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a249e-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="a249e-128">-SecurityRules</span></span>
<span data-ttu-id="a249e-129">指定要在網路安全性群組中建立的網路安全規則物件清單。</span><span class="sxs-lookup"><span data-stu-id="a249e-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a249e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a249e-130">-Tag</span></span>
<span data-ttu-id="a249e-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a249e-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a249e-132">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a249e-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a249e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a249e-133">-Confirm</span></span>
<span data-ttu-id="a249e-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a249e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a249e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a249e-135">-WhatIf</span></span>
<span data-ttu-id="a249e-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a249e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a249e-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a249e-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a249e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a249e-138">CommonParameters</span></span>
<span data-ttu-id="a249e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a249e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a249e-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a249e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a249e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a249e-141">INPUTS</span></span>

### <span data-ttu-id="a249e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a249e-142">System.String</span></span>

### <span data-ttu-id="a249e-143">PSSecurityRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a249e-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="a249e-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a249e-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a249e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a249e-145">OUTPUTS</span></span>

### <span data-ttu-id="a249e-146">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a249e-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a249e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a249e-147">NOTES</span></span>

## <span data-ttu-id="a249e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a249e-148">RELATED LINKS</span></span>

[<span data-ttu-id="a249e-149">AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a249e-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a249e-150">移除-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a249e-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a249e-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a249e-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)