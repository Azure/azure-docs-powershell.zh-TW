---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 764d26c2b0b95b74277fc74dab03fe55d12261f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452456"
---
# <span data-ttu-id="ac8ed-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ac8ed-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="ac8ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8ed-103">取得負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ac8ed-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac8ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac8ed-104">SYNTAX</span></span>

### <span data-ttu-id="ac8ed-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ac8ed-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac8ed-106">擴充</span><span class="sxs-lookup"><span data-stu-id="ac8ed-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac8ed-107">說明</span><span class="sxs-lookup"><span data-stu-id="ac8ed-107">DESCRIPTION</span></span>
<span data-ttu-id="ac8ed-108">**AzureRmLoadBalancer** Cmdlet 會取得包含在資源群組中的一個或多個 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ac8ed-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="ac8ed-109">示例</span><span class="sxs-lookup"><span data-stu-id="ac8ed-109">EXAMPLES</span></span>

### <span data-ttu-id="ac8ed-110">範例1：取得負載平衡器</span><span class="sxs-lookup"><span data-stu-id="ac8ed-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ac8ed-111">這個命令會取得名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="ac8ed-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="ac8ed-112">必須先存在負載平衡器，才能執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac8ed-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="ac8ed-113">參數</span><span class="sxs-lookup"><span data-stu-id="ac8ed-113">PARAMETERS</span></span>

### <span data-ttu-id="ac8ed-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ac8ed-114">-ExpandResource</span></span>
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

### <span data-ttu-id="ac8ed-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac8ed-115">-Name</span></span>
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

### <span data-ttu-id="ac8ed-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac8ed-116">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ac8ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8ed-117">-DefaultProfile</span></span>
<span data-ttu-id="ac8ed-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac8ed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac8ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8ed-119">CommonParameters</span></span>
<span data-ttu-id="ac8ed-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac8ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8ed-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac8ed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8ed-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ac8ed-122">INPUTS</span></span>

## <span data-ttu-id="ac8ed-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ac8ed-123">OUTPUTS</span></span>

### <span data-ttu-id="ac8ed-124">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ac8ed-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ac8ed-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ac8ed-125">NOTES</span></span>

## <span data-ttu-id="ac8ed-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac8ed-126">RELATED LINKS</span></span>

[<span data-ttu-id="ac8ed-127">新-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ac8ed-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="ac8ed-128">移除-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ac8ed-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="ac8ed-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ac8ed-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


