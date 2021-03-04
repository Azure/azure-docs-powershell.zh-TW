---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 0082f5625351b8bb8e832ad60eb76837f09ccd47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907502"
---
# <span data-ttu-id="1b190-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1b190-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="1b190-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b190-102">SYNOPSIS</span></span>
<span data-ttu-id="1b190-103">取得 Service Fabric 應用程式類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1b190-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="1b190-104">僅支援 ARM 部署的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="1b190-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="1b190-105">語法</span><span class="sxs-lookup"><span data-stu-id="1b190-105">SYNTAX</span></span>

### <span data-ttu-id="1b190-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="1b190-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b190-107">ByName</span><span class="sxs-lookup"><span data-stu-id="1b190-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b190-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b190-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b190-109">描述</span><span class="sxs-lookup"><span data-stu-id="1b190-109">DESCRIPTION</span></span>
<span data-ttu-id="1b190-110">使用此 Cmdlet 取得指定資源群組和群組中的應用程式類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1b190-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="1b190-111">例子</span><span class="sxs-lookup"><span data-stu-id="1b190-111">EXAMPLES</span></span>

### <span data-ttu-id="1b190-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="1b190-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="1b190-113">此範例會取得具有指定參數的應用程式類型詳細資料，如果找不到資源，就會引發例外。</span><span class="sxs-lookup"><span data-stu-id="1b190-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="1b190-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="1b190-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="1b190-115">此範例會取得指定組群下定義的應用程式類型清單。</span><span class="sxs-lookup"><span data-stu-id="1b190-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="1b190-116">參數</span><span class="sxs-lookup"><span data-stu-id="1b190-116">PARAMETERS</span></span>

### <span data-ttu-id="1b190-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1b190-117">-ClusterName</span></span>
<span data-ttu-id="1b190-118">指定組名。</span><span class="sxs-lookup"><span data-stu-id="1b190-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1b190-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b190-119">-DefaultProfile</span></span>
<span data-ttu-id="1b190-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b190-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b190-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b190-121">-Name</span></span>
<span data-ttu-id="1b190-122">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="1b190-122">Specify the name of the application type</span></span>

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

### <span data-ttu-id="1b190-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b190-123">-ResourceGroupName</span></span>
<span data-ttu-id="1b190-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b190-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1b190-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b190-125">-ResourceId</span></span>
<span data-ttu-id="1b190-126">應用程式類型的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1b190-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="1b190-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b190-127">CommonParameters</span></span>
<span data-ttu-id="1b190-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b190-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b190-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b190-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b190-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1b190-130">INPUTS</span></span>

### <span data-ttu-id="1b190-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1b190-131">System.String</span></span>

## <span data-ttu-id="1b190-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1b190-132">OUTPUTS</span></span>

### <span data-ttu-id="1b190-133">Microsoft.Azure.Commands.ServiceFabric.models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="1b190-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="1b190-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1b190-134">NOTES</span></span>

## <span data-ttu-id="1b190-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b190-135">RELATED LINKS</span></span>
