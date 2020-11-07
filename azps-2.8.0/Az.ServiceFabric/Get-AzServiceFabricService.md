---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 3076a405c47f165d2ace1e5251644cf4e4484a03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790950"
---
# <span data-ttu-id="2583b-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2583b-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="2583b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2583b-102">SYNOPSIS</span></span>
<span data-ttu-id="2583b-103">在指定的應用程式和群集下取得服務結構服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2583b-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="2583b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2583b-104">SYNTAX</span></span>

### <span data-ttu-id="2583b-105">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="2583b-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2583b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2583b-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2583b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2583b-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2583b-108">說明</span><span class="sxs-lookup"><span data-stu-id="2583b-108">DESCRIPTION</span></span>
<span data-ttu-id="2583b-109">這個 Cmdlet 會在指定的應用程式和群集中取得服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2583b-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="2583b-110">示例</span><span class="sxs-lookup"><span data-stu-id="2583b-110">EXAMPLES</span></span>

### <span data-ttu-id="2583b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2583b-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="2583b-112">這個範例會取得服務「testApp ~ testService」的服務資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2583b-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="2583b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="2583b-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="2583b-114">這個範例會取得 aplication "testApp" 下的服務清單。</span><span class="sxs-lookup"><span data-stu-id="2583b-114">This example gets a list of the services under the aplication "testApp".</span></span>

## <span data-ttu-id="2583b-115">參數</span><span class="sxs-lookup"><span data-stu-id="2583b-115">PARAMETERS</span></span>

### <span data-ttu-id="2583b-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="2583b-116">-ApplicationName</span></span>
<span data-ttu-id="2583b-117">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2583b-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="2583b-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2583b-118">-ClusterName</span></span>
<span data-ttu-id="2583b-119">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2583b-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2583b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2583b-120">-DefaultProfile</span></span>
<span data-ttu-id="2583b-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2583b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2583b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2583b-122">-Name</span></span>
<span data-ttu-id="2583b-123">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2583b-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="2583b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2583b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2583b-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2583b-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2583b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2583b-126">-ResourceId</span></span>
<span data-ttu-id="2583b-127">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="2583b-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="2583b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2583b-128">CommonParameters</span></span>
<span data-ttu-id="2583b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2583b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2583b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2583b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2583b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2583b-131">INPUTS</span></span>

### <span data-ttu-id="2583b-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2583b-132">System.String</span></span>

## <span data-ttu-id="2583b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2583b-133">OUTPUTS</span></span>

### <span data-ttu-id="2583b-134">PSService 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="2583b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="2583b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2583b-135">NOTES</span></span>

## <span data-ttu-id="2583b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2583b-136">RELATED LINKS</span></span>
