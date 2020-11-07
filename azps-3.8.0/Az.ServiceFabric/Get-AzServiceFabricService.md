---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 62f1e4a9313ebcbd2ad6d815344dc18e5844ed13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957665"
---
# <span data-ttu-id="a920e-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a920e-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="a920e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a920e-102">SYNOPSIS</span></span>
<span data-ttu-id="a920e-103">在指定的應用程式和群集下取得服務結構服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a920e-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="a920e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a920e-104">SYNTAX</span></span>

### <span data-ttu-id="a920e-105">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="a920e-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a920e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a920e-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a920e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a920e-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a920e-108">說明</span><span class="sxs-lookup"><span data-stu-id="a920e-108">DESCRIPTION</span></span>
<span data-ttu-id="a920e-109">這個 Cmdlet 會在指定的應用程式和群集中取得服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a920e-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="a920e-110">示例</span><span class="sxs-lookup"><span data-stu-id="a920e-110">EXAMPLES</span></span>

### <span data-ttu-id="a920e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a920e-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="a920e-112">這個範例會取得服務「testApp ~ testService」的服務資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a920e-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="a920e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a920e-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="a920e-114">這個範例會在應用程式 "testApp" 下取得服務清單。</span><span class="sxs-lookup"><span data-stu-id="a920e-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="a920e-115">參數</span><span class="sxs-lookup"><span data-stu-id="a920e-115">PARAMETERS</span></span>

### <span data-ttu-id="a920e-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a920e-116">-ApplicationName</span></span>
<span data-ttu-id="a920e-117">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a920e-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="a920e-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a920e-118">-ClusterName</span></span>
<span data-ttu-id="a920e-119">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a920e-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a920e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a920e-120">-DefaultProfile</span></span>
<span data-ttu-id="a920e-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a920e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a920e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a920e-122">-Name</span></span>
<span data-ttu-id="a920e-123">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a920e-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="a920e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a920e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a920e-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a920e-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a920e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a920e-126">-ResourceId</span></span>
<span data-ttu-id="a920e-127">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a920e-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="a920e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a920e-128">CommonParameters</span></span>
<span data-ttu-id="a920e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a920e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a920e-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a920e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a920e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a920e-131">INPUTS</span></span>

### <span data-ttu-id="a920e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="a920e-132">System.String</span></span>

## <span data-ttu-id="a920e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a920e-133">OUTPUTS</span></span>

### <span data-ttu-id="a920e-134">PSService 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a920e-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="a920e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a920e-135">NOTES</span></span>

## <span data-ttu-id="a920e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a920e-136">RELATED LINKS</span></span>
