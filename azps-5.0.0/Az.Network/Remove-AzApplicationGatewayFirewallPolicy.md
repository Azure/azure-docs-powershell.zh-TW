---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139692"
---
# <span data-ttu-id="37e51-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="37e51-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="37e51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37e51-102">SYNOPSIS</span></span>
<span data-ttu-id="37e51-103">移除應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="37e51-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="37e51-104">句法</span><span class="sxs-lookup"><span data-stu-id="37e51-104">SYNTAX</span></span>

### <span data-ttu-id="37e51-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="37e51-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37e51-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="37e51-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37e51-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="37e51-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e51-108">說明</span><span class="sxs-lookup"><span data-stu-id="37e51-108">DESCRIPTION</span></span>
<span data-ttu-id="37e51-109">**AzApplicationGatewayFirewallPolicy** Cmdlet 會移除應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="37e51-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="37e51-110">示例</span><span class="sxs-lookup"><span data-stu-id="37e51-110">EXAMPLES</span></span>

### <span data-ttu-id="37e51-111">範例1</span><span class="sxs-lookup"><span data-stu-id="37e51-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="37e51-112">這個命令會在名為 ResourceGroup01 的資源群組中，移除名為 ApplicationGatewayFirewallPolicy01 的應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="37e51-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="37e51-113">參數</span><span class="sxs-lookup"><span data-stu-id="37e51-113">PARAMETERS</span></span>

### <span data-ttu-id="37e51-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37e51-114">-AsJob</span></span>
<span data-ttu-id="37e51-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37e51-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37e51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e51-116">-DefaultProfile</span></span>
<span data-ttu-id="37e51-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37e51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e51-118">-Force</span><span class="sxs-lookup"><span data-stu-id="37e51-118">-Force</span></span>
<span data-ttu-id="37e51-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="37e51-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="37e51-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37e51-120">-InputObject</span></span>
<span data-ttu-id="37e51-121">防火牆原則物件</span><span class="sxs-lookup"><span data-stu-id="37e51-121">The firewall policy object</span></span>

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

### <span data-ttu-id="37e51-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="37e51-122">-Name</span></span>
<span data-ttu-id="37e51-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="37e51-123">The resource name.</span></span>

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

### <span data-ttu-id="37e51-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37e51-124">-PassThru</span></span>
<span data-ttu-id="37e51-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="37e51-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="37e51-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="37e51-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="37e51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e51-127">-ResourceGroupName</span></span>
<span data-ttu-id="37e51-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37e51-128">The resource group name.</span></span>

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

### <span data-ttu-id="37e51-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37e51-129">-ResourceId</span></span>
<span data-ttu-id="37e51-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="37e51-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="37e51-131">-確認</span><span class="sxs-lookup"><span data-stu-id="37e51-131">-Confirm</span></span>
<span data-ttu-id="37e51-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37e51-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e51-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e51-133">-WhatIf</span></span>
<span data-ttu-id="37e51-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37e51-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e51-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37e51-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e51-136">CommonParameters</span></span>
<span data-ttu-id="37e51-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37e51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e51-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37e51-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e51-139">輸入</span><span class="sxs-lookup"><span data-stu-id="37e51-139">INPUTS</span></span>

### <span data-ttu-id="37e51-140">System.object</span><span class="sxs-lookup"><span data-stu-id="37e51-140">System.String</span></span>

## <span data-ttu-id="37e51-141">輸出</span><span class="sxs-lookup"><span data-stu-id="37e51-141">OUTPUTS</span></span>

### <span data-ttu-id="37e51-142">System.object</span><span class="sxs-lookup"><span data-stu-id="37e51-142">System.Boolean</span></span>

## <span data-ttu-id="37e51-143">筆記</span><span class="sxs-lookup"><span data-stu-id="37e51-143">NOTES</span></span>

## <span data-ttu-id="37e51-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="37e51-144">RELATED LINKS</span></span>