---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: fe1182f165e347b312288d56604fddad6bad68da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788990"
---
# <span data-ttu-id="c2d14-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c2d14-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="c2d14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2d14-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d14-103">修改 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="c2d14-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="c2d14-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2d14-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2d14-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2d14-105">DESCRIPTION</span></span>
<span data-ttu-id="c2d14-106">**AzExpressRoutePort** Cmdlet 會將已修改的 ExpressRoutePort 儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="c2d14-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="c2d14-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2d14-107">EXAMPLES</span></span>

### <span data-ttu-id="c2d14-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c2d14-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="c2d14-109">範例2</span><span class="sxs-lookup"><span data-stu-id="c2d14-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="c2d14-110">修改 ExpressRoutePort 連結的系統管理員狀態</span><span class="sxs-lookup"><span data-stu-id="c2d14-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="c2d14-111">參數</span><span class="sxs-lookup"><span data-stu-id="c2d14-111">PARAMETERS</span></span>

### <span data-ttu-id="c2d14-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2d14-112">-AsJob</span></span>
<span data-ttu-id="c2d14-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2d14-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2d14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d14-114">-DefaultProfile</span></span>
<span data-ttu-id="c2d14-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2d14-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d14-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c2d14-116">-ExpressRoutePort</span></span>
<span data-ttu-id="c2d14-117">ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="c2d14-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="c2d14-118">-確認</span><span class="sxs-lookup"><span data-stu-id="c2d14-118">-Confirm</span></span>
<span data-ttu-id="c2d14-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2d14-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2d14-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2d14-120">-WhatIf</span></span>
<span data-ttu-id="c2d14-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2d14-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2d14-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2d14-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2d14-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d14-123">CommonParameters</span></span>
<span data-ttu-id="c2d14-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2d14-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d14-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2d14-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d14-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c2d14-126">INPUTS</span></span>

### <span data-ttu-id="c2d14-127">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2d14-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c2d14-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c2d14-128">OUTPUTS</span></span>

### <span data-ttu-id="c2d14-129">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2d14-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c2d14-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c2d14-130">NOTES</span></span>

## <span data-ttu-id="c2d14-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2d14-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2d14-132">AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c2d14-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="c2d14-133">新-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c2d14-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="c2d14-134">移除-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c2d14-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
