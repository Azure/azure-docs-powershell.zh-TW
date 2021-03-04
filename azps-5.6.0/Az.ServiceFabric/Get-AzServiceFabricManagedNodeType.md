---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 15ba499908a4a631a22f9064b1938d3b32fdafd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902829"
---
# <span data-ttu-id="3a860-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3a860-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="3a860-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a860-102">SYNOPSIS</span></span>
<span data-ttu-id="3a860-103">取得受管理的節點類型資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3a860-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="3a860-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a860-104">SYNTAX</span></span>

### <span data-ttu-id="3a860-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="3a860-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a860-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a860-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a860-107">描述</span><span class="sxs-lookup"><span data-stu-id="3a860-107">DESCRIPTION</span></span>
<span data-ttu-id="3a860-108">取得受管理的節點類型資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3a860-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="3a860-109">例子</span><span class="sxs-lookup"><span data-stu-id="3a860-109">EXAMPLES</span></span>

### <span data-ttu-id="3a860-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3a860-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="3a860-111">取得節點類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3a860-111">Get node type details.</span></span>

### <span data-ttu-id="3a860-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="3a860-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="3a860-113">取得指定集區下的節點類型清單。</span><span class="sxs-lookup"><span data-stu-id="3a860-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="3a860-114">參數</span><span class="sxs-lookup"><span data-stu-id="3a860-114">PARAMETERS</span></span>

### <span data-ttu-id="3a860-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3a860-115">-ClusterName</span></span>
<span data-ttu-id="3a860-116">指定組名。</span><span class="sxs-lookup"><span data-stu-id="3a860-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a860-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a860-117">-DefaultProfile</span></span>
<span data-ttu-id="3a860-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a860-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a860-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a860-119">-Name</span></span>
<span data-ttu-id="3a860-120">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a860-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a860-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a860-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a860-122">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a860-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a860-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a860-123">CommonParameters</span></span>
<span data-ttu-id="3a860-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a860-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a860-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a860-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a860-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3a860-126">INPUTS</span></span>

### <span data-ttu-id="3a860-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3a860-127">System.String</span></span>

## <span data-ttu-id="3a860-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3a860-128">OUTPUTS</span></span>

### <span data-ttu-id="3a860-129">Microsoft.Azure.Commands.ServiceFabric.models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="3a860-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="3a860-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3a860-130">NOTES</span></span>

## <span data-ttu-id="3a860-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a860-131">RELATED LINKS</span></span>
