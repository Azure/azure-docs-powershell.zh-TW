---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133778"
---
# <span data-ttu-id="1597d-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1597d-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="1597d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1597d-102">SYNOPSIS</span></span>
<span data-ttu-id="1597d-103">修改 ExpressRoute 交叉連線。</span><span class="sxs-lookup"><span data-stu-id="1597d-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="1597d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1597d-104">SYNTAX</span></span>

### <span data-ttu-id="1597d-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="1597d-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1597d-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="1597d-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1597d-107">說明</span><span class="sxs-lookup"><span data-stu-id="1597d-107">DESCRIPTION</span></span>
<span data-ttu-id="1597d-108">**AzExpressRouteCrossConnection** Cmdlet 會將已修改的 ExpressRoute 交叉連接儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="1597d-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="1597d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1597d-109">EXAMPLES</span></span>

### <span data-ttu-id="1597d-110">範例1：變更 ExpressRoute 交叉連線的服務提供者預配狀態</span><span class="sxs-lookup"><span data-stu-id="1597d-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="1597d-111">參數</span><span class="sxs-lookup"><span data-stu-id="1597d-111">PARAMETERS</span></span>

### <span data-ttu-id="1597d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1597d-112">-AsJob</span></span>
<span data-ttu-id="1597d-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1597d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1597d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1597d-114">-DefaultProfile</span></span>
<span data-ttu-id="1597d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1597d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1597d-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1597d-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1597d-117">指定此 Cmdlet 修改的 **ExpressRouteCrossConnection** 物件。</span><span class="sxs-lookup"><span data-stu-id="1597d-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1597d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1597d-118">-Force</span></span>
<span data-ttu-id="1597d-119">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="1597d-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1597d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1597d-120">-Name</span></span>
<span data-ttu-id="1597d-121">快速路由的名稱（交叉連接）。</span><span class="sxs-lookup"><span data-stu-id="1597d-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1597d-122">-Peerings</span><span class="sxs-lookup"><span data-stu-id="1597d-122">-Peerings</span></span>
<span data-ttu-id="1597d-123">交叉連接的 peerings 清單</span><span class="sxs-lookup"><span data-stu-id="1597d-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1597d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1597d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1597d-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1597d-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1597d-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="1597d-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="1597d-127">服務提供者注意事項</span><span class="sxs-lookup"><span data-stu-id="1597d-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1597d-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="1597d-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="1597d-129">要設定的服務提供者預配狀態</span><span class="sxs-lookup"><span data-stu-id="1597d-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1597d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1597d-130">-Confirm</span></span>
<span data-ttu-id="1597d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1597d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1597d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1597d-132">-WhatIf</span></span>
<span data-ttu-id="1597d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1597d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1597d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1597d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1597d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1597d-135">CommonParameters</span></span>
<span data-ttu-id="1597d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1597d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1597d-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1597d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1597d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1597d-138">INPUTS</span></span>

### <span data-ttu-id="1597d-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1597d-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="1597d-140">形參 "ExpressRouteCrossConnection" 接受管線中 "PSExpressRouteCrossConnection" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1597d-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="1597d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1597d-141">OUTPUTS</span></span>

### <span data-ttu-id="1597d-142">PSExpressRouteCrossConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1597d-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="1597d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1597d-143">NOTES</span></span>

## <span data-ttu-id="1597d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1597d-144">RELATED LINKS</span></span>

[<span data-ttu-id="1597d-145">AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1597d-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
