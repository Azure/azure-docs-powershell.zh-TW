---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 5a67faaf48d96a93fe1bc3e6380abb4fe6d03d98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902830"
---
# <span data-ttu-id="bea2d-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="bea2d-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="bea2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bea2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bea2d-103">取得受管理的組群資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bea2d-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="bea2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="bea2d-104">SYNTAX</span></span>

### <span data-ttu-id="bea2d-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="bea2d-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea2d-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bea2d-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bea2d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="bea2d-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bea2d-108">描述</span><span class="sxs-lookup"><span data-stu-id="bea2d-108">DESCRIPTION</span></span>
<span data-ttu-id="bea2d-109">取得受管理的組群資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bea2d-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="bea2d-110">例子</span><span class="sxs-lookup"><span data-stu-id="bea2d-110">EXAMPLES</span></span>

### <span data-ttu-id="bea2d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bea2d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="bea2d-112">取得組群詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bea2d-112">Get cluster details.</span></span>

### <span data-ttu-id="bea2d-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bea2d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="bea2d-114">取得指定資源群組下的群組清單。</span><span class="sxs-lookup"><span data-stu-id="bea2d-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="bea2d-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="bea2d-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="bea2d-116">取得目前訂閱下的組清單。</span><span class="sxs-lookup"><span data-stu-id="bea2d-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="bea2d-117">參數</span><span class="sxs-lookup"><span data-stu-id="bea2d-117">PARAMETERS</span></span>

### <span data-ttu-id="bea2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea2d-118">-DefaultProfile</span></span>
<span data-ttu-id="bea2d-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bea2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea2d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="bea2d-120">-Name</span></span>
<span data-ttu-id="bea2d-121">指定組名。</span><span class="sxs-lookup"><span data-stu-id="bea2d-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bea2d-123">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bea2d-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea2d-124">CommonParameters</span></span>
<span data-ttu-id="bea2d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bea2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea2d-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bea2d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea2d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bea2d-127">INPUTS</span></span>

### <span data-ttu-id="bea2d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bea2d-128">System.String</span></span>

## <span data-ttu-id="bea2d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bea2d-129">OUTPUTS</span></span>

### <span data-ttu-id="bea2d-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="bea2d-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="bea2d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bea2d-131">NOTES</span></span>

## <span data-ttu-id="bea2d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bea2d-132">RELATED LINKS</span></span>
