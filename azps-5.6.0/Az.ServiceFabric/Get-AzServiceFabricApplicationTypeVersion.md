---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 9c9f1b3c88e49eca3be8a923324d195d3a773c1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907501"
---
# <span data-ttu-id="8c195-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8c195-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="8c195-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c195-102">SYNOPSIS</span></span>
<span data-ttu-id="8c195-103">取得 Service Fabric 應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c195-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="8c195-104">僅支援 ARM 部署的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="8c195-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="8c195-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c195-105">SYNTAX</span></span>

### <span data-ttu-id="8c195-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="8c195-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c195-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="8c195-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c195-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c195-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c195-109">描述</span><span class="sxs-lookup"><span data-stu-id="8c195-109">DESCRIPTION</span></span>
<span data-ttu-id="8c195-110">使用此 Cmdlet 取得指定資源群組和群組中的應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c195-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="8c195-111">例子</span><span class="sxs-lookup"><span data-stu-id="8c195-111">EXAMPLES</span></span>

### <span data-ttu-id="8c195-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="8c195-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="8c195-113">此範例會使用版本 "v1" 的應用程式類型"testAppType"，如果找不到資源，就會傳出例外。</span><span class="sxs-lookup"><span data-stu-id="8c195-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="8c195-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="8c195-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="8c195-115">此範例會獲得指定組群和類型下定義的應用程式類型版本清單。</span><span class="sxs-lookup"><span data-stu-id="8c195-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="8c195-116">參數</span><span class="sxs-lookup"><span data-stu-id="8c195-116">PARAMETERS</span></span>

### <span data-ttu-id="8c195-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8c195-117">-ClusterName</span></span>
<span data-ttu-id="8c195-118">指定組名。</span><span class="sxs-lookup"><span data-stu-id="8c195-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8c195-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c195-119">-DefaultProfile</span></span>
<span data-ttu-id="8c195-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c195-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c195-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c195-121">-Name</span></span>
<span data-ttu-id="8c195-122">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c195-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="8c195-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c195-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c195-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c195-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8c195-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c195-125">-ResourceId</span></span>
<span data-ttu-id="8c195-126">應用程式類型版本的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="8c195-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="8c195-127">-版本</span><span class="sxs-lookup"><span data-stu-id="8c195-127">-Version</span></span>
<span data-ttu-id="8c195-128">指定應用程式類型的版本。</span><span class="sxs-lookup"><span data-stu-id="8c195-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="8c195-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c195-129">CommonParameters</span></span>
<span data-ttu-id="8c195-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c195-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c195-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c195-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c195-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8c195-132">INPUTS</span></span>

### <span data-ttu-id="8c195-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8c195-133">System.String</span></span>

## <span data-ttu-id="8c195-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8c195-134">OUTPUTS</span></span>

### <span data-ttu-id="8c195-135">Microsoft.Azure.Commands.ServiceFabric.models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8c195-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="8c195-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8c195-136">NOTES</span></span>

## <span data-ttu-id="8c195-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c195-137">RELATED LINKS</span></span>
