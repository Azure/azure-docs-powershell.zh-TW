---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142497"
---
# <span data-ttu-id="546fe-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="546fe-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="546fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="546fe-102">SYNOPSIS</span></span>
<span data-ttu-id="546fe-103">取得 Service Fabric 應用程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="546fe-103">Get Service Fabric application details.</span></span> <span data-ttu-id="546fe-104">僅支援 ARM 部署的應用程式。</span><span class="sxs-lookup"><span data-stu-id="546fe-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="546fe-105">句法</span><span class="sxs-lookup"><span data-stu-id="546fe-105">SYNTAX</span></span>

### <span data-ttu-id="546fe-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="546fe-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546fe-107">ByName</span><span class="sxs-lookup"><span data-stu-id="546fe-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546fe-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="546fe-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="546fe-109">說明</span><span class="sxs-lookup"><span data-stu-id="546fe-109">DESCRIPTION</span></span>
<span data-ttu-id="546fe-110">這個 Cmdlet 會在指定的資源群組和群集中取得應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="546fe-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="546fe-111">示例</span><span class="sxs-lookup"><span data-stu-id="546fe-111">EXAMPLES</span></span>

### <span data-ttu-id="546fe-112">範例1</span><span class="sxs-lookup"><span data-stu-id="546fe-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="546fe-113">這個範例會取得應用程式「testApp」的應用程式資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="546fe-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="546fe-114">範例2</span><span class="sxs-lookup"><span data-stu-id="546fe-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="546fe-115">這個範例會取得群集「testCluster」下的應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="546fe-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="546fe-116">參數</span><span class="sxs-lookup"><span data-stu-id="546fe-116">PARAMETERS</span></span>

### <span data-ttu-id="546fe-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="546fe-117">-ClusterName</span></span>
<span data-ttu-id="546fe-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="546fe-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="546fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546fe-119">-DefaultProfile</span></span>
<span data-ttu-id="546fe-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="546fe-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="546fe-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="546fe-121">-Name</span></span>
<span data-ttu-id="546fe-122">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="546fe-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="546fe-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="546fe-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="546fe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="546fe-125">-ResourceId</span></span>
<span data-ttu-id="546fe-126">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="546fe-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="546fe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546fe-127">CommonParameters</span></span>
<span data-ttu-id="546fe-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="546fe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546fe-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="546fe-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546fe-130">輸入</span><span class="sxs-lookup"><span data-stu-id="546fe-130">INPUTS</span></span>

### <span data-ttu-id="546fe-131">System.object</span><span class="sxs-lookup"><span data-stu-id="546fe-131">System.String</span></span>

## <span data-ttu-id="546fe-132">輸出</span><span class="sxs-lookup"><span data-stu-id="546fe-132">OUTPUTS</span></span>

### <span data-ttu-id="546fe-133">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="546fe-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="546fe-134">筆記</span><span class="sxs-lookup"><span data-stu-id="546fe-134">NOTES</span></span>

## <span data-ttu-id="546fe-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="546fe-135">RELATED LINKS</span></span>
