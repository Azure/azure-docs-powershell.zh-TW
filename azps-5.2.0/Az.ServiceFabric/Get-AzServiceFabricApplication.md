---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273275"
---
# <span data-ttu-id="31a7b-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="31a7b-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="31a7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="31a7b-103">取得 Service Fabric 應用程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="31a7b-103">Get Service Fabric application details.</span></span> <span data-ttu-id="31a7b-104">僅支援 ARM 部署的應用程式。</span><span class="sxs-lookup"><span data-stu-id="31a7b-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="31a7b-105">句法</span><span class="sxs-lookup"><span data-stu-id="31a7b-105">SYNTAX</span></span>

### <span data-ttu-id="31a7b-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="31a7b-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31a7b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="31a7b-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31a7b-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="31a7b-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31a7b-109">說明</span><span class="sxs-lookup"><span data-stu-id="31a7b-109">DESCRIPTION</span></span>
<span data-ttu-id="31a7b-110">這個 Cmdlet 會在指定的資源群組和群集中取得應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="31a7b-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="31a7b-111">示例</span><span class="sxs-lookup"><span data-stu-id="31a7b-111">EXAMPLES</span></span>

### <span data-ttu-id="31a7b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="31a7b-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="31a7b-113">這個範例會取得應用程式「testApp」的應用程式資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="31a7b-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="31a7b-114">範例2</span><span class="sxs-lookup"><span data-stu-id="31a7b-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="31a7b-115">這個範例會取得群集「testCluster」下的應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="31a7b-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="31a7b-116">參數</span><span class="sxs-lookup"><span data-stu-id="31a7b-116">PARAMETERS</span></span>

### <span data-ttu-id="31a7b-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="31a7b-117">-ClusterName</span></span>
<span data-ttu-id="31a7b-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="31a7b-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="31a7b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a7b-119">-DefaultProfile</span></span>
<span data-ttu-id="31a7b-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31a7b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a7b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="31a7b-121">-Name</span></span>
<span data-ttu-id="31a7b-122">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="31a7b-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="31a7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="31a7b-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31a7b-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="31a7b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31a7b-125">-ResourceId</span></span>
<span data-ttu-id="31a7b-126">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="31a7b-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="31a7b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a7b-127">CommonParameters</span></span>
<span data-ttu-id="31a7b-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31a7b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a7b-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="31a7b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a7b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="31a7b-130">INPUTS</span></span>

### <span data-ttu-id="31a7b-131">System.object</span><span class="sxs-lookup"><span data-stu-id="31a7b-131">System.String</span></span>

## <span data-ttu-id="31a7b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="31a7b-132">OUTPUTS</span></span>

### <span data-ttu-id="31a7b-133">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="31a7b-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="31a7b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="31a7b-134">NOTES</span></span>

## <span data-ttu-id="31a7b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="31a7b-135">RELATED LINKS</span></span>
