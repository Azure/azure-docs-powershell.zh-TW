---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128875"
---
# <span data-ttu-id="90a55-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90a55-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="90a55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90a55-102">SYNOPSIS</span></span>
<span data-ttu-id="90a55-103">建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="90a55-103">Creates an application security group.</span></span>

## <span data-ttu-id="90a55-104">句法</span><span class="sxs-lookup"><span data-stu-id="90a55-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a55-105">說明</span><span class="sxs-lookup"><span data-stu-id="90a55-105">DESCRIPTION</span></span>
<span data-ttu-id="90a55-106">**新的-AzApplicationSecurityGroup** Cmdlet 會建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="90a55-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="90a55-107">示例</span><span class="sxs-lookup"><span data-stu-id="90a55-107">EXAMPLES</span></span>

### <span data-ttu-id="90a55-108">範例1</span><span class="sxs-lookup"><span data-stu-id="90a55-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="90a55-109">這個範例會建立沒有關聯性的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="90a55-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="90a55-110">一旦建立之後，就可以將網路介面中的 IP 配置納入群組中。</span><span class="sxs-lookup"><span data-stu-id="90a55-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="90a55-111">安全性規則也可能會將群組參照為其來源或目的地。</span><span class="sxs-lookup"><span data-stu-id="90a55-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="90a55-112">參數</span><span class="sxs-lookup"><span data-stu-id="90a55-112">PARAMETERS</span></span>

### <span data-ttu-id="90a55-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90a55-113">-AsJob</span></span>
<span data-ttu-id="90a55-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="90a55-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90a55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a55-115">-DefaultProfile</span></span>
<span data-ttu-id="90a55-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90a55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a55-117">-Force</span><span class="sxs-lookup"><span data-stu-id="90a55-117">-Force</span></span>
<span data-ttu-id="90a55-118">若要覆寫資源，請不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="90a55-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="90a55-119">-位置</span><span class="sxs-lookup"><span data-stu-id="90a55-119">-Location</span></span>
<span data-ttu-id="90a55-120">位置。</span><span class="sxs-lookup"><span data-stu-id="90a55-120">The location.</span></span>

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

### <span data-ttu-id="90a55-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="90a55-121">-Name</span></span>
<span data-ttu-id="90a55-122">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90a55-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="90a55-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a55-123">-ResourceGroupName</span></span>
<span data-ttu-id="90a55-124">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="90a55-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="90a55-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="90a55-125">-Tag</span></span>
<span data-ttu-id="90a55-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="90a55-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="90a55-127">-確認</span><span class="sxs-lookup"><span data-stu-id="90a55-127">-Confirm</span></span>
<span data-ttu-id="90a55-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90a55-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a55-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a55-129">-WhatIf</span></span>
<span data-ttu-id="90a55-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90a55-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a55-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90a55-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a55-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a55-132">CommonParameters</span></span>
<span data-ttu-id="90a55-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90a55-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a55-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90a55-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a55-135">輸入</span><span class="sxs-lookup"><span data-stu-id="90a55-135">INPUTS</span></span>

### <span data-ttu-id="90a55-136">System.object</span><span class="sxs-lookup"><span data-stu-id="90a55-136">System.String</span></span>

### <span data-ttu-id="90a55-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90a55-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90a55-138">輸出</span><span class="sxs-lookup"><span data-stu-id="90a55-138">OUTPUTS</span></span>

### <span data-ttu-id="90a55-139">PSApplicationSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="90a55-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="90a55-140">筆記</span><span class="sxs-lookup"><span data-stu-id="90a55-140">NOTES</span></span>

## <span data-ttu-id="90a55-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="90a55-141">RELATED LINKS</span></span>

[<span data-ttu-id="90a55-142">AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90a55-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="90a55-143">移除-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90a55-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="90a55-144">新-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90a55-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="90a55-145">附加 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90a55-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="90a55-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90a55-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="90a55-147">新-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="90a55-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="90a55-148">附加 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="90a55-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="90a55-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="90a55-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
