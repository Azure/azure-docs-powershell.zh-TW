---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448259"
---
# <span data-ttu-id="f509a-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f509a-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="f509a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f509a-102">SYNOPSIS</span></span>
<span data-ttu-id="f509a-103">取得受管理的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f509a-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="f509a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f509a-104">SYNTAX</span></span>

### <span data-ttu-id="f509a-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="f509a-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f509a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f509a-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f509a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="f509a-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f509a-108">說明</span><span class="sxs-lookup"><span data-stu-id="f509a-108">DESCRIPTION</span></span>
<span data-ttu-id="f509a-109">取得受管理的群集資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f509a-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="f509a-110">示例</span><span class="sxs-lookup"><span data-stu-id="f509a-110">EXAMPLES</span></span>

### <span data-ttu-id="f509a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f509a-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="f509a-112">取得群集詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f509a-112">Get cluster details.</span></span>

### <span data-ttu-id="f509a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f509a-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="f509a-114">在指定的資源群組下取得群集清單。</span><span class="sxs-lookup"><span data-stu-id="f509a-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="f509a-115">範例3</span><span class="sxs-lookup"><span data-stu-id="f509a-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="f509a-116">在目前的訂閱下方取得群集清單。</span><span class="sxs-lookup"><span data-stu-id="f509a-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="f509a-117">參數</span><span class="sxs-lookup"><span data-stu-id="f509a-117">PARAMETERS</span></span>

### <span data-ttu-id="f509a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f509a-118">-DefaultProfile</span></span>
<span data-ttu-id="f509a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f509a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f509a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f509a-120">-Name</span></span>
<span data-ttu-id="f509a-121">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f509a-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f509a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f509a-122">-ResourceGroupName</span></span>
<span data-ttu-id="f509a-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f509a-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f509a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f509a-124">CommonParameters</span></span>
<span data-ttu-id="f509a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f509a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f509a-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f509a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f509a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f509a-127">INPUTS</span></span>

### <span data-ttu-id="f509a-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f509a-128">System.String</span></span>

## <span data-ttu-id="f509a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f509a-129">OUTPUTS</span></span>

### <span data-ttu-id="f509a-130">PSManagedCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="f509a-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="f509a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f509a-131">NOTES</span></span>

## <span data-ttu-id="f509a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f509a-132">RELATED LINKS</span></span>
