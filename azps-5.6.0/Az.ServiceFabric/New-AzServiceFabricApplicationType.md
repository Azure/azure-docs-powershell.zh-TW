---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: f8724fe13cb44ac3e2640f747026c121303be252
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908730"
---
# <span data-ttu-id="84e42-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="84e42-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="84e42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84e42-102">SYNOPSIS</span></span>
<span data-ttu-id="84e42-103">在指定的資源群組和群組下，建立新的服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="84e42-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="84e42-104">語法</span><span class="sxs-lookup"><span data-stu-id="84e42-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e42-105">描述</span><span class="sxs-lookup"><span data-stu-id="84e42-105">DESCRIPTION</span></span>
<span data-ttu-id="84e42-106">Cmdlet 會建立指定資源群組和群組下的新服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="84e42-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="84e42-107">例子</span><span class="sxs-lookup"><span data-stu-id="84e42-107">EXAMPLES</span></span>

### <span data-ttu-id="84e42-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="84e42-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="84e42-109">此範例將在指定的資源群組和群組下建立新應用程式類型"testAppType"。</span><span class="sxs-lookup"><span data-stu-id="84e42-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="84e42-110">參數</span><span class="sxs-lookup"><span data-stu-id="84e42-110">PARAMETERS</span></span>

### <span data-ttu-id="84e42-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="84e42-111">-ClusterName</span></span>
<span data-ttu-id="84e42-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="84e42-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e42-113">-DefaultProfile</span></span>
<span data-ttu-id="84e42-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84e42-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84e42-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="84e42-115">-Name</span></span>
<span data-ttu-id="84e42-116">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="84e42-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84e42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e42-117">-ResourceGroupName</span></span>
<span data-ttu-id="84e42-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84e42-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e42-119">-確認</span><span class="sxs-lookup"><span data-stu-id="84e42-119">-Confirm</span></span>
<span data-ttu-id="84e42-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84e42-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e42-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e42-121">-WhatIf</span></span>
<span data-ttu-id="84e42-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84e42-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84e42-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84e42-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e42-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e42-124">CommonParameters</span></span>
<span data-ttu-id="84e42-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84e42-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e42-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84e42-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e42-127">輸入</span><span class="sxs-lookup"><span data-stu-id="84e42-127">INPUTS</span></span>

### <span data-ttu-id="84e42-128">System.String</span><span class="sxs-lookup"><span data-stu-id="84e42-128">System.String</span></span>

## <span data-ttu-id="84e42-129">輸出</span><span class="sxs-lookup"><span data-stu-id="84e42-129">OUTPUTS</span></span>

### <span data-ttu-id="84e42-130">Microsoft.Azure.Commands.ServiceFabric.models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="84e42-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="84e42-131">筆記</span><span class="sxs-lookup"><span data-stu-id="84e42-131">NOTES</span></span>

## <span data-ttu-id="84e42-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="84e42-132">RELATED LINKS</span></span>
