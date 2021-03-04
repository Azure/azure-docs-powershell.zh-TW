---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 9769a5506f528eb03d5e6d5a26340b961786c363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904921"
---
# <span data-ttu-id="eec37-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eec37-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="eec37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eec37-102">SYNOPSIS</span></span>
<span data-ttu-id="eec37-103">修改 ExpressRoute 交叉連接。</span><span class="sxs-lookup"><span data-stu-id="eec37-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="eec37-104">語法</span><span class="sxs-lookup"><span data-stu-id="eec37-104">SYNTAX</span></span>

### <span data-ttu-id="eec37-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="eec37-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec37-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="eec37-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec37-107">描述</span><span class="sxs-lookup"><span data-stu-id="eec37-107">DESCRIPTION</span></span>
<span data-ttu-id="eec37-108">**Set-AzExpressRouteCrossConnection** Cmdlet 會將經過修改的 ExpressRoute 交叉連接存到 Azure。</span><span class="sxs-lookup"><span data-stu-id="eec37-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="eec37-109">例子</span><span class="sxs-lookup"><span data-stu-id="eec37-109">EXAMPLES</span></span>

### <span data-ttu-id="eec37-110">範例 1：變更 ExpressRoute 交叉連接的服務提供者布備狀態</span><span class="sxs-lookup"><span data-stu-id="eec37-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="eec37-111">參數</span><span class="sxs-lookup"><span data-stu-id="eec37-111">PARAMETERS</span></span>

### <span data-ttu-id="eec37-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eec37-112">-AsJob</span></span>
<span data-ttu-id="eec37-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eec37-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eec37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec37-114">-DefaultProfile</span></span>
<span data-ttu-id="eec37-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eec37-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec37-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eec37-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="eec37-117">指定此 **Cmdlet 修改的 ExpressRouteCrossConnection** 物件。</span><span class="sxs-lookup"><span data-stu-id="eec37-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eec37-118">-強制</span><span class="sxs-lookup"><span data-stu-id="eec37-118">-Force</span></span>
<span data-ttu-id="eec37-119">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="eec37-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eec37-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="eec37-120">-Name</span></span>
<span data-ttu-id="eec37-121">快速路由交叉連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="eec37-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="eec37-122">-對等</span><span class="sxs-lookup"><span data-stu-id="eec37-122">-Peerings</span></span>
<span data-ttu-id="eec37-123">交叉連接的對等互連清單</span><span class="sxs-lookup"><span data-stu-id="eec37-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="eec37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec37-124">-ResourceGroupName</span></span>
<span data-ttu-id="eec37-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eec37-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="eec37-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="eec37-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="eec37-127">服務提供者附注</span><span class="sxs-lookup"><span data-stu-id="eec37-127">The service provider notes</span></span>

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

### <span data-ttu-id="eec37-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="eec37-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="eec37-129">要設定之服務提供者的設定狀態</span><span class="sxs-lookup"><span data-stu-id="eec37-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="eec37-130">-確認</span><span class="sxs-lookup"><span data-stu-id="eec37-130">-Confirm</span></span>
<span data-ttu-id="eec37-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eec37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec37-132">-WhatIf</span></span>
<span data-ttu-id="eec37-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eec37-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eec37-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eec37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec37-135">CommonParameters</span></span>
<span data-ttu-id="eec37-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eec37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec37-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eec37-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec37-138">輸入</span><span class="sxs-lookup"><span data-stu-id="eec37-138">INPUTS</span></span>

### <span data-ttu-id="eec37-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eec37-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="eec37-140">參數 'ExpressRouteCrossConnection' 接受來自管線之類型 'PSExpressRouteCrossConnection'的值</span><span class="sxs-lookup"><span data-stu-id="eec37-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="eec37-141">輸出</span><span class="sxs-lookup"><span data-stu-id="eec37-141">OUTPUTS</span></span>

### <span data-ttu-id="eec37-142">Microsoft.Azure.Commands.Network.models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eec37-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="eec37-143">筆記</span><span class="sxs-lookup"><span data-stu-id="eec37-143">NOTES</span></span>

## <span data-ttu-id="eec37-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="eec37-144">RELATED LINKS</span></span>

[<span data-ttu-id="eec37-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eec37-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
