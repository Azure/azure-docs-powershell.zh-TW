---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448248"
---
# <span data-ttu-id="0c7c4-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0c7c4-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="0c7c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7c4-103">取得 managed 節點類型的資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="0c7c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c7c4-104">SYNTAX</span></span>

### <span data-ttu-id="0c7c4-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="0c7c4-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c7c4-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0c7c4-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7c4-107">說明</span><span class="sxs-lookup"><span data-stu-id="0c7c4-107">DESCRIPTION</span></span>
<span data-ttu-id="0c7c4-108">取得 managed 節點類型的資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="0c7c4-109">示例</span><span class="sxs-lookup"><span data-stu-id="0c7c4-109">EXAMPLES</span></span>

### <span data-ttu-id="0c7c4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0c7c4-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="0c7c4-111">取得節點類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-111">Get node type details.</span></span>

### <span data-ttu-id="0c7c4-112">範例2</span><span class="sxs-lookup"><span data-stu-id="0c7c4-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="0c7c4-113">在指定的群集下取得節點類型清單。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="0c7c4-114">參數</span><span class="sxs-lookup"><span data-stu-id="0c7c4-114">PARAMETERS</span></span>

### <span data-ttu-id="0c7c4-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0c7c4-115">-ClusterName</span></span>
<span data-ttu-id="0c7c4-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0c7c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7c4-117">-DefaultProfile</span></span>
<span data-ttu-id="0c7c4-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c7c4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c7c4-119">-Name</span></span>
<span data-ttu-id="0c7c4-120">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="0c7c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c7c4-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0c7c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7c4-123">CommonParameters</span></span>
<span data-ttu-id="0c7c4-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7c4-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7c4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0c7c4-126">INPUTS</span></span>

### <span data-ttu-id="0c7c4-127">System.object</span><span class="sxs-lookup"><span data-stu-id="0c7c4-127">System.String</span></span>

## <span data-ttu-id="0c7c4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0c7c4-128">OUTPUTS</span></span>

### <span data-ttu-id="0c7c4-129">PSManagedNodeType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="0c7c4-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="0c7c4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0c7c4-130">NOTES</span></span>

## <span data-ttu-id="0c7c4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c7c4-131">RELATED LINKS</span></span>
