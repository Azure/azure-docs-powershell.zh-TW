---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: fc3780ea0e6cfff80117779786f1c9d9354ecf8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908097"
---
# <span data-ttu-id="4d781-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="4d781-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="4d781-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4d781-102">SYNOPSIS</span></span>
<span data-ttu-id="4d781-103">下載快速路由埠的授權書檔。</span><span class="sxs-lookup"><span data-stu-id="4d781-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="4d781-104">語法</span><span class="sxs-lookup"><span data-stu-id="4d781-104">SYNTAX</span></span>

### <span data-ttu-id="4d781-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4d781-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d781-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d781-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d781-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d781-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d781-108">描述</span><span class="sxs-lookup"><span data-stu-id="4d781-108">DESCRIPTION</span></span>
<span data-ttu-id="4d781-109">New-AzExpressRoutePortLOA Cmdlet 會下載 PDF 格式的授權信，以用於快速路由埠。</span><span class="sxs-lookup"><span data-stu-id="4d781-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="4d781-110">例子</span><span class="sxs-lookup"><span data-stu-id="4d781-110">EXAMPLES</span></span>

### <span data-ttu-id="4d781-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4d781-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="4d781-112">下載 Express 路由埠 'myPort' 的授權信，並儲存在檔案 'loa.pdf'。</span><span class="sxs-lookup"><span data-stu-id="4d781-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="4d781-113">參數</span><span class="sxs-lookup"><span data-stu-id="4d781-113">PARAMETERS</span></span>

### <span data-ttu-id="4d781-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d781-114">-AsJob</span></span>
<span data-ttu-id="4d781-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4d781-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d781-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="4d781-116">-CustomerName</span></span>
<span data-ttu-id="4d781-117">指派給此 Express Route 埠的客戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4d781-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d781-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d781-118">-DefaultProfile</span></span>
<span data-ttu-id="4d781-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d781-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d781-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="4d781-120">-Destination</span></span>
<span data-ttu-id="4d781-121">要儲存授權信的輸出 filepath。</span><span class="sxs-lookup"><span data-stu-id="4d781-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d781-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4d781-122">-ExpressRoutePort</span></span>
<span data-ttu-id="4d781-123">Express Route 埠資源。</span><span class="sxs-lookup"><span data-stu-id="4d781-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d781-124">-Id</span><span class="sxs-lookup"><span data-stu-id="4d781-124">-Id</span></span>
<span data-ttu-id="4d781-125">Express 路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="4d781-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d781-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d781-126">-PassThru</span></span>
<span data-ttu-id="4d781-127">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4d781-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="4d781-128">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4d781-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d781-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="4d781-129">-PortName</span></span>
<span data-ttu-id="4d781-130">快速路由埠名稱。</span><span class="sxs-lookup"><span data-stu-id="4d781-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d781-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d781-131">-ResourceGroupName</span></span>
<span data-ttu-id="4d781-132">Express 路由埠的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4d781-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d781-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d781-133">CommonParameters</span></span>
<span data-ttu-id="4d781-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4d781-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d781-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d781-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d781-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4d781-136">INPUTS</span></span>

### <span data-ttu-id="4d781-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4d781-137">System.String</span></span>

## <span data-ttu-id="4d781-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4d781-138">OUTPUTS</span></span>

### <span data-ttu-id="4d781-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d781-139">System.Boolean</span></span>

## <span data-ttu-id="4d781-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4d781-140">NOTES</span></span>

## <span data-ttu-id="4d781-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d781-141">RELATED LINKS</span></span>
