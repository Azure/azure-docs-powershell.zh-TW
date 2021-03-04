---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: c331cbb9731024598fe4d2542e734e406ac144ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912634"
---
# <span data-ttu-id="d0af9-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d0af9-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="d0af9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0af9-102">SYNOPSIS</span></span>
<span data-ttu-id="d0af9-103">移除現有的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="d0af9-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="d0af9-104">語法</span><span class="sxs-lookup"><span data-stu-id="d0af9-104">SYNTAX</span></span>

### <span data-ttu-id="d0af9-105">ByP2S VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="d0af9-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0af9-106">ByP2S VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d0af9-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0af9-107">ByP2S VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d0af9-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0af9-108">描述</span><span class="sxs-lookup"><span data-stu-id="d0af9-108">DESCRIPTION</span></span>
<span data-ttu-id="d0af9-109">**Remove-AzP2s VpnGateway** Cmdlet 可讓您在 VirtualHub 下移除現有的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="d0af9-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="d0af9-110">移除 P2S VpnGateway 後，所有指向網站用戶端的連接都會失敗。</span><span class="sxs-lookup"><span data-stu-id="d0af9-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="d0af9-111">例子</span><span class="sxs-lookup"><span data-stu-id="d0af9-111">EXAMPLES</span></span>

### <span data-ttu-id="d0af9-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d0af9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="d0af9-113">**Remove-AzP2s VpnGateway** Cmdlet 可讓您在 VirtualHub 下移除現有的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="d0af9-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="d0af9-114">參數</span><span class="sxs-lookup"><span data-stu-id="d0af9-114">PARAMETERS</span></span>

### <span data-ttu-id="d0af9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0af9-115">-DefaultProfile</span></span>
<span data-ttu-id="d0af9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0af9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-117">-強制</span><span class="sxs-lookup"><span data-stu-id="d0af9-117">-Force</span></span>
<span data-ttu-id="d0af9-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="d0af9-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0af9-119">-InputObject</span></span>
<span data-ttu-id="d0af9-120">要刪除的 p2s VpnGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="d0af9-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0af9-121">-Name</span></span>
<span data-ttu-id="d0af9-122">P2S VpnGateway 名稱。</span><span class="sxs-lookup"><span data-stu-id="d0af9-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0af9-123">-PassThru</span></span>
<span data-ttu-id="d0af9-124">會返回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d0af9-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0af9-125">-ResourceGroupName</span></span>
<span data-ttu-id="d0af9-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d0af9-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0af9-127">-ResourceId</span></span>
<span data-ttu-id="d0af9-128">要刪除 p2s VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0af9-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d0af9-129">-Confirm</span></span>
<span data-ttu-id="d0af9-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d0af9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0af9-131">-WhatIf</span></span>
<span data-ttu-id="d0af9-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0af9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0af9-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0af9-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0af9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0af9-134">CommonParameters</span></span>
<span data-ttu-id="d0af9-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0af9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0af9-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d0af9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0af9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d0af9-137">INPUTS</span></span>

### <span data-ttu-id="d0af9-138">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d0af9-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="d0af9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d0af9-139">System.String</span></span>

## <span data-ttu-id="d0af9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d0af9-140">OUTPUTS</span></span>

### <span data-ttu-id="d0af9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0af9-141">System.Boolean</span></span>

## <span data-ttu-id="d0af9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d0af9-142">NOTES</span></span>

## <span data-ttu-id="d0af9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0af9-143">RELATED LINKS</span></span>
