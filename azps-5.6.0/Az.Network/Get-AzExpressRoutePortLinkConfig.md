---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: a8326afbeb6d71d54ec861eb3ec65868e7e230bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903170"
---
# <span data-ttu-id="a6790-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="a6790-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="a6790-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6790-102">SYNOPSIS</span></span>
<span data-ttu-id="a6790-103">獲得 ExpressRoutePort 連結組配置。</span><span class="sxs-lookup"><span data-stu-id="a6790-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="a6790-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6790-104">SYNTAX</span></span>

### <span data-ttu-id="a6790-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a6790-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6790-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6790-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6790-107">描述</span><span class="sxs-lookup"><span data-stu-id="a6790-107">DESCRIPTION</span></span>
<span data-ttu-id="a6790-108">**Get-AzExpressRoutePortLinkConfig** Cmdlet 會取得 ExpressRoutePort 連結的組式。</span><span class="sxs-lookup"><span data-stu-id="a6790-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="a6790-109">例子</span><span class="sxs-lookup"><span data-stu-id="a6790-109">EXAMPLES</span></span>

### <span data-ttu-id="a6790-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a6790-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="a6790-111">獲得 ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="a6790-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="a6790-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="a6790-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="a6790-113">在 ExpressRoutePort $id中使用 ResourceId 連結$erport</span><span class="sxs-lookup"><span data-stu-id="a6790-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="a6790-114">參數</span><span class="sxs-lookup"><span data-stu-id="a6790-114">PARAMETERS</span></span>

### <span data-ttu-id="a6790-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6790-115">-DefaultProfile</span></span>
<span data-ttu-id="a6790-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6790-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6790-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a6790-117">-ExpressRoutePort</span></span>
<span data-ttu-id="a6790-118">ExpressRoutePort 資源的參照。</span><span class="sxs-lookup"><span data-stu-id="a6790-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6790-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6790-119">-Name</span></span>
<span data-ttu-id="a6790-120">連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6790-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6790-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6790-121">-ResourceId</span></span>
<span data-ttu-id="a6790-122">連結的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a6790-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="a6790-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6790-123">CommonParameters</span></span>
<span data-ttu-id="a6790-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6790-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6790-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6790-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6790-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a6790-126">INPUTS</span></span>

### <span data-ttu-id="a6790-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a6790-127">System.String</span></span>

### <span data-ttu-id="a6790-128">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a6790-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a6790-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a6790-129">OUTPUTS</span></span>

### <span data-ttu-id="a6790-130">Microsoft.Azure.Commands.Network.models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="a6790-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="a6790-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a6790-131">NOTES</span></span>

## <span data-ttu-id="a6790-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6790-132">RELATED LINKS</span></span>
