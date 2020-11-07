---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959297"
---
# <span data-ttu-id="45ed9-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="45ed9-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="45ed9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="45ed9-103">取得 ExpressRoutePort 連結設定。</span><span class="sxs-lookup"><span data-stu-id="45ed9-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="45ed9-104">句法</span><span class="sxs-lookup"><span data-stu-id="45ed9-104">SYNTAX</span></span>

### <span data-ttu-id="45ed9-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="45ed9-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45ed9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ed9-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45ed9-107">說明</span><span class="sxs-lookup"><span data-stu-id="45ed9-107">DESCRIPTION</span></span>
<span data-ttu-id="45ed9-108">**AzExpressRoutePortLinkConfig** Cmdlet 會檢索 ExpressRoutePort 連結的設定。</span><span class="sxs-lookup"><span data-stu-id="45ed9-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="45ed9-109">示例</span><span class="sxs-lookup"><span data-stu-id="45ed9-109">EXAMPLES</span></span>

### <span data-ttu-id="45ed9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="45ed9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="45ed9-111">取得 ExpressRoutePort $erport 的 Link1 設定</span><span class="sxs-lookup"><span data-stu-id="45ed9-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="45ed9-112">範例2</span><span class="sxs-lookup"><span data-stu-id="45ed9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="45ed9-113">取得 ExpressRoutePort $erport 中與 ResourceId $id 連結的設定</span><span class="sxs-lookup"><span data-stu-id="45ed9-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="45ed9-114">參數</span><span class="sxs-lookup"><span data-stu-id="45ed9-114">PARAMETERS</span></span>

### <span data-ttu-id="45ed9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ed9-115">-DefaultProfile</span></span>
<span data-ttu-id="45ed9-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45ed9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ed9-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="45ed9-117">-ExpressRoutePort</span></span>
<span data-ttu-id="45ed9-118">ExpressRoutePort 資源的參照。</span><span class="sxs-lookup"><span data-stu-id="45ed9-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="45ed9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="45ed9-119">-Name</span></span>
<span data-ttu-id="45ed9-120">連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="45ed9-120">Name of the link.</span></span>

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

### <span data-ttu-id="45ed9-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45ed9-121">-ResourceId</span></span>
<span data-ttu-id="45ed9-122">連結的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="45ed9-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="45ed9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ed9-123">CommonParameters</span></span>
<span data-ttu-id="45ed9-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45ed9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ed9-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="45ed9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ed9-126">輸入</span><span class="sxs-lookup"><span data-stu-id="45ed9-126">INPUTS</span></span>

### <span data-ttu-id="45ed9-127">System.object</span><span class="sxs-lookup"><span data-stu-id="45ed9-127">System.String</span></span>

### <span data-ttu-id="45ed9-128">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45ed9-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="45ed9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="45ed9-129">OUTPUTS</span></span>

### <span data-ttu-id="45ed9-130">PSExpressRouteLink 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="45ed9-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="45ed9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="45ed9-131">NOTES</span></span>

## <span data-ttu-id="45ed9-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="45ed9-132">RELATED LINKS</span></span>
