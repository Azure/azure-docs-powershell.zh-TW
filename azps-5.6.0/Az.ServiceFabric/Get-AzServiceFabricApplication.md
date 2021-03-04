---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 346664d4714836b9965088d946262257e76747e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904826"
---
# <span data-ttu-id="ded84-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ded84-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ded84-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ded84-102">SYNOPSIS</span></span>
<span data-ttu-id="ded84-103">取得 Service Fabric 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ded84-103">Get Service Fabric application details.</span></span> <span data-ttu-id="ded84-104">僅支援 ARM 部署的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ded84-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="ded84-105">語法</span><span class="sxs-lookup"><span data-stu-id="ded84-105">SYNTAX</span></span>

### <span data-ttu-id="ded84-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="ded84-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ded84-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ded84-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ded84-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ded84-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ded84-109">描述</span><span class="sxs-lookup"><span data-stu-id="ded84-109">DESCRIPTION</span></span>
<span data-ttu-id="ded84-110">此 Cmdlet 會獲得指定資源群組和群組中的應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ded84-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="ded84-111">例子</span><span class="sxs-lookup"><span data-stu-id="ded84-111">EXAMPLES</span></span>

### <span data-ttu-id="ded84-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="ded84-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="ded84-113">此範例會獲得應用程式 "testApp" 的應用程式資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ded84-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="ded84-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="ded84-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="ded84-115">此範例會取得「testCluster」叢集下的應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="ded84-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="ded84-116">參數</span><span class="sxs-lookup"><span data-stu-id="ded84-116">PARAMETERS</span></span>

### <span data-ttu-id="ded84-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ded84-117">-ClusterName</span></span>
<span data-ttu-id="ded84-118">指定組名。</span><span class="sxs-lookup"><span data-stu-id="ded84-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ded84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded84-119">-DefaultProfile</span></span>
<span data-ttu-id="ded84-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ded84-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ded84-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ded84-121">-Name</span></span>
<span data-ttu-id="ded84-122">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ded84-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="ded84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded84-123">-ResourceGroupName</span></span>
<span data-ttu-id="ded84-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ded84-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ded84-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ded84-125">-ResourceId</span></span>
<span data-ttu-id="ded84-126">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ded84-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ded84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded84-127">CommonParameters</span></span>
<span data-ttu-id="ded84-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ded84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded84-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ded84-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded84-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ded84-130">INPUTS</span></span>

### <span data-ttu-id="ded84-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ded84-131">System.String</span></span>

## <span data-ttu-id="ded84-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ded84-132">OUTPUTS</span></span>

### <span data-ttu-id="ded84-133">Microsoft.Azure.Commands.ServiceFabric.models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ded84-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ded84-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ded84-134">NOTES</span></span>

## <span data-ttu-id="ded84-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ded84-135">RELATED LINKS</span></span>
