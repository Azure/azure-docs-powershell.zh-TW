---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904917"
---
# <span data-ttu-id="343ff-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="343ff-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="343ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="343ff-102">SYNOPSIS</span></span>
<span data-ttu-id="343ff-103">修改 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="343ff-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="343ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="343ff-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="343ff-105">DESCRIPTION</span></span>
<span data-ttu-id="343ff-106">**Set-AzExpressRoutePort** Cmdlet 會將修改後的 ExpressRoutePort 存到 Azure。</span><span class="sxs-lookup"><span data-stu-id="343ff-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="343ff-107">例子</span><span class="sxs-lookup"><span data-stu-id="343ff-107">EXAMPLES</span></span>

### <span data-ttu-id="343ff-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="343ff-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="343ff-109">範例 2</span><span class="sxs-lookup"><span data-stu-id="343ff-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="343ff-110">修改 ExpressRoutePort 連結的系統管理員狀態</span><span class="sxs-lookup"><span data-stu-id="343ff-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="343ff-111">範例 3</span><span class="sxs-lookup"><span data-stu-id="343ff-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="343ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="343ff-112">PARAMETERS</span></span>

### <span data-ttu-id="343ff-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="343ff-113">-AsJob</span></span>
<span data-ttu-id="343ff-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="343ff-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="343ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343ff-115">-DefaultProfile</span></span>
<span data-ttu-id="343ff-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="343ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="343ff-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="343ff-117">-ExpressRoutePort</span></span>
<span data-ttu-id="343ff-118">ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="343ff-118">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="343ff-119">-確認</span><span class="sxs-lookup"><span data-stu-id="343ff-119">-Confirm</span></span>
<span data-ttu-id="343ff-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="343ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343ff-121">-WhatIf</span></span>
<span data-ttu-id="343ff-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="343ff-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343ff-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="343ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="343ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343ff-124">CommonParameters</span></span>
<span data-ttu-id="343ff-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="343ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343ff-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="343ff-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343ff-127">輸入</span><span class="sxs-lookup"><span data-stu-id="343ff-127">INPUTS</span></span>

### <span data-ttu-id="343ff-128">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="343ff-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="343ff-129">輸出</span><span class="sxs-lookup"><span data-stu-id="343ff-129">OUTPUTS</span></span>

### <span data-ttu-id="343ff-130">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="343ff-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="343ff-131">筆記</span><span class="sxs-lookup"><span data-stu-id="343ff-131">NOTES</span></span>

## <span data-ttu-id="343ff-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="343ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="343ff-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="343ff-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="343ff-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="343ff-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="343ff-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="343ff-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
