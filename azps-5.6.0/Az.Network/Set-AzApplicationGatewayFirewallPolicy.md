---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e6b9c873110118392e9380418276bfa0f4d938a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909349"
---
# <span data-ttu-id="5a109-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5a109-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="5a109-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a109-102">SYNOPSIS</span></span>
<span data-ttu-id="5a109-103">更新應用程式閘道防火牆政策。</span><span class="sxs-lookup"><span data-stu-id="5a109-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="5a109-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a109-104">SYNTAX</span></span>

### <span data-ttu-id="5a109-105">ByFactoryObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5a109-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a109-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="5a109-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a109-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a109-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a109-108">描述</span><span class="sxs-lookup"><span data-stu-id="5a109-108">DESCRIPTION</span></span>
<span data-ttu-id="5a109-109">**Set-AzApplicationGatewayFirewallPolicy** Cmdlet 會更新 Azure 應用程式閘道防火牆政策。</span><span class="sxs-lookup"><span data-stu-id="5a109-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="5a109-110">例子</span><span class="sxs-lookup"><span data-stu-id="5a109-110">EXAMPLES</span></span>

### <span data-ttu-id="5a109-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a109-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="5a109-112">此命令會使用 $AppGwFirewallPolicy 變數中的設定來更新應用程式閘道防火牆$UpdatedAppGwFirewallPolicy變數中儲存更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="5a109-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="5a109-113">參數</span><span class="sxs-lookup"><span data-stu-id="5a109-113">PARAMETERS</span></span>

### <span data-ttu-id="5a109-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a109-114">-AsJob</span></span>
<span data-ttu-id="5a109-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a109-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a109-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="5a109-116">-CustomRule</span></span>
<span data-ttu-id="5a109-117">自訂規則清單</span><span class="sxs-lookup"><span data-stu-id="5a109-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a109-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a109-118">-DefaultProfile</span></span>
<span data-ttu-id="5a109-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a109-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a109-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a109-120">-InputObject</span></span>
<span data-ttu-id="5a109-121">應用程式GatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5a109-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a109-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5a109-122">-ManagedRule</span></span>
<span data-ttu-id="5a109-123">防火牆策略的 ManagedRules</span><span class="sxs-lookup"><span data-stu-id="5a109-123">ManagedRules of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a109-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a109-124">-Name</span></span>
<span data-ttu-id="5a109-125">防火牆政策名稱。</span><span class="sxs-lookup"><span data-stu-id="5a109-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a109-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="5a109-126">-PolicySetting</span></span>
<span data-ttu-id="5a109-127">防火牆策略的設定</span><span class="sxs-lookup"><span data-stu-id="5a109-127">Policysettings of the firewall policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a109-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a109-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a109-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5a109-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a109-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a109-130">-ResourceId</span></span>
<span data-ttu-id="5a109-131">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a109-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a109-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5a109-132">-Confirm</span></span>
<span data-ttu-id="5a109-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5a109-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a109-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a109-134">-WhatIf</span></span>
<span data-ttu-id="5a109-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a109-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a109-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a109-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a109-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a109-137">CommonParameters</span></span>
<span data-ttu-id="5a109-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a109-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a109-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a109-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a109-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5a109-140">INPUTS</span></span>

### <span data-ttu-id="5a109-141">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5a109-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="5a109-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5a109-142">OUTPUTS</span></span>

### <span data-ttu-id="5a109-143">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5a109-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="5a109-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5a109-144">NOTES</span></span>

## <span data-ttu-id="5a109-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a109-145">RELATED LINKS</span></span>
