---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 1ffcad92a50cc332fdcab71337112b8d0c436388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450230"
---
# <span data-ttu-id="d74bd-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d74bd-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="d74bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d74bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d74bd-103">建立網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d74bd-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d74bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="d74bd-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d74bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="d74bd-105">DESCRIPTION</span></span>
<span data-ttu-id="d74bd-106">**新的-AzureRmNetworkSecurityGroup** Cmdlet 會建立 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d74bd-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="d74bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="d74bd-107">EXAMPLES</span></span>

### <span data-ttu-id="d74bd-108">1：建立新的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="d74bd-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="d74bd-109">這個命令會在位置 "westus" 的資源群組 "rg1" 中，建立名為 "nsg1" 的新 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d74bd-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="d74bd-110">2：建立詳細的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="d74bd-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="d74bd-111">步驟：1建立允許從網際網路存取到埠3389的安全規則。</span><span class="sxs-lookup"><span data-stu-id="d74bd-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="d74bd-112">步驟：2建立允許從網際網路存取到埠80的安全規則。</span><span class="sxs-lookup"><span data-stu-id="d74bd-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="d74bd-113">步驟：3將上述建立的規則新增至名為 NSG-前端的新 NSG。</span><span class="sxs-lookup"><span data-stu-id="d74bd-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="d74bd-114">參數</span><span class="sxs-lookup"><span data-stu-id="d74bd-114">PARAMETERS</span></span>

### <span data-ttu-id="d74bd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d74bd-115">-AsJob</span></span>
<span data-ttu-id="d74bd-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d74bd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d74bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74bd-117">-DefaultProfile</span></span>
<span data-ttu-id="d74bd-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d74bd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74bd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d74bd-119">-Force</span></span>
<span data-ttu-id="d74bd-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d74bd-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d74bd-121">-位置</span><span class="sxs-lookup"><span data-stu-id="d74bd-121">-Location</span></span>
<span data-ttu-id="d74bd-122">指定要為其建立網路安全性群組的地區。</span><span class="sxs-lookup"><span data-stu-id="d74bd-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="d74bd-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="d74bd-123">-Name</span></span>
<span data-ttu-id="d74bd-124">指定要建立之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d74bd-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="d74bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="d74bd-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d74bd-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d74bd-127">這個 Cmdlet 會在 [資源] 群組中建立此參數指定的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d74bd-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d74bd-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="d74bd-128">-SecurityRules</span></span>
<span data-ttu-id="d74bd-129">指定要在網路安全性群組中建立的網路安全規則物件清單。</span><span class="sxs-lookup"><span data-stu-id="d74bd-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d74bd-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d74bd-130">-Tag</span></span>
<span data-ttu-id="d74bd-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d74bd-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d74bd-132">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d74bd-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d74bd-133">-確認</span><span class="sxs-lookup"><span data-stu-id="d74bd-133">-Confirm</span></span>
<span data-ttu-id="d74bd-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d74bd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74bd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74bd-135">-WhatIf</span></span>
<span data-ttu-id="d74bd-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d74bd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74bd-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d74bd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74bd-138">CommonParameters</span></span>
<span data-ttu-id="d74bd-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d74bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74bd-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d74bd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74bd-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d74bd-141">INPUTS</span></span>

### <span data-ttu-id="d74bd-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d74bd-142">System.String</span></span>

### <span data-ttu-id="d74bd-143">[System.object]. 清單 ' 1 [PSSecurityRule，6.4.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="d74bd-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSecurityRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d74bd-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d74bd-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d74bd-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d74bd-145">OUTPUTS</span></span>

### <span data-ttu-id="d74bd-146">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d74bd-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d74bd-147">筆記</span><span class="sxs-lookup"><span data-stu-id="d74bd-147">NOTES</span></span>

## <span data-ttu-id="d74bd-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="d74bd-148">RELATED LINKS</span></span>

[<span data-ttu-id="d74bd-149">AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d74bd-149">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="d74bd-150">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d74bd-150">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="d74bd-151">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d74bd-151">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
