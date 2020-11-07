---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 39bbf3a30f4334e35f58109da86b9b07208682af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800865"
---
# <span data-ttu-id="38a64-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38a64-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="38a64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38a64-102">SYNOPSIS</span></span>
<span data-ttu-id="38a64-103">取得負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="38a64-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38a64-104">句法</span><span class="sxs-lookup"><span data-stu-id="38a64-104">SYNTAX</span></span>

### <span data-ttu-id="38a64-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="38a64-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a64-106">擴充</span><span class="sxs-lookup"><span data-stu-id="38a64-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a64-107">說明</span><span class="sxs-lookup"><span data-stu-id="38a64-107">DESCRIPTION</span></span>
<span data-ttu-id="38a64-108">**AzureRmLoadBalancer** Cmdlet 會取得包含在資源群組中的一個或多個 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="38a64-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="38a64-109">示例</span><span class="sxs-lookup"><span data-stu-id="38a64-109">EXAMPLES</span></span>

### <span data-ttu-id="38a64-110">範例1：取得負載平衡器</span><span class="sxs-lookup"><span data-stu-id="38a64-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="38a64-111">這個命令會取得名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="38a64-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="38a64-112">必須先存在負載平衡器，才能執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38a64-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="38a64-113">參數</span><span class="sxs-lookup"><span data-stu-id="38a64-113">PARAMETERS</span></span>

### <span data-ttu-id="38a64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a64-114">-DefaultProfile</span></span>
<span data-ttu-id="38a64-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38a64-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38a64-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="38a64-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a64-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="38a64-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a64-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a64-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a64-119">CommonParameters</span></span>
<span data-ttu-id="38a64-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38a64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a64-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38a64-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a64-122">輸入</span><span class="sxs-lookup"><span data-stu-id="38a64-122">INPUTS</span></span>

## <span data-ttu-id="38a64-123">輸出</span><span class="sxs-lookup"><span data-stu-id="38a64-123">OUTPUTS</span></span>

### <span data-ttu-id="38a64-124">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="38a64-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="38a64-125">筆記</span><span class="sxs-lookup"><span data-stu-id="38a64-125">NOTES</span></span>

## <span data-ttu-id="38a64-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="38a64-126">RELATED LINKS</span></span>

[<span data-ttu-id="38a64-127">新-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38a64-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="38a64-128">移除-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38a64-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="38a64-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38a64-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


