---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 2d7bdd9a1669859f0bcd650577ed3169a0aeea2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912353"
---
# <span data-ttu-id="cf159-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cf159-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="cf159-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf159-102">SYNOPSIS</span></span>
<span data-ttu-id="cf159-103">移除應用程式閘道防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="cf159-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="cf159-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf159-104">SYNTAX</span></span>

### <span data-ttu-id="cf159-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="cf159-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf159-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cf159-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf159-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf159-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf159-108">描述</span><span class="sxs-lookup"><span data-stu-id="cf159-108">DESCRIPTION</span></span>
<span data-ttu-id="cf159-109">**Remove-AzApplicationGatewayFirewallPolicy** Cmdlet 會移除應用程式閘道防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="cf159-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="cf159-110">例子</span><span class="sxs-lookup"><span data-stu-id="cf159-110">EXAMPLES</span></span>

### <span data-ttu-id="cf159-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="cf159-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cf159-112">此命令會移除名為 ResourceGroup01 的資源群組中名為 ApplicationGatewayFirewallPolicy01 的應用程式閘道防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="cf159-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="cf159-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf159-113">PARAMETERS</span></span>

### <span data-ttu-id="cf159-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf159-114">-AsJob</span></span>
<span data-ttu-id="cf159-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf159-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf159-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf159-116">-DefaultProfile</span></span>
<span data-ttu-id="cf159-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf159-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf159-118">-強制</span><span class="sxs-lookup"><span data-stu-id="cf159-118">-Force</span></span>
<span data-ttu-id="cf159-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="cf159-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf159-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf159-120">-InputObject</span></span>
<span data-ttu-id="cf159-121">防火牆政策物件</span><span class="sxs-lookup"><span data-stu-id="cf159-121">The firewall policy object</span></span>

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

### <span data-ttu-id="cf159-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf159-122">-Name</span></span>
<span data-ttu-id="cf159-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cf159-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf159-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf159-124">-PassThru</span></span>
<span data-ttu-id="cf159-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cf159-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf159-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cf159-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf159-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf159-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf159-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cf159-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf159-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf159-129">-ResourceId</span></span>
<span data-ttu-id="cf159-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf159-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cf159-131">-確認</span><span class="sxs-lookup"><span data-stu-id="cf159-131">-Confirm</span></span>
<span data-ttu-id="cf159-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf159-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf159-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf159-133">-WhatIf</span></span>
<span data-ttu-id="cf159-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf159-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf159-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf159-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf159-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf159-136">CommonParameters</span></span>
<span data-ttu-id="cf159-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf159-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf159-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cf159-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf159-139">輸入</span><span class="sxs-lookup"><span data-stu-id="cf159-139">INPUTS</span></span>

### <span data-ttu-id="cf159-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cf159-140">System.String</span></span>

## <span data-ttu-id="cf159-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cf159-141">OUTPUTS</span></span>

### <span data-ttu-id="cf159-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf159-142">System.Boolean</span></span>

## <span data-ttu-id="cf159-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cf159-143">NOTES</span></span>

## <span data-ttu-id="cf159-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf159-144">RELATED LINKS</span></span>
