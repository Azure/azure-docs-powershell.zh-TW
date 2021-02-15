---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142492"
---
# <span data-ttu-id="f9ad9-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f9ad9-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="f9ad9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ad9-103">取得 Service Fabric 應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="f9ad9-104">僅支援 ARM 已部署的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="f9ad9-105">句法</span><span class="sxs-lookup"><span data-stu-id="f9ad9-105">SYNTAX</span></span>

### <span data-ttu-id="f9ad9-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="f9ad9-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9ad9-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="f9ad9-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9ad9-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ad9-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9ad9-109">說明</span><span class="sxs-lookup"><span data-stu-id="f9ad9-109">DESCRIPTION</span></span>
<span data-ttu-id="f9ad9-110">使用此 Cmdlet 在指定的資源群組和群集中取得應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="f9ad9-111">示例</span><span class="sxs-lookup"><span data-stu-id="f9ad9-111">EXAMPLES</span></span>

### <span data-ttu-id="f9ad9-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f9ad9-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="f9ad9-113">這個範例會取得版本為「v1」的應用程式類型「testAppType」，找不到該資源將會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="f9ad9-114">範例2</span><span class="sxs-lookup"><span data-stu-id="f9ad9-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="f9ad9-115">這個範例會取得在指定的群集及類型下定義之應用程式類型版本的清單。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="f9ad9-116">參數</span><span class="sxs-lookup"><span data-stu-id="f9ad9-116">PARAMETERS</span></span>

### <span data-ttu-id="f9ad9-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f9ad9-117">-ClusterName</span></span>
<span data-ttu-id="f9ad9-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ad9-119">-DefaultProfile</span></span>
<span data-ttu-id="f9ad9-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9ad9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9ad9-121">-Name</span></span>
<span data-ttu-id="f9ad9-122">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-122">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9ad9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9ad9-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ad9-125">-ResourceId</span></span>
<span data-ttu-id="f9ad9-126">應用程式類型版本的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-126">Arm ResourceId of the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad9-127">-版本</span><span class="sxs-lookup"><span data-stu-id="f9ad9-127">-Version</span></span>
<span data-ttu-id="f9ad9-128">指定應用程式類型的版本。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-128">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ad9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ad9-129">CommonParameters</span></span>
<span data-ttu-id="f9ad9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ad9-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ad9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f9ad9-132">INPUTS</span></span>

### <span data-ttu-id="f9ad9-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f9ad9-133">System.String</span></span>

## <span data-ttu-id="f9ad9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f9ad9-134">OUTPUTS</span></span>

### <span data-ttu-id="f9ad9-135">PSApplicationTypeVersion 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="f9ad9-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="f9ad9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f9ad9-136">NOTES</span></span>

## <span data-ttu-id="f9ad9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9ad9-137">RELATED LINKS</span></span>
