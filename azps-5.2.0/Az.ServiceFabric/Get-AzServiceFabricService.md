---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273272"
---
# <span data-ttu-id="797dd-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="797dd-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="797dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="797dd-102">SYNOPSIS</span></span>
<span data-ttu-id="797dd-103">在指定的應用程式和群集下取得服務結構服務的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="797dd-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="797dd-104">僅支援 ARM 部署服務。</span><span class="sxs-lookup"><span data-stu-id="797dd-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="797dd-105">句法</span><span class="sxs-lookup"><span data-stu-id="797dd-105">SYNTAX</span></span>

### <span data-ttu-id="797dd-106">ByResourceGroupAndCluster (預設) </span><span class="sxs-lookup"><span data-stu-id="797dd-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="797dd-107">ByName</span><span class="sxs-lookup"><span data-stu-id="797dd-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="797dd-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="797dd-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="797dd-109">說明</span><span class="sxs-lookup"><span data-stu-id="797dd-109">DESCRIPTION</span></span>
<span data-ttu-id="797dd-110">這個 Cmdlet 會在指定的應用程式和群集中取得服務詳細資料。</span><span class="sxs-lookup"><span data-stu-id="797dd-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="797dd-111">示例</span><span class="sxs-lookup"><span data-stu-id="797dd-111">EXAMPLES</span></span>

### <span data-ttu-id="797dd-112">範例1</span><span class="sxs-lookup"><span data-stu-id="797dd-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="797dd-113">這個範例會取得服務「testApp ~ testService」的服務資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="797dd-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="797dd-114">範例2</span><span class="sxs-lookup"><span data-stu-id="797dd-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="797dd-115">這個範例會在應用程式 "testApp" 下取得服務清單。</span><span class="sxs-lookup"><span data-stu-id="797dd-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="797dd-116">參數</span><span class="sxs-lookup"><span data-stu-id="797dd-116">PARAMETERS</span></span>

### <span data-ttu-id="797dd-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="797dd-117">-ApplicationName</span></span>
<span data-ttu-id="797dd-118">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="797dd-118">Specify the name of the application.</span></span>

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

### <span data-ttu-id="797dd-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="797dd-119">-ClusterName</span></span>
<span data-ttu-id="797dd-120">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="797dd-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="797dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797dd-121">-DefaultProfile</span></span>
<span data-ttu-id="797dd-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="797dd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="797dd-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="797dd-123">-Name</span></span>
<span data-ttu-id="797dd-124">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="797dd-124">Specify the name of the service.</span></span>

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

### <span data-ttu-id="797dd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="797dd-125">-ResourceGroupName</span></span>
<span data-ttu-id="797dd-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="797dd-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="797dd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="797dd-127">-ResourceId</span></span>
<span data-ttu-id="797dd-128">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="797dd-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="797dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797dd-129">CommonParameters</span></span>
<span data-ttu-id="797dd-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="797dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797dd-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="797dd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797dd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="797dd-132">INPUTS</span></span>

### <span data-ttu-id="797dd-133">System.object</span><span class="sxs-lookup"><span data-stu-id="797dd-133">System.String</span></span>

## <span data-ttu-id="797dd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="797dd-134">OUTPUTS</span></span>

### <span data-ttu-id="797dd-135">PSService 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="797dd-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="797dd-136">筆記</span><span class="sxs-lookup"><span data-stu-id="797dd-136">NOTES</span></span>

## <span data-ttu-id="797dd-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="797dd-137">RELATED LINKS</span></span>
