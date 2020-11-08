---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137313"
---
# <span data-ttu-id="a48fa-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a48fa-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="a48fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a48fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a48fa-103">在指定的資源群組和群集底下建立新的 service fabric 應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="a48fa-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="a48fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="a48fa-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a48fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="a48fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a48fa-106">這個 Cmdlet 會在指定的資源群組和群集底下建立新的服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="a48fa-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="a48fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="a48fa-107">EXAMPLES</span></span>

### <span data-ttu-id="a48fa-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a48fa-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="a48fa-109">這個範例會在指定的資源群組和群集底下建立新的應用程式類型「testAppType」。</span><span class="sxs-lookup"><span data-stu-id="a48fa-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="a48fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="a48fa-110">PARAMETERS</span></span>

### <span data-ttu-id="a48fa-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a48fa-111">-ClusterName</span></span>
<span data-ttu-id="a48fa-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a48fa-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a48fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48fa-113">-DefaultProfile</span></span>
<span data-ttu-id="a48fa-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a48fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a48fa-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a48fa-115">-Name</span></span>
<span data-ttu-id="a48fa-116">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="a48fa-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="a48fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="a48fa-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a48fa-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a48fa-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a48fa-119">-Confirm</span></span>
<span data-ttu-id="a48fa-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a48fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a48fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a48fa-121">-WhatIf</span></span>
<span data-ttu-id="a48fa-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a48fa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a48fa-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a48fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a48fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48fa-124">CommonParameters</span></span>
<span data-ttu-id="a48fa-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a48fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48fa-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a48fa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48fa-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a48fa-127">INPUTS</span></span>

### <span data-ttu-id="a48fa-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a48fa-128">System.String</span></span>

## <span data-ttu-id="a48fa-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a48fa-129">OUTPUTS</span></span>

### <span data-ttu-id="a48fa-130">PSApplicationType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a48fa-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="a48fa-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a48fa-131">NOTES</span></span>

## <span data-ttu-id="a48fa-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a48fa-132">RELATED LINKS</span></span>
