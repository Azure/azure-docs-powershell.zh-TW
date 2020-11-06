---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622009"
---
# <span data-ttu-id="d6a22-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6a22-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="d6a22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6a22-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a22-103">Get-AzInterfaceEndpoint Cmdlet 會取得介面端點。</span><span class="sxs-lookup"><span data-stu-id="d6a22-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="d6a22-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6a22-104">SYNTAX</span></span>

### <span data-ttu-id="d6a22-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6a22-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6a22-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a22-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6a22-107">說明</span><span class="sxs-lookup"><span data-stu-id="d6a22-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a22-108">**AzInterfaceEndpoint** Cmdlet 會取得介面端點。</span><span class="sxs-lookup"><span data-stu-id="d6a22-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="d6a22-109">示例</span><span class="sxs-lookup"><span data-stu-id="d6a22-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a22-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d6a22-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d6a22-111">這個命令會取得名為 InterfaceEndpoint1 的介面端點，該介面端點屬於名為 ResourceGroup01 的資源群組，並將它儲存在 $interfaceendpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="d6a22-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="d6a22-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d6a22-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="d6a22-113">這個命令會取得具有 resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 的介面端點，並將它儲存在 $interfaceendpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="d6a22-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="d6a22-114">範例3</span><span class="sxs-lookup"><span data-stu-id="d6a22-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="d6a22-115">這個命令會取得以 "InterfaceEndpoint" 開頭的介面端點</span><span class="sxs-lookup"><span data-stu-id="d6a22-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="d6a22-116">參數</span><span class="sxs-lookup"><span data-stu-id="d6a22-116">PARAMETERS</span></span>

### <span data-ttu-id="d6a22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a22-117">-DefaultProfile</span></span>
<span data-ttu-id="d6a22-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6a22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a22-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6a22-119">-Name</span></span>
<span data-ttu-id="d6a22-120">介面端點的名稱</span><span class="sxs-lookup"><span data-stu-id="d6a22-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d6a22-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a22-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6a22-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6a22-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d6a22-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6a22-123">-ResourceId</span></span>
<span data-ttu-id="d6a22-124">介面端點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6a22-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a22-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d6a22-125">-Confirm</span></span>
<span data-ttu-id="d6a22-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6a22-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6a22-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a22-127">-WhatIf</span></span>
<span data-ttu-id="d6a22-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6a22-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a22-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6a22-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6a22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a22-130">CommonParameters</span></span>
<span data-ttu-id="d6a22-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6a22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a22-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d6a22-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a22-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d6a22-133">INPUTS</span></span>

### <span data-ttu-id="d6a22-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d6a22-134">System.String</span></span>

## <span data-ttu-id="d6a22-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d6a22-135">OUTPUTS</span></span>

### <span data-ttu-id="d6a22-136">PSInterfaceEndpoint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d6a22-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="d6a22-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d6a22-137">NOTES</span></span>

## <span data-ttu-id="d6a22-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6a22-138">RELATED LINKS</span></span>
