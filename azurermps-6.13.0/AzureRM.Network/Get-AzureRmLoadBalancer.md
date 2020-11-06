---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 90cafc66857ee2ec94806628b41960eaafaf6e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449055"
---
# <span data-ttu-id="087b1-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="087b1-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="087b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="087b1-102">SYNOPSIS</span></span>
<span data-ttu-id="087b1-103">取得負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="087b1-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="087b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="087b1-104">SYNTAX</span></span>

### <span data-ttu-id="087b1-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="087b1-105">NoExpand (Default)</span></span>
```
Get-AzureRmLoadBalancer [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="087b1-106">擴充</span><span class="sxs-lookup"><span data-stu-id="087b1-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="087b1-107">說明</span><span class="sxs-lookup"><span data-stu-id="087b1-107">DESCRIPTION</span></span>
<span data-ttu-id="087b1-108">**AzureRmLoadBalancer** Cmdlet 會取得包含在資源群組中的一個或多個 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="087b1-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="087b1-109">示例</span><span class="sxs-lookup"><span data-stu-id="087b1-109">EXAMPLES</span></span>

### <span data-ttu-id="087b1-110">範例1：取得負載平衡器</span><span class="sxs-lookup"><span data-stu-id="087b1-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="087b1-111">這個命令會取得名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="087b1-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="087b1-112">必須先存在負載平衡器，才能執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="087b1-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="087b1-113">參數</span><span class="sxs-lookup"><span data-stu-id="087b1-113">PARAMETERS</span></span>

### <span data-ttu-id="087b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087b1-114">-DefaultProfile</span></span>
<span data-ttu-id="087b1-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="087b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="087b1-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="087b1-116">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="087b1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="087b1-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="087b1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="087b1-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="087b1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087b1-119">CommonParameters</span></span>
<span data-ttu-id="087b1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="087b1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087b1-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="087b1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087b1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="087b1-122">INPUTS</span></span>

### <span data-ttu-id="087b1-123">System.object</span><span class="sxs-lookup"><span data-stu-id="087b1-123">System.String</span></span>

## <span data-ttu-id="087b1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="087b1-124">OUTPUTS</span></span>

### <span data-ttu-id="087b1-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="087b1-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="087b1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="087b1-126">NOTES</span></span>

## <span data-ttu-id="087b1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="087b1-127">RELATED LINKS</span></span>

[<span data-ttu-id="087b1-128">新-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="087b1-128">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="087b1-129">移除-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="087b1-129">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="087b1-130">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="087b1-130">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


