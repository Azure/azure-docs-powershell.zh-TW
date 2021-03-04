---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 001023fd313db4228d7fb1f155b5a686f9649277
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902405"
---
# <span data-ttu-id="39ef0-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39ef0-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="39ef0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="39ef0-103">建立網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="39ef0-103">Creates a network security group.</span></span>

## <span data-ttu-id="39ef0-104">語法</span><span class="sxs-lookup"><span data-stu-id="39ef0-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ef0-105">描述</span><span class="sxs-lookup"><span data-stu-id="39ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="39ef0-106">**New-AzNetworkSecurityGroup** Cmdlet 會建立 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="39ef0-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="39ef0-107">例子</span><span class="sxs-lookup"><span data-stu-id="39ef0-107">EXAMPLES</span></span>

### <span data-ttu-id="39ef0-108">範例 1：建立新網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="39ef0-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="39ef0-109">此命令在位置 "westus" 的資源群組 "rg1" 中，建立一個名為 "nsg1" 的新 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="39ef0-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="39ef0-110">範例 2：建立詳細的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="39ef0-110">Example 2: Create a detailed network security group</span></span>
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

<span data-ttu-id="39ef0-111">步驟：1 建立允許從網際網路存取埠 3389 的安全性規則。</span><span class="sxs-lookup"><span data-stu-id="39ef0-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="39ef0-112">步驟：2 建立允許從網際網路存取埠 80 的安全性規則。</span><span class="sxs-lookup"><span data-stu-id="39ef0-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="39ef0-113">步驟：3 新增上述建立的規則至名為 NSG-FrontEnd 的新 NSG。</span><span class="sxs-lookup"><span data-stu-id="39ef0-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="39ef0-114">參數</span><span class="sxs-lookup"><span data-stu-id="39ef0-114">PARAMETERS</span></span>

### <span data-ttu-id="39ef0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39ef0-115">-AsJob</span></span>
<span data-ttu-id="39ef0-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="39ef0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39ef0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ef0-117">-DefaultProfile</span></span>
<span data-ttu-id="39ef0-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39ef0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39ef0-119">-強制</span><span class="sxs-lookup"><span data-stu-id="39ef0-119">-Force</span></span>
<span data-ttu-id="39ef0-120">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="39ef0-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="39ef0-121">-位置</span><span class="sxs-lookup"><span data-stu-id="39ef0-121">-Location</span></span>
<span data-ttu-id="39ef0-122">指定要建立網路安全性群組的區域。</span><span class="sxs-lookup"><span data-stu-id="39ef0-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="39ef0-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="39ef0-123">-Name</span></span>
<span data-ttu-id="39ef0-124">指定要建立的網路安全性群組名。</span><span class="sxs-lookup"><span data-stu-id="39ef0-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="39ef0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ef0-125">-ResourceGroupName</span></span>
<span data-ttu-id="39ef0-126">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39ef0-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="39ef0-127">此 Cmdlet 會在此參數指定的資源群組中建立網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="39ef0-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="39ef0-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="39ef0-128">-SecurityRules</span></span>
<span data-ttu-id="39ef0-129">指定在網路安全群組中建立的網路安全性規則物件清單。</span><span class="sxs-lookup"><span data-stu-id="39ef0-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="39ef0-130">-標記</span><span class="sxs-lookup"><span data-stu-id="39ef0-130">-Tag</span></span>
<span data-ttu-id="39ef0-131">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="39ef0-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="39ef0-132">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="39ef0-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="39ef0-133">-確認</span><span class="sxs-lookup"><span data-stu-id="39ef0-133">-Confirm</span></span>
<span data-ttu-id="39ef0-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="39ef0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ef0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ef0-135">-WhatIf</span></span>
<span data-ttu-id="39ef0-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39ef0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ef0-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39ef0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ef0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ef0-138">CommonParameters</span></span>
<span data-ttu-id="39ef0-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39ef0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ef0-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="39ef0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ef0-141">輸入</span><span class="sxs-lookup"><span data-stu-id="39ef0-141">INPUTS</span></span>

### <span data-ttu-id="39ef0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="39ef0-142">System.String</span></span>

### <span data-ttu-id="39ef0-143">Microsoft.Azure.Commands.Network.models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="39ef0-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="39ef0-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="39ef0-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="39ef0-145">輸出</span><span class="sxs-lookup"><span data-stu-id="39ef0-145">OUTPUTS</span></span>

### <span data-ttu-id="39ef0-146">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39ef0-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="39ef0-147">筆記</span><span class="sxs-lookup"><span data-stu-id="39ef0-147">NOTES</span></span>

## <span data-ttu-id="39ef0-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="39ef0-148">RELATED LINKS</span></span>

[<span data-ttu-id="39ef0-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39ef0-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="39ef0-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39ef0-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="39ef0-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39ef0-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
