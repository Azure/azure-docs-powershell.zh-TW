---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136306"
---
# <span data-ttu-id="b6d83-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="b6d83-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="b6d83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6d83-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d83-103">下載快速路由埠的授權檔信件。</span><span class="sxs-lookup"><span data-stu-id="b6d83-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="b6d83-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6d83-104">SYNTAX</span></span>

### <span data-ttu-id="b6d83-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b6d83-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6d83-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6d83-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6d83-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6d83-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6d83-108">說明</span><span class="sxs-lookup"><span data-stu-id="b6d83-108">DESCRIPTION</span></span>
<span data-ttu-id="b6d83-109">New-AzExpressRoutePortLOA Cmdlet 會以 PDF 格式下載快速路由埠的授權檔（英文）。</span><span class="sxs-lookup"><span data-stu-id="b6d83-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="b6d83-110">示例</span><span class="sxs-lookup"><span data-stu-id="b6d83-110">EXAMPLES</span></span>

### <span data-ttu-id="b6d83-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b6d83-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="b6d83-112">下載快速路由埠 ' myPort」的授權檔信件，並將其儲存在 [loa.pdf] 中。</span><span class="sxs-lookup"><span data-stu-id="b6d83-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="b6d83-113">參數</span><span class="sxs-lookup"><span data-stu-id="b6d83-113">PARAMETERS</span></span>

### <span data-ttu-id="b6d83-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6d83-114">-AsJob</span></span>
<span data-ttu-id="b6d83-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6d83-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6d83-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="b6d83-116">-CustomerName</span></span>
<span data-ttu-id="b6d83-117">已將此 Express Route 埠指派給的客戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b6d83-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="b6d83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d83-118">-DefaultProfile</span></span>
<span data-ttu-id="b6d83-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6d83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d83-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="b6d83-120">-Destination</span></span>
<span data-ttu-id="b6d83-121">要儲存授權信的輸出 filepath。</span><span class="sxs-lookup"><span data-stu-id="b6d83-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="b6d83-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b6d83-122">-ExpressRoutePort</span></span>
<span data-ttu-id="b6d83-123">Express route 埠資源。</span><span class="sxs-lookup"><span data-stu-id="b6d83-123">The express route port resource.</span></span>

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

### <span data-ttu-id="b6d83-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b6d83-124">-Id</span></span>
<span data-ttu-id="b6d83-125">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b6d83-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="b6d83-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6d83-126">-PassThru</span></span>
<span data-ttu-id="b6d83-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b6d83-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b6d83-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b6d83-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6d83-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="b6d83-129">-PortName</span></span>
<span data-ttu-id="b6d83-130">Express route 埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6d83-130">The express route port name.</span></span>

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

### <span data-ttu-id="b6d83-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d83-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6d83-132">快速路由埠的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b6d83-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="b6d83-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d83-133">CommonParameters</span></span>
<span data-ttu-id="b6d83-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6d83-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d83-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6d83-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d83-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b6d83-136">INPUTS</span></span>

### <span data-ttu-id="b6d83-137">System.object</span><span class="sxs-lookup"><span data-stu-id="b6d83-137">System.String</span></span>

## <span data-ttu-id="b6d83-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b6d83-138">OUTPUTS</span></span>

### <span data-ttu-id="b6d83-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b6d83-139">System.Boolean</span></span>

## <span data-ttu-id="b6d83-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b6d83-140">NOTES</span></span>

## <span data-ttu-id="b6d83-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6d83-141">RELATED LINKS</span></span>
