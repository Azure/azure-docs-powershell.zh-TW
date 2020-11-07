---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: f2d9781f205df70e5becbc53f597f27791ca6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624148"
---
# <span data-ttu-id="52ac5-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="52ac5-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="52ac5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="52ac5-103">建立網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="52ac5-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ac5-104">句法</span><span class="sxs-lookup"><span data-stu-id="52ac5-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52ac5-105">說明</span><span class="sxs-lookup"><span data-stu-id="52ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="52ac5-106">**新的-AzureRmNetworkSecurityGroup** Cmdlet 會建立 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="52ac5-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="52ac5-107">示例</span><span class="sxs-lookup"><span data-stu-id="52ac5-107">EXAMPLES</span></span>

### <span data-ttu-id="52ac5-108">1：建立新的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="52ac5-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="52ac5-109">這個命令會在位置 "westus" 的資源群組 "rg1" 中，建立名為 "nsg1" 的新 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="52ac5-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="52ac5-110">2：建立詳細的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="52ac5-110">2: Create a detailed network security group</span></span>
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

<span data-ttu-id="52ac5-111">步驟：1建立允許從網際網路存取到埠3389的安全規則。</span><span class="sxs-lookup"><span data-stu-id="52ac5-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="52ac5-112">步驟：2建立允許從網際網路存取到埠80的安全規則。</span><span class="sxs-lookup"><span data-stu-id="52ac5-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="52ac5-113">步驟：3將上述建立的規則新增至名為 NSG-前端的新 NSG。</span><span class="sxs-lookup"><span data-stu-id="52ac5-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="52ac5-114">參數</span><span class="sxs-lookup"><span data-stu-id="52ac5-114">PARAMETERS</span></span>

### <span data-ttu-id="52ac5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="52ac5-115">-Force</span></span>
<span data-ttu-id="52ac5-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="52ac5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52ac5-117">-位置</span><span class="sxs-lookup"><span data-stu-id="52ac5-117">-Location</span></span>
<span data-ttu-id="52ac5-118">指定要為其建立網路安全性群組的地區。</span><span class="sxs-lookup"><span data-stu-id="52ac5-118">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="52ac5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="52ac5-119">-Name</span></span>
<span data-ttu-id="52ac5-120">指定要建立之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52ac5-120">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="52ac5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ac5-121">-ResourceGroupName</span></span>
<span data-ttu-id="52ac5-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52ac5-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="52ac5-123">這個 Cmdlet 會在 [資源] 群組中建立此參數指定的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="52ac5-123">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52ac5-124">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="52ac5-124">-SecurityRules</span></span>
<span data-ttu-id="52ac5-125">指定要在網路安全性群組中建立的網路安全規則物件清單。</span><span class="sxs-lookup"><span data-stu-id="52ac5-125">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="52ac5-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="52ac5-126">-Tag</span></span>
<span data-ttu-id="52ac5-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="52ac5-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="52ac5-128">例如：</span><span class="sxs-lookup"><span data-stu-id="52ac5-128">For example:</span></span>

<span data-ttu-id="52ac5-129">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="52ac5-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="52ac5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="52ac5-130">-Confirm</span></span>
<span data-ttu-id="52ac5-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52ac5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ac5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ac5-132">-WhatIf</span></span>
<span data-ttu-id="52ac5-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52ac5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ac5-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52ac5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ac5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ac5-135">-DefaultProfile</span></span>
<span data-ttu-id="52ac5-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52ac5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52ac5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ac5-137">CommonParameters</span></span>
<span data-ttu-id="52ac5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52ac5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ac5-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52ac5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ac5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="52ac5-140">INPUTS</span></span>

## <span data-ttu-id="52ac5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="52ac5-141">OUTPUTS</span></span>

### <span data-ttu-id="52ac5-142">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52ac5-142">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="52ac5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="52ac5-143">NOTES</span></span>

## <span data-ttu-id="52ac5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="52ac5-144">RELATED LINKS</span></span>

[<span data-ttu-id="52ac5-145">AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="52ac5-145">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="52ac5-146">移除-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="52ac5-146">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="52ac5-147">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="52ac5-147">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
