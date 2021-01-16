---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437451"
---
# <span data-ttu-id="ead52-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ead52-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="ead52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ead52-102">SYNOPSIS</span></span>
<span data-ttu-id="ead52-103">更新應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="ead52-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="ead52-104">句法</span><span class="sxs-lookup"><span data-stu-id="ead52-104">SYNTAX</span></span>

### <span data-ttu-id="ead52-105">ByFactoryObject (預設) </span><span class="sxs-lookup"><span data-stu-id="ead52-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead52-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="ead52-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead52-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ead52-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead52-108">說明</span><span class="sxs-lookup"><span data-stu-id="ead52-108">DESCRIPTION</span></span>
<span data-ttu-id="ead52-109">**AzApplicationGatewayFirewallPolicy** Cmdlet 會更新 Azure 應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="ead52-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="ead52-110">示例</span><span class="sxs-lookup"><span data-stu-id="ead52-110">EXAMPLES</span></span>

### <span data-ttu-id="ead52-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ead52-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="ead52-112">這個命令會使用 $AppGwFirewallPolicy 變數中的設定來更新應用程式閘道防火牆原則，並將更新的閘道儲存在 $UpdatedAppGwFirewallPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="ead52-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="ead52-113">參數</span><span class="sxs-lookup"><span data-stu-id="ead52-113">PARAMETERS</span></span>

### <span data-ttu-id="ead52-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ead52-114">-AsJob</span></span>
<span data-ttu-id="ead52-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ead52-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ead52-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="ead52-116">-CustomRule</span></span>
<span data-ttu-id="ead52-117">CustomRules 清單</span><span class="sxs-lookup"><span data-stu-id="ead52-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="ead52-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead52-118">-DefaultProfile</span></span>
<span data-ttu-id="ead52-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ead52-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead52-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ead52-120">-InputObject</span></span>
<span data-ttu-id="ead52-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ead52-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="ead52-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="ead52-122">-ManagedRule</span></span>
<span data-ttu-id="ead52-123">防火牆原則的 ManagedRules</span><span class="sxs-lookup"><span data-stu-id="ead52-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="ead52-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ead52-124">-Name</span></span>
<span data-ttu-id="ead52-125">防火牆原則名稱。</span><span class="sxs-lookup"><span data-stu-id="ead52-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="ead52-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="ead52-126">-PolicySetting</span></span>
<span data-ttu-id="ead52-127">防火牆原則的 Policysettings</span><span class="sxs-lookup"><span data-stu-id="ead52-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="ead52-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead52-128">-ResourceGroupName</span></span>
<span data-ttu-id="ead52-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ead52-129">The resource group name.</span></span>

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

### <span data-ttu-id="ead52-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ead52-130">-ResourceId</span></span>
<span data-ttu-id="ead52-131">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ead52-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ead52-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ead52-132">-Confirm</span></span>
<span data-ttu-id="ead52-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ead52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead52-134">-WhatIf</span></span>
<span data-ttu-id="ead52-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ead52-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ead52-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ead52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead52-137">CommonParameters</span></span>
<span data-ttu-id="ead52-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ead52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead52-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ead52-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead52-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ead52-140">INPUTS</span></span>

### <span data-ttu-id="ead52-141">PSApplicationGatewayWebApplicationFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ead52-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="ead52-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ead52-142">OUTPUTS</span></span>

### <span data-ttu-id="ead52-143">PSApplicationGatewayWebApplicationFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ead52-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="ead52-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ead52-144">NOTES</span></span>

## <span data-ttu-id="ead52-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ead52-145">RELATED LINKS</span></span>
