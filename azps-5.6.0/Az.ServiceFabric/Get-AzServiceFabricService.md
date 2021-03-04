---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 51e2efb18a6c39e6d3206697d552f49f74648712
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917893"
---
# <span data-ttu-id="a117a-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a117a-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="a117a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a117a-102">SYNOPSIS</span></span>
<span data-ttu-id="a117a-103">取得指定應用程式和組群下的 Service Fabric 服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a117a-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="a117a-104">僅支援 ARM 部署的服務。</span><span class="sxs-lookup"><span data-stu-id="a117a-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="a117a-105">語法</span><span class="sxs-lookup"><span data-stu-id="a117a-105">SYNTAX</span></span>

### <span data-ttu-id="a117a-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="a117a-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a117a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a117a-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a117a-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a117a-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a117a-109">描述</span><span class="sxs-lookup"><span data-stu-id="a117a-109">DESCRIPTION</span></span>
<span data-ttu-id="a117a-110">此 Cmdlet 會取得指定應用程式和組集中的服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a117a-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="a117a-111">例子</span><span class="sxs-lookup"><span data-stu-id="a117a-111">EXAMPLES</span></span>

### <span data-ttu-id="a117a-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a117a-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="a117a-113">此範例會獲得服務 "testApp~testService" 的服務資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a117a-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="a117a-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="a117a-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="a117a-115">此範例會獲得應用程式 "testApp" 下的服務清單。</span><span class="sxs-lookup"><span data-stu-id="a117a-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="a117a-116">參數</span><span class="sxs-lookup"><span data-stu-id="a117a-116">PARAMETERS</span></span>

### <span data-ttu-id="a117a-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a117a-117">-ApplicationName</span></span>
<span data-ttu-id="a117a-118">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a117a-118">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a117a-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a117a-119">-ClusterName</span></span>
<span data-ttu-id="a117a-120">指定組名。</span><span class="sxs-lookup"><span data-stu-id="a117a-120">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a117a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a117a-121">-DefaultProfile</span></span>
<span data-ttu-id="a117a-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a117a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a117a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a117a-123">-Name</span></span>
<span data-ttu-id="a117a-124">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a117a-124">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a117a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a117a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a117a-126">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a117a-126">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a117a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a117a-127">-ResourceId</span></span>
<span data-ttu-id="a117a-128">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a117a-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="a117a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a117a-129">CommonParameters</span></span>
<span data-ttu-id="a117a-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a117a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a117a-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a117a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a117a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a117a-132">INPUTS</span></span>

### <span data-ttu-id="a117a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a117a-133">System.String</span></span>

## <span data-ttu-id="a117a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a117a-134">OUTPUTS</span></span>

### <span data-ttu-id="a117a-135">Microsoft.Azure.Commands.ServiceFabric.models.PSService</span><span class="sxs-lookup"><span data-stu-id="a117a-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="a117a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a117a-136">NOTES</span></span>

## <span data-ttu-id="a117a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a117a-137">RELATED LINKS</span></span>
