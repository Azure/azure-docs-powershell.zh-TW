---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625490"
---
# <span data-ttu-id="ca83a-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca83a-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="ca83a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca83a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca83a-103">建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ca83a-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca83a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca83a-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca83a-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca83a-105">DESCRIPTION</span></span>
<span data-ttu-id="ca83a-106">**新的-AzureRmApplicationSecurityGroup** Cmdlet 會建立應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ca83a-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="ca83a-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca83a-107">EXAMPLES</span></span>

### <span data-ttu-id="ca83a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ca83a-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="ca83a-109">這個範例會建立沒有關聯性的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ca83a-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="ca83a-110">一旦建立之後，就可以將網路介面中的 IP 配置納入群組中。</span><span class="sxs-lookup"><span data-stu-id="ca83a-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="ca83a-111">安全性規則也可能會將群組參照為其來源或目的地。</span><span class="sxs-lookup"><span data-stu-id="ca83a-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="ca83a-112">參數</span><span class="sxs-lookup"><span data-stu-id="ca83a-112">PARAMETERS</span></span>

### <span data-ttu-id="ca83a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca83a-113">-DefaultProfile</span></span>
<span data-ttu-id="ca83a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca83a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca83a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca83a-115">-Force</span></span>
<span data-ttu-id="ca83a-116">若要覆寫資源，請不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ca83a-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="ca83a-117">-位置</span><span class="sxs-lookup"><span data-stu-id="ca83a-117">-Location</span></span>
<span data-ttu-id="ca83a-118">位置。</span><span class="sxs-lookup"><span data-stu-id="ca83a-118">The location.</span></span>

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

### <span data-ttu-id="ca83a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca83a-119">-Name</span></span>
<span data-ttu-id="ca83a-120">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca83a-120">The name of the application security group.</span></span>

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

### <span data-ttu-id="ca83a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca83a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca83a-122">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ca83a-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="ca83a-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca83a-123">-Tag</span></span>
<span data-ttu-id="ca83a-124">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="ca83a-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ca83a-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ca83a-125">-Confirm</span></span>
<span data-ttu-id="ca83a-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca83a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca83a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca83a-127">-WhatIf</span></span>
<span data-ttu-id="ca83a-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca83a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca83a-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca83a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca83a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca83a-130">CommonParameters</span></span>
<span data-ttu-id="ca83a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca83a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca83a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca83a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca83a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ca83a-133">INPUTS</span></span>

### <span data-ttu-id="ca83a-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ca83a-134">System.String</span></span>
<span data-ttu-id="ca83a-135">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca83a-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca83a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ca83a-136">OUTPUTS</span></span>

### <span data-ttu-id="ca83a-137">PSApplicationSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ca83a-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="ca83a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ca83a-138">NOTES</span></span>

## <span data-ttu-id="ca83a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca83a-139">RELATED LINKS</span></span>

[<span data-ttu-id="ca83a-140">AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca83a-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="ca83a-141">移除-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ca83a-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="ca83a-142">新-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca83a-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ca83a-143">附加 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca83a-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ca83a-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca83a-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ca83a-145">新-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca83a-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ca83a-146">附加 AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca83a-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ca83a-147">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca83a-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
