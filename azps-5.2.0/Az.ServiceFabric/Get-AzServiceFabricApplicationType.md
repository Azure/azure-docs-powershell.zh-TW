---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279833"
---
# <span data-ttu-id="a142d-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a142d-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="a142d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a142d-102">SYNOPSIS</span></span>
<span data-ttu-id="a142d-103">取得 Service Fabric 應用程式類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a142d-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="a142d-104">僅支援 ARM 已部署的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="a142d-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="a142d-105">句法</span><span class="sxs-lookup"><span data-stu-id="a142d-105">SYNTAX</span></span>

### <span data-ttu-id="a142d-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="a142d-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a142d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a142d-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a142d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a142d-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a142d-109">說明</span><span class="sxs-lookup"><span data-stu-id="a142d-109">DESCRIPTION</span></span>
<span data-ttu-id="a142d-110">使用此 Cmdlet 來取得指定資源群組和群集中的應用程式類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a142d-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="a142d-111">示例</span><span class="sxs-lookup"><span data-stu-id="a142d-111">EXAMPLES</span></span>

### <span data-ttu-id="a142d-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a142d-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="a142d-113">這個範例會使用指定的參數來取得應用程式類型的詳細資料（如果沒有找到資源），它會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a142d-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="a142d-114">範例2</span><span class="sxs-lookup"><span data-stu-id="a142d-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="a142d-115">這個範例會取得在指定的群集底下定義的應用程式類型清單。</span><span class="sxs-lookup"><span data-stu-id="a142d-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="a142d-116">參數</span><span class="sxs-lookup"><span data-stu-id="a142d-116">PARAMETERS</span></span>

### <span data-ttu-id="a142d-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a142d-117">-ClusterName</span></span>
<span data-ttu-id="a142d-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a142d-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a142d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a142d-119">-DefaultProfile</span></span>
<span data-ttu-id="a142d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a142d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a142d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a142d-121">-Name</span></span>
<span data-ttu-id="a142d-122">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="a142d-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a142d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a142d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a142d-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a142d-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a142d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a142d-125">-ResourceId</span></span>
<span data-ttu-id="a142d-126">應用程式類型的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a142d-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="a142d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a142d-127">CommonParameters</span></span>
<span data-ttu-id="a142d-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a142d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a142d-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a142d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a142d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a142d-130">INPUTS</span></span>

### <span data-ttu-id="a142d-131">System.object</span><span class="sxs-lookup"><span data-stu-id="a142d-131">System.String</span></span>

## <span data-ttu-id="a142d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a142d-132">OUTPUTS</span></span>

### <span data-ttu-id="a142d-133">PSApplicationType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a142d-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="a142d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a142d-134">NOTES</span></span>

## <span data-ttu-id="a142d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a142d-135">RELATED LINKS</span></span>
