---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140307"
---
# <span data-ttu-id="99525-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="99525-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="99525-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99525-102">SYNOPSIS</span></span>
<span data-ttu-id="99525-103">移除應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="99525-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="99525-104">句法</span><span class="sxs-lookup"><span data-stu-id="99525-104">SYNTAX</span></span>

### <span data-ttu-id="99525-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="99525-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99525-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="99525-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99525-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99525-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99525-108">說明</span><span class="sxs-lookup"><span data-stu-id="99525-108">DESCRIPTION</span></span>
<span data-ttu-id="99525-109">**AzApplicationGatewayFirewallPolicy** Cmdlet 會移除應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="99525-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="99525-110">示例</span><span class="sxs-lookup"><span data-stu-id="99525-110">EXAMPLES</span></span>

### <span data-ttu-id="99525-111">範例1</span><span class="sxs-lookup"><span data-stu-id="99525-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="99525-112">這個命令會在名為 ResourceGroup01 的資源群組中，移除名為 ApplicationGatewayFirewallPolicy01 的應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="99525-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="99525-113">參數</span><span class="sxs-lookup"><span data-stu-id="99525-113">PARAMETERS</span></span>

### <span data-ttu-id="99525-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99525-114">-AsJob</span></span>
<span data-ttu-id="99525-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="99525-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99525-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99525-116">-DefaultProfile</span></span>
<span data-ttu-id="99525-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99525-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99525-118">-Force</span><span class="sxs-lookup"><span data-stu-id="99525-118">-Force</span></span>
<span data-ttu-id="99525-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="99525-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="99525-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99525-120">-InputObject</span></span>
<span data-ttu-id="99525-121">防火牆原則物件</span><span class="sxs-lookup"><span data-stu-id="99525-121">The firewall policy object</span></span>

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

### <span data-ttu-id="99525-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="99525-122">-Name</span></span>
<span data-ttu-id="99525-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="99525-123">The resource name.</span></span>

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

### <span data-ttu-id="99525-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99525-124">-PassThru</span></span>
<span data-ttu-id="99525-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="99525-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="99525-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="99525-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99525-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99525-127">-ResourceGroupName</span></span>
<span data-ttu-id="99525-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99525-128">The resource group name.</span></span>

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

### <span data-ttu-id="99525-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99525-129">-ResourceId</span></span>
<span data-ttu-id="99525-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="99525-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="99525-131">-確認</span><span class="sxs-lookup"><span data-stu-id="99525-131">-Confirm</span></span>
<span data-ttu-id="99525-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99525-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99525-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99525-133">-WhatIf</span></span>
<span data-ttu-id="99525-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99525-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99525-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99525-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99525-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99525-136">CommonParameters</span></span>
<span data-ttu-id="99525-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99525-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99525-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99525-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99525-139">輸入</span><span class="sxs-lookup"><span data-stu-id="99525-139">INPUTS</span></span>

### <span data-ttu-id="99525-140">System.object</span><span class="sxs-lookup"><span data-stu-id="99525-140">System.String</span></span>

## <span data-ttu-id="99525-141">輸出</span><span class="sxs-lookup"><span data-stu-id="99525-141">OUTPUTS</span></span>

### <span data-ttu-id="99525-142">System.object</span><span class="sxs-lookup"><span data-stu-id="99525-142">System.Boolean</span></span>

## <span data-ttu-id="99525-143">筆記</span><span class="sxs-lookup"><span data-stu-id="99525-143">NOTES</span></span>

## <span data-ttu-id="99525-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="99525-144">RELATED LINKS</span></span>
