---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449057"
---
# <span data-ttu-id="2f399-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f399-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="2f399-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f399-102">SYNOPSIS</span></span>
<span data-ttu-id="2f399-103">Get-AzureRmInterfaceEndpoint Cmdlet 會取得介面端點。</span><span class="sxs-lookup"><span data-stu-id="2f399-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f399-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f399-104">SYNTAX</span></span>

### <span data-ttu-id="2f399-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2f399-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f399-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f399-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f399-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f399-107">DESCRIPTION</span></span>
<span data-ttu-id="2f399-108">**AzureRmInterfaceEndpoint** Cmdlet 會取得介面端點。</span><span class="sxs-lookup"><span data-stu-id="2f399-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="2f399-109">示例</span><span class="sxs-lookup"><span data-stu-id="2f399-109">EXAMPLES</span></span>

### <span data-ttu-id="2f399-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2f399-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2f399-111">這個命令會取得名為 InterfaceEndpoint1 的介面端點，該介面端點屬於名為 ResourceGroup01 的資源群組，並將它儲存在 $interfaceendpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f399-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="2f399-112">範例2</span><span class="sxs-lookup"><span data-stu-id="2f399-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="2f399-113">這個命令會取得具有 resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 的介面端點，並將它儲存在 $interfaceendpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f399-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="2f399-114">參數</span><span class="sxs-lookup"><span data-stu-id="2f399-114">PARAMETERS</span></span>

### <span data-ttu-id="2f399-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f399-115">-DefaultProfile</span></span>
<span data-ttu-id="2f399-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f399-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f399-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f399-117">-Name</span></span>
<span data-ttu-id="2f399-118">介面端點的名稱</span><span class="sxs-lookup"><span data-stu-id="2f399-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f399-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f399-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f399-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f399-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f399-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f399-121">-ResourceId</span></span>
<span data-ttu-id="2f399-122">{{Fill ResourceId 描述}}</span><span class="sxs-lookup"><span data-stu-id="2f399-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f399-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2f399-123">-Confirm</span></span>
<span data-ttu-id="2f399-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f399-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f399-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f399-125">-WhatIf</span></span>
<span data-ttu-id="2f399-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f399-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f399-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f399-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f399-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f399-128">CommonParameters</span></span>
<span data-ttu-id="2f399-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f399-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2f399-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f399-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f399-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2f399-131">INPUTS</span></span>

### <span data-ttu-id="2f399-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2f399-132">System.String</span></span>


## <span data-ttu-id="2f399-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2f399-133">OUTPUTS</span></span>

### <span data-ttu-id="2f399-134">PSInterfaceEndpoint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f399-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="2f399-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2f399-135">NOTES</span></span>

## <span data-ttu-id="2f399-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f399-136">RELATED LINKS</span></span>
