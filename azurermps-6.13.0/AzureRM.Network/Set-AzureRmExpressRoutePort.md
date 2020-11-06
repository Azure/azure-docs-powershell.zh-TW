---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451816"
---
# <span data-ttu-id="32ef0-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="32ef0-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="32ef0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="32ef0-103">修改 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="32ef0-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32ef0-104">句法</span><span class="sxs-lookup"><span data-stu-id="32ef0-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32ef0-105">說明</span><span class="sxs-lookup"><span data-stu-id="32ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="32ef0-106">**AzureRmExpressRoutePort** Cmdlet 會將已修改的 ExpressRoutePort 儲存至 Azure。</span><span class="sxs-lookup"><span data-stu-id="32ef0-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="32ef0-107">示例</span><span class="sxs-lookup"><span data-stu-id="32ef0-107">EXAMPLES</span></span>

### <span data-ttu-id="32ef0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="32ef0-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="32ef0-109">範例2</span><span class="sxs-lookup"><span data-stu-id="32ef0-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="32ef0-110">修改 ExpressRoutePort 連結的系統管理員狀態</span><span class="sxs-lookup"><span data-stu-id="32ef0-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="32ef0-111">參數</span><span class="sxs-lookup"><span data-stu-id="32ef0-111">PARAMETERS</span></span>

### <span data-ttu-id="32ef0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32ef0-112">-AsJob</span></span>
<span data-ttu-id="32ef0-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="32ef0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32ef0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ef0-114">-DefaultProfile</span></span>
<span data-ttu-id="32ef0-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32ef0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ef0-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="32ef0-116">-ExpressRoutePort</span></span>
<span data-ttu-id="32ef0-117">ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="32ef0-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="32ef0-118">-確認</span><span class="sxs-lookup"><span data-stu-id="32ef0-118">-Confirm</span></span>
<span data-ttu-id="32ef0-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32ef0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32ef0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32ef0-120">-WhatIf</span></span>
<span data-ttu-id="32ef0-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32ef0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32ef0-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32ef0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32ef0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ef0-123">CommonParameters</span></span>
<span data-ttu-id="32ef0-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32ef0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ef0-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32ef0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ef0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="32ef0-126">INPUTS</span></span>

### <span data-ttu-id="32ef0-127">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="32ef0-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="32ef0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="32ef0-128">OUTPUTS</span></span>

### <span data-ttu-id="32ef0-129">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="32ef0-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="32ef0-130">筆記</span><span class="sxs-lookup"><span data-stu-id="32ef0-130">NOTES</span></span>

## <span data-ttu-id="32ef0-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="32ef0-131">RELATED LINKS</span></span>
