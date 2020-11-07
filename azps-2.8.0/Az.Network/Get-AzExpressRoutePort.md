---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 69a03bc9772e9d74fdc1863221c99b46620ae700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790126"
---
# <span data-ttu-id="ad866-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ad866-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="ad866-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad866-102">SYNOPSIS</span></span>
<span data-ttu-id="ad866-103">取得 Azure ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="ad866-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="ad866-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad866-104">SYNTAX</span></span>

### <span data-ttu-id="ad866-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ad866-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad866-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad866-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad866-107">說明</span><span class="sxs-lookup"><span data-stu-id="ad866-107">DESCRIPTION</span></span>
<span data-ttu-id="ad866-108">**AzExpressRoutePort** Cmdlet 是用來從您的訂閱中檢索 ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="ad866-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="ad866-109">傳回的 expressrouteport 物件可以用來做為在 ExpressRoutePort 上執行的其他 Cmdlet 的輸入。</span><span class="sxs-lookup"><span data-stu-id="ad866-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="ad866-110">示例</span><span class="sxs-lookup"><span data-stu-id="ad866-110">EXAMPLES</span></span>

### <span data-ttu-id="ad866-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ad866-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="ad866-112">取得您訂閱中的 [資源群組] $rg 中名稱 $PortName 的 ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="ad866-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="ad866-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ad866-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="ad866-114">取得名稱以「test」開頭的所有 ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="ad866-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="ad866-115">範例3</span><span class="sxs-lookup"><span data-stu-id="ad866-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="ad866-116">取得 ExpressRoutePort 物件，其中包含 ResourceId $id。</span><span class="sxs-lookup"><span data-stu-id="ad866-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="ad866-117">參數</span><span class="sxs-lookup"><span data-stu-id="ad866-117">PARAMETERS</span></span>

### <span data-ttu-id="ad866-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad866-118">-DefaultProfile</span></span>
<span data-ttu-id="ad866-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad866-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad866-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad866-120">-Name</span></span>
<span data-ttu-id="ad866-121">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad866-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="ad866-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad866-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad866-123">ExpressRoutePort 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ad866-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="ad866-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad866-124">-ResourceId</span></span>
<span data-ttu-id="ad866-125">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ad866-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="ad866-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad866-126">CommonParameters</span></span>
<span data-ttu-id="ad866-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad866-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad866-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad866-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad866-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ad866-129">INPUTS</span></span>

### <span data-ttu-id="ad866-130">System.object</span><span class="sxs-lookup"><span data-stu-id="ad866-130">System.String</span></span>

## <span data-ttu-id="ad866-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ad866-131">OUTPUTS</span></span>

### <span data-ttu-id="ad866-132">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ad866-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ad866-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ad866-133">NOTES</span></span>

## <span data-ttu-id="ad866-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad866-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad866-135">新-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ad866-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="ad866-136">移除-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ad866-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="ad866-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ad866-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
