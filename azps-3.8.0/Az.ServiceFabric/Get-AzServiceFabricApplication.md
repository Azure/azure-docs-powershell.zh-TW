---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965737"
---
# <span data-ttu-id="a51d6-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a51d6-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="a51d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a51d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a51d6-103">取得 Service Fabric 應用程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a51d6-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="a51d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a51d6-104">SYNTAX</span></span>

### <span data-ttu-id="a51d6-105">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="a51d6-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a51d6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a51d6-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a51d6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a51d6-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a51d6-108">說明</span><span class="sxs-lookup"><span data-stu-id="a51d6-108">DESCRIPTION</span></span>
<span data-ttu-id="a51d6-109">這個 Cmdlet 會在指定的資源群組和群集中取得應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a51d6-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="a51d6-110">示例</span><span class="sxs-lookup"><span data-stu-id="a51d6-110">EXAMPLES</span></span>

### <span data-ttu-id="a51d6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a51d6-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="a51d6-112">這個範例會取得應用程式「testApp」的應用程式資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a51d6-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="a51d6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a51d6-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="a51d6-114">這個範例會取得群集「testCluster」下的應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="a51d6-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="a51d6-115">參數</span><span class="sxs-lookup"><span data-stu-id="a51d6-115">PARAMETERS</span></span>

### <span data-ttu-id="a51d6-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a51d6-116">-ClusterName</span></span>
<span data-ttu-id="a51d6-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a51d6-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a51d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51d6-118">-DefaultProfile</span></span>
<span data-ttu-id="a51d6-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a51d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a51d6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a51d6-120">-Name</span></span>
<span data-ttu-id="a51d6-121">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a51d6-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="a51d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a51d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="a51d6-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a51d6-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a51d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a51d6-124">-ResourceId</span></span>
<span data-ttu-id="a51d6-125">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a51d6-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="a51d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51d6-126">CommonParameters</span></span>
<span data-ttu-id="a51d6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a51d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51d6-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a51d6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51d6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a51d6-129">INPUTS</span></span>

### <span data-ttu-id="a51d6-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a51d6-130">System.String</span></span>

## <span data-ttu-id="a51d6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a51d6-131">OUTPUTS</span></span>

### <span data-ttu-id="a51d6-132">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a51d6-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="a51d6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a51d6-133">NOTES</span></span>

## <span data-ttu-id="a51d6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a51d6-134">RELATED LINKS</span></span>
