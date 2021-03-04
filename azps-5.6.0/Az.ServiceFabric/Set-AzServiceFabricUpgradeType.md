---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c117937d674c95f69eb967667c86c503ffbb62c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908002"
---
# <span data-ttu-id="e8598-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="e8598-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="e8598-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e8598-102">SYNOPSIS</span></span>
<span data-ttu-id="e8598-103">變更組群的服務結構升級類型。</span><span class="sxs-lookup"><span data-stu-id="e8598-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="e8598-104">語法</span><span class="sxs-lookup"><span data-stu-id="e8598-104">SYNTAX</span></span>

### <span data-ttu-id="e8598-105">自動</span><span class="sxs-lookup"><span data-stu-id="e8598-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8598-106">手動</span><span class="sxs-lookup"><span data-stu-id="e8598-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8598-107">描述</span><span class="sxs-lookup"><span data-stu-id="e8598-107">DESCRIPTION</span></span>
<span data-ttu-id="e8598-108">使用 **Set-AzServiceFabricUpgradeType，** 將升級類型設定為自動升級，或以特定的 Service 內容代碼版本手動設定升級類型。</span><span class="sxs-lookup"><span data-stu-id="e8598-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="e8598-109">例子</span><span class="sxs-lookup"><span data-stu-id="e8598-109">EXAMPLES</span></span>

### <span data-ttu-id="e8598-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e8598-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="e8598-111">此命令將設定為自動的組群升級模式。</span><span class="sxs-lookup"><span data-stu-id="e8598-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="e8598-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8598-112">PARAMETERS</span></span>

### <span data-ttu-id="e8598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8598-113">-DefaultProfile</span></span>
<span data-ttu-id="e8598-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8598-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8598-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8598-115">-Name</span></span>
<span data-ttu-id="e8598-116">指定組名</span><span class="sxs-lookup"><span data-stu-id="e8598-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8598-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8598-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8598-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8598-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e8598-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e8598-119">-UpgradeMode</span></span>
<span data-ttu-id="e8598-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e8598-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8598-121">-版本</span><span class="sxs-lookup"><span data-stu-id="e8598-121">-Version</span></span>
<span data-ttu-id="e8598-122">組代碼版本</span><span class="sxs-lookup"><span data-stu-id="e8598-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8598-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e8598-123">-Confirm</span></span>
<span data-ttu-id="e8598-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e8598-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8598-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8598-125">-WhatIf</span></span>
<span data-ttu-id="e8598-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8598-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8598-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8598-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8598-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8598-128">CommonParameters</span></span>
<span data-ttu-id="e8598-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e8598-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8598-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8598-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8598-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e8598-131">INPUTS</span></span>

### <span data-ttu-id="e8598-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e8598-132">System.String</span></span>

### <span data-ttu-id="e8598-133">Microsoft.Azure.Commands.ServiceFabric.models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e8598-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="e8598-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e8598-134">OUTPUTS</span></span>

### <span data-ttu-id="e8598-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="e8598-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e8598-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e8598-136">NOTES</span></span>

## <span data-ttu-id="e8598-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8598-137">RELATED LINKS</span></span>
