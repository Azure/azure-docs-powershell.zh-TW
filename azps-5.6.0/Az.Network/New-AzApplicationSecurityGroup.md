---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: d0fcdff243294210449eb32f99faa3d9d74cef0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908401"
---
# <span data-ttu-id="eb76b-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="eb76b-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="eb76b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb76b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb76b-103">建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="eb76b-103">Creates an application security group.</span></span>

## <span data-ttu-id="eb76b-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb76b-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb76b-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb76b-105">DESCRIPTION</span></span>
<span data-ttu-id="eb76b-106">**New-AzApplicationSecurityGroup** Cmdlet 會建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="eb76b-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="eb76b-107">例子</span><span class="sxs-lookup"><span data-stu-id="eb76b-107">EXAMPLES</span></span>

### <span data-ttu-id="eb76b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="eb76b-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="eb76b-109">此範例會建立沒有關聯的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="eb76b-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="eb76b-110">建立之後，網路介面中的 IP 組就可以包含在群組中。</span><span class="sxs-lookup"><span data-stu-id="eb76b-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="eb76b-111">安全性規則也可能將群組視為其來源或目的地。</span><span class="sxs-lookup"><span data-stu-id="eb76b-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="eb76b-112">參數</span><span class="sxs-lookup"><span data-stu-id="eb76b-112">PARAMETERS</span></span>

### <span data-ttu-id="eb76b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb76b-113">-AsJob</span></span>
<span data-ttu-id="eb76b-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eb76b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb76b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb76b-115">-DefaultProfile</span></span>
<span data-ttu-id="eb76b-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb76b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb76b-117">-強制</span><span class="sxs-lookup"><span data-stu-id="eb76b-117">-Force</span></span>
<span data-ttu-id="eb76b-118">如果您想要覆寫資源，請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="eb76b-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="eb76b-119">-位置</span><span class="sxs-lookup"><span data-stu-id="eb76b-119">-Location</span></span>
<span data-ttu-id="eb76b-120">位置。</span><span class="sxs-lookup"><span data-stu-id="eb76b-120">The location.</span></span>

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

### <span data-ttu-id="eb76b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb76b-121">-Name</span></span>
<span data-ttu-id="eb76b-122">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb76b-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="eb76b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb76b-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb76b-124">應用程式安全性群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="eb76b-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="eb76b-125">-標記</span><span class="sxs-lookup"><span data-stu-id="eb76b-125">-Tag</span></span>
<span data-ttu-id="eb76b-126">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eb76b-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="eb76b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="eb76b-127">-Confirm</span></span>
<span data-ttu-id="eb76b-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eb76b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb76b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb76b-129">-WhatIf</span></span>
<span data-ttu-id="eb76b-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb76b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb76b-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb76b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb76b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb76b-132">CommonParameters</span></span>
<span data-ttu-id="eb76b-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb76b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb76b-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eb76b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb76b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="eb76b-135">INPUTS</span></span>

### <span data-ttu-id="eb76b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eb76b-136">System.String</span></span>

### <span data-ttu-id="eb76b-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eb76b-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eb76b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="eb76b-138">OUTPUTS</span></span>

### <span data-ttu-id="eb76b-139">Microsoft.Azure.Commands.Network.models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="eb76b-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="eb76b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="eb76b-140">NOTES</span></span>

## <span data-ttu-id="eb76b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb76b-141">RELATED LINKS</span></span>

[<span data-ttu-id="eb76b-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="eb76b-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="eb76b-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="eb76b-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="eb76b-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eb76b-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="eb76b-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eb76b-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="eb76b-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eb76b-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="eb76b-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb76b-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="eb76b-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb76b-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="eb76b-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb76b-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
