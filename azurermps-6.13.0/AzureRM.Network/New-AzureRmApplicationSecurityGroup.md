---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 359b98d19edfdbdd3c1ce8d6ab7286f13cf5dbfa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626378"
---
# <span data-ttu-id="d2c0f-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d2c0f-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="d2c0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c0f-103">建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2c0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2c0f-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2c0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c0f-106">**新的-AzureRmApplicationSecurityGroup** Cmdlet 會建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="d2c0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="d2c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c0f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d2c0f-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="d2c0f-109">這個範例會建立沒有關聯性的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="d2c0f-110">一旦建立之後，就可以將網路介面中的 IP 配置納入群組中。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="d2c0f-111">安全性規則也可能會將群組參照為其來源或目的地。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="d2c0f-112">參數</span><span class="sxs-lookup"><span data-stu-id="d2c0f-112">PARAMETERS</span></span>

### <span data-ttu-id="d2c0f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2c0f-113">-AsJob</span></span>
<span data-ttu-id="d2c0f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d2c0f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2c0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c0f-115">-DefaultProfile</span></span>
<span data-ttu-id="d2c0f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2c0f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d2c0f-117">-Force</span></span>
<span data-ttu-id="d2c0f-118">若要覆寫資源，請不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="d2c0f-119">-位置</span><span class="sxs-lookup"><span data-stu-id="d2c0f-119">-Location</span></span>
<span data-ttu-id="d2c0f-120">位置。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-120">The location.</span></span>

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

### <span data-ttu-id="d2c0f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2c0f-121">-Name</span></span>
<span data-ttu-id="d2c0f-122">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="d2c0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2c0f-124">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="d2c0f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2c0f-125">-Tag</span></span>
<span data-ttu-id="d2c0f-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d2c0f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d2c0f-127">-Confirm</span></span>
<span data-ttu-id="d2c0f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c0f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c0f-129">-WhatIf</span></span>
<span data-ttu-id="d2c0f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c0f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c0f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c0f-132">CommonParameters</span></span>
<span data-ttu-id="d2c0f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c0f-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c0f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d2c0f-135">INPUTS</span></span>

### <span data-ttu-id="d2c0f-136">System.object</span><span class="sxs-lookup"><span data-stu-id="d2c0f-136">System.String</span></span>

### <span data-ttu-id="d2c0f-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2c0f-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d2c0f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d2c0f-138">OUTPUTS</span></span>

### <span data-ttu-id="d2c0f-139">PSApplicationSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d2c0f-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="d2c0f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d2c0f-140">NOTES</span></span>

## <span data-ttu-id="d2c0f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2c0f-141">RELATED LINKS</span></span>

[<span data-ttu-id="d2c0f-142">AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d2c0f-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="d2c0f-143">移除-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d2c0f-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="d2c0f-144">新-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2c0f-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d2c0f-145">附加 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2c0f-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d2c0f-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2c0f-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d2c0f-147">新-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2c0f-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d2c0f-148">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2c0f-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d2c0f-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2c0f-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
