---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794423"
---
# <span data-ttu-id="96a5a-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96a5a-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="96a5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="96a5a-103">取得負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="96a5a-103">Gets a load balancer.</span></span>

## <span data-ttu-id="96a5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="96a5a-104">SYNTAX</span></span>

### <span data-ttu-id="96a5a-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="96a5a-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96a5a-106">擴充</span><span class="sxs-lookup"><span data-stu-id="96a5a-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96a5a-107">說明</span><span class="sxs-lookup"><span data-stu-id="96a5a-107">DESCRIPTION</span></span>
<span data-ttu-id="96a5a-108">**AzLoadBalancer** Cmdlet 會取得包含在資源群組中的一個或多個 Azure 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="96a5a-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="96a5a-109">示例</span><span class="sxs-lookup"><span data-stu-id="96a5a-109">EXAMPLES</span></span>

### <span data-ttu-id="96a5a-110">範例1：取得負載平衡器</span><span class="sxs-lookup"><span data-stu-id="96a5a-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="96a5a-111">這個命令會取得名為 MyLoadBalancer 的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="96a5a-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="96a5a-112">必須先存在負載平衡器，才能執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96a5a-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="96a5a-113">參數</span><span class="sxs-lookup"><span data-stu-id="96a5a-113">PARAMETERS</span></span>

### <span data-ttu-id="96a5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a5a-114">-DefaultProfile</span></span>
<span data-ttu-id="96a5a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96a5a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96a5a-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="96a5a-116">-ExpandResource</span></span>
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

### <span data-ttu-id="96a5a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="96a5a-117">-Name</span></span>
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

### <span data-ttu-id="96a5a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a5a-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="96a5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a5a-119">CommonParameters</span></span>
<span data-ttu-id="96a5a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96a5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a5a-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96a5a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a5a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="96a5a-122">INPUTS</span></span>

## <span data-ttu-id="96a5a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="96a5a-123">OUTPUTS</span></span>

### <span data-ttu-id="96a5a-124">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="96a5a-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="96a5a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="96a5a-125">NOTES</span></span>

## <span data-ttu-id="96a5a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="96a5a-126">RELATED LINKS</span></span>

[<span data-ttu-id="96a5a-127">新-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96a5a-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="96a5a-128">移除-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96a5a-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="96a5a-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="96a5a-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


