---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 3603adcce2ce39cc4e0a2dd57869a6ca10c48998
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801253"
---
# <span data-ttu-id="9bf17-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9bf17-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="9bf17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9bf17-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf17-103">建立網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="9bf17-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bf17-104">句法</span><span class="sxs-lookup"><span data-stu-id="9bf17-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf17-105">說明</span><span class="sxs-lookup"><span data-stu-id="9bf17-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf17-106">**新的-AzureRmNetworkSecurityGroup** Cmdlet 會建立 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="9bf17-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="9bf17-107">示例</span><span class="sxs-lookup"><span data-stu-id="9bf17-107">EXAMPLES</span></span>

### <span data-ttu-id="9bf17-108">1：建立新的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="9bf17-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="9bf17-109">這個命令會在位置 "westus" 的資源群組 "rg1" 中，建立名為 "nsg1" 的新 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="9bf17-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="9bf17-110">2：建立詳細的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="9bf17-110">2: Create a detailed network security group</span></span>
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

<span data-ttu-id="9bf17-111">步驟：1建立允許從網際網路存取到埠3389的安全規則。</span><span class="sxs-lookup"><span data-stu-id="9bf17-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="9bf17-112">步驟：2建立允許從網際網路存取到埠80的安全規則。</span><span class="sxs-lookup"><span data-stu-id="9bf17-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="9bf17-113">步驟：3將上述建立的規則新增至名為 NSG-前端的新 NSG。</span><span class="sxs-lookup"><span data-stu-id="9bf17-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="9bf17-114">參數</span><span class="sxs-lookup"><span data-stu-id="9bf17-114">PARAMETERS</span></span>

### <span data-ttu-id="9bf17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf17-115">-AsJob</span></span>
<span data-ttu-id="9bf17-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9bf17-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf17-117">-DefaultProfile</span></span>
<span data-ttu-id="9bf17-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9bf17-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf17-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9bf17-119">-Force</span></span>
<span data-ttu-id="9bf17-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9bf17-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bf17-121">-位置</span><span class="sxs-lookup"><span data-stu-id="9bf17-121">-Location</span></span>
<span data-ttu-id="9bf17-122">指定要為其建立網路安全性群組的地區。</span><span class="sxs-lookup"><span data-stu-id="9bf17-122">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf17-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9bf17-123">-Name</span></span>
<span data-ttu-id="9bf17-124">指定要建立之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf17-124">Specifies the name of the network security group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf17-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf17-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bf17-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf17-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9bf17-127">這個 Cmdlet 會在 [資源] 群組中建立此參數指定的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="9bf17-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf17-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="9bf17-128">-SecurityRules</span></span>
<span data-ttu-id="9bf17-129">指定要在網路安全性群組中建立的網路安全規則物件清單。</span><span class="sxs-lookup"><span data-stu-id="9bf17-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="9bf17-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9bf17-130">-Tag</span></span>
<span data-ttu-id="9bf17-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="9bf17-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9bf17-132">例如：</span><span class="sxs-lookup"><span data-stu-id="9bf17-132">For example:</span></span>

<span data-ttu-id="9bf17-133">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9bf17-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf17-134">-確認</span><span class="sxs-lookup"><span data-stu-id="9bf17-134">-Confirm</span></span>
<span data-ttu-id="9bf17-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9bf17-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf17-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf17-136">-WhatIf</span></span>
<span data-ttu-id="9bf17-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9bf17-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf17-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bf17-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf17-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf17-139">CommonParameters</span></span>
<span data-ttu-id="9bf17-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9bf17-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf17-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9bf17-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf17-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9bf17-142">INPUTS</span></span>

## <span data-ttu-id="9bf17-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9bf17-143">OUTPUTS</span></span>

### <span data-ttu-id="9bf17-144">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9bf17-144">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9bf17-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9bf17-145">NOTES</span></span>

## <span data-ttu-id="9bf17-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bf17-146">RELATED LINKS</span></span>

[<span data-ttu-id="9bf17-147">AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9bf17-147">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="9bf17-148">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9bf17-148">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="9bf17-149">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9bf17-149">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
