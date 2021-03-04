---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: f9ce00bb5efbe5182143a08f9f205101b9f85611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908818"
---
# <span data-ttu-id="bea28-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bea28-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="bea28-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bea28-102">SYNOPSIS</span></span>
<span data-ttu-id="bea28-103">獲得 Azure ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="bea28-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="bea28-104">語法</span><span class="sxs-lookup"><span data-stu-id="bea28-104">SYNTAX</span></span>

### <span data-ttu-id="bea28-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bea28-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea28-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bea28-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bea28-107">描述</span><span class="sxs-lookup"><span data-stu-id="bea28-107">DESCRIPTION</span></span>
<span data-ttu-id="bea28-108">**Get-AzExpressRoutePort** Cmdlet 可用來從訂閱中取回 ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="bea28-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="bea28-109">所返回的 expressrouteport 物件可以用來做為在 ExpressRoutePort 上操作的其他 Cmdlet 的輸入。</span><span class="sxs-lookup"><span data-stu-id="bea28-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="bea28-110">例子</span><span class="sxs-lookup"><span data-stu-id="bea28-110">EXAMPLES</span></span>

### <span data-ttu-id="bea28-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bea28-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="bea28-112">在訂閱的資源群組中$PortName名稱為 ExpressRoutePort $rg物件。</span><span class="sxs-lookup"><span data-stu-id="bea28-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="bea28-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bea28-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="bea28-114">會獲得名稱以「測試」開頭的所有 ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="bea28-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="bea28-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="bea28-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="bea28-116">使用 ResourceId $id。</span><span class="sxs-lookup"><span data-stu-id="bea28-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="bea28-117">參數</span><span class="sxs-lookup"><span data-stu-id="bea28-117">PARAMETERS</span></span>

### <span data-ttu-id="bea28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea28-118">-DefaultProfile</span></span>
<span data-ttu-id="bea28-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bea28-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea28-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="bea28-120">-Name</span></span>
<span data-ttu-id="bea28-121">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bea28-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bea28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea28-122">-ResourceGroupName</span></span>
<span data-ttu-id="bea28-123">ExpressRoutePort 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bea28-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bea28-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bea28-124">-ResourceId</span></span>
<span data-ttu-id="bea28-125">Express 路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="bea28-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea28-126">CommonParameters</span></span>
<span data-ttu-id="bea28-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bea28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea28-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bea28-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea28-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bea28-129">INPUTS</span></span>

### <span data-ttu-id="bea28-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bea28-130">System.String</span></span>

## <span data-ttu-id="bea28-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bea28-131">OUTPUTS</span></span>

### <span data-ttu-id="bea28-132">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bea28-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="bea28-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bea28-133">NOTES</span></span>

## <span data-ttu-id="bea28-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bea28-134">RELATED LINKS</span></span>

[<span data-ttu-id="bea28-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bea28-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="bea28-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bea28-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="bea28-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bea28-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
