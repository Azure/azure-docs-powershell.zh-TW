---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: a0625a974da7d6544345419573fa4e96f0bbcae1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971729"
---
# <span data-ttu-id="9294c-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="9294c-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="9294c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9294c-102">SYNOPSIS</span></span>
<span data-ttu-id="9294c-103">取得 Service Fabric 應用程式類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9294c-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="9294c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9294c-104">SYNTAX</span></span>

### <span data-ttu-id="9294c-105">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="9294c-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9294c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9294c-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9294c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9294c-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9294c-108">說明</span><span class="sxs-lookup"><span data-stu-id="9294c-108">DESCRIPTION</span></span>
<span data-ttu-id="9294c-109">使用此 Cmdlet 來取得指定資源群組和群集中的應用程式類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9294c-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="9294c-110">示例</span><span class="sxs-lookup"><span data-stu-id="9294c-110">EXAMPLES</span></span>

### <span data-ttu-id="9294c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9294c-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="9294c-112">這個範例會使用指定的參數來取得應用程式類型的詳細資料（如果沒有找到資源），它會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="9294c-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="9294c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9294c-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="9294c-114">這個範例會取得在指定的群集底下定義的應用程式類型清單。</span><span class="sxs-lookup"><span data-stu-id="9294c-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="9294c-115">參數</span><span class="sxs-lookup"><span data-stu-id="9294c-115">PARAMETERS</span></span>

### <span data-ttu-id="9294c-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9294c-116">-ClusterName</span></span>
<span data-ttu-id="9294c-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9294c-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9294c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9294c-118">-DefaultProfile</span></span>
<span data-ttu-id="9294c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9294c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9294c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9294c-120">-Name</span></span>
<span data-ttu-id="9294c-121">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="9294c-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="9294c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9294c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9294c-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9294c-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9294c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9294c-124">-ResourceId</span></span>
<span data-ttu-id="9294c-125">應用程式類型的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="9294c-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="9294c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9294c-126">CommonParameters</span></span>
<span data-ttu-id="9294c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9294c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9294c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9294c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9294c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9294c-129">INPUTS</span></span>

### <span data-ttu-id="9294c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="9294c-130">System.String</span></span>

## <span data-ttu-id="9294c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9294c-131">OUTPUTS</span></span>

### <span data-ttu-id="9294c-132">PSApplicationType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="9294c-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="9294c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9294c-133">NOTES</span></span>

## <span data-ttu-id="9294c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9294c-134">RELATED LINKS</span></span>
