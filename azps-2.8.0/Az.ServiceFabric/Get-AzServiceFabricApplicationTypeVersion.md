---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 0af0b8ac4f632682ee60bd691c41fb4500c2c2a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790954"
---
# <span data-ttu-id="6ac00-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6ac00-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="6ac00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ac00-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac00-103">取得 Service Fabric 應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6ac00-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="6ac00-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ac00-104">SYNTAX</span></span>

### <span data-ttu-id="6ac00-105">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="6ac00-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ac00-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="6ac00-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ac00-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ac00-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ac00-108">說明</span><span class="sxs-lookup"><span data-stu-id="6ac00-108">DESCRIPTION</span></span>
<span data-ttu-id="6ac00-109">使用此 Cmdlet 在指定的資源群組和群集中取得應用程式類型版本詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6ac00-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="6ac00-110">示例</span><span class="sxs-lookup"><span data-stu-id="6ac00-110">EXAMPLES</span></span>

### <span data-ttu-id="6ac00-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6ac00-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="6ac00-112">這個範例會取得版本為「v1」的應用程式類型「testAppType」，找不到該資源將會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6ac00-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="6ac00-113">範例2</span><span class="sxs-lookup"><span data-stu-id="6ac00-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="6ac00-114">這個範例會取得在指定的群集及類型下定義之應用程式類型版本的清單。</span><span class="sxs-lookup"><span data-stu-id="6ac00-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="6ac00-115">參數</span><span class="sxs-lookup"><span data-stu-id="6ac00-115">PARAMETERS</span></span>

### <span data-ttu-id="6ac00-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6ac00-116">-ClusterName</span></span>
<span data-ttu-id="6ac00-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac00-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6ac00-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac00-118">-DefaultProfile</span></span>
<span data-ttu-id="6ac00-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ac00-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ac00-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ac00-120">-Name</span></span>
<span data-ttu-id="6ac00-121">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac00-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="6ac00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac00-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ac00-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac00-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6ac00-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ac00-124">-ResourceId</span></span>
<span data-ttu-id="6ac00-125">應用程式類型版本的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="6ac00-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="6ac00-126">-版本</span><span class="sxs-lookup"><span data-stu-id="6ac00-126">-Version</span></span>
<span data-ttu-id="6ac00-127">指定應用程式類型的版本。</span><span class="sxs-lookup"><span data-stu-id="6ac00-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="6ac00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac00-128">CommonParameters</span></span>
<span data-ttu-id="6ac00-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ac00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac00-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ac00-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac00-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6ac00-131">INPUTS</span></span>

### <span data-ttu-id="6ac00-132">System.object</span><span class="sxs-lookup"><span data-stu-id="6ac00-132">System.String</span></span>

## <span data-ttu-id="6ac00-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6ac00-133">OUTPUTS</span></span>

### <span data-ttu-id="6ac00-134">PSApplicationTypeVersion 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="6ac00-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="6ac00-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6ac00-135">NOTES</span></span>

## <span data-ttu-id="6ac00-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ac00-136">RELATED LINKS</span></span>
