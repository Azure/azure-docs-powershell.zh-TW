---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286904"
---
# <span data-ttu-id="3b148-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="3b148-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="3b148-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b148-102">SYNOPSIS</span></span>
<span data-ttu-id="3b148-103">下載快速路由埠的授權檔信件。</span><span class="sxs-lookup"><span data-stu-id="3b148-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="3b148-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b148-104">SYNTAX</span></span>

### <span data-ttu-id="3b148-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b148-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b148-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b148-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b148-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b148-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b148-108">說明</span><span class="sxs-lookup"><span data-stu-id="3b148-108">DESCRIPTION</span></span>
<span data-ttu-id="3b148-109">New-AzExpressRoutePortLOA Cmdlet 會以 PDF 格式下載快速路由埠的授權檔（英文）。</span><span class="sxs-lookup"><span data-stu-id="3b148-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="3b148-110">示例</span><span class="sxs-lookup"><span data-stu-id="3b148-110">EXAMPLES</span></span>

### <span data-ttu-id="3b148-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3b148-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="3b148-112">下載快速路由埠 ' myPort」的授權檔信件，並將其儲存在 [loa.pdf] 中。</span><span class="sxs-lookup"><span data-stu-id="3b148-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="3b148-113">參數</span><span class="sxs-lookup"><span data-stu-id="3b148-113">PARAMETERS</span></span>

### <span data-ttu-id="3b148-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b148-114">-AsJob</span></span>
<span data-ttu-id="3b148-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3b148-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b148-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="3b148-116">-CustomerName</span></span>
<span data-ttu-id="3b148-117">已將此 Express Route 埠指派給的客戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3b148-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="3b148-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b148-118">-DefaultProfile</span></span>
<span data-ttu-id="3b148-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b148-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b148-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="3b148-120">-Destination</span></span>
<span data-ttu-id="3b148-121">要儲存授權信的輸出 filepath。</span><span class="sxs-lookup"><span data-stu-id="3b148-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="3b148-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3b148-122">-ExpressRoutePort</span></span>
<span data-ttu-id="3b148-123">Express route 埠資源。</span><span class="sxs-lookup"><span data-stu-id="3b148-123">The express route port resource.</span></span>

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

### <span data-ttu-id="3b148-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="3b148-124">-Id</span></span>
<span data-ttu-id="3b148-125">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="3b148-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="3b148-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b148-126">-PassThru</span></span>
<span data-ttu-id="3b148-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3b148-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3b148-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3b148-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b148-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="3b148-129">-PortName</span></span>
<span data-ttu-id="3b148-130">Express route 埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b148-130">The express route port name.</span></span>

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

### <span data-ttu-id="3b148-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b148-131">-ResourceGroupName</span></span>
<span data-ttu-id="3b148-132">快速路由埠的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3b148-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="3b148-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b148-133">CommonParameters</span></span>
<span data-ttu-id="3b148-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b148-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b148-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3b148-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b148-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3b148-136">INPUTS</span></span>

### <span data-ttu-id="3b148-137">System.object</span><span class="sxs-lookup"><span data-stu-id="3b148-137">System.String</span></span>

## <span data-ttu-id="3b148-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3b148-138">OUTPUTS</span></span>

### <span data-ttu-id="3b148-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3b148-139">System.Boolean</span></span>

## <span data-ttu-id="3b148-140">筆記</span><span class="sxs-lookup"><span data-stu-id="3b148-140">NOTES</span></span>

## <span data-ttu-id="3b148-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b148-141">RELATED LINKS</span></span>
